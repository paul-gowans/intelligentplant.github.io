# App Store Connect: Back Up and Restore

App Store Connect is quick to install, but at some point you may wish to
consider a back up policy. Particularly if you've configured multiple
data sources and/or are using the built-in Edge Historian to store
application data (e.g. Alarm Analysis or Controller Consultant reports).

Depending on your circumstances, the following options are available:

## Virtual Machine Snapshot

If App Store Connect is installed on a Virtual Machine, snapshot is a
reliable way to back-up an entire server. However, we also recommend
backing up "Big Data" as well (see below). Refer to VM documentation for
information on how to create, schedule and restore snapshots.

## Manual Backup

If snapshot is not an option, configuration and data files can be
manually backed up and restored. Instructions are provided below.

**1. Back Up App Store Connect Configuration**

To protect against hardware failure, the contents of the App Store
Connect program-data folder should be copied to an alternative location.

  - C:\\ProgramData\\Intelligent Plant\\Data Core Application
    Host\\Service\\Applications\\App Store Connect

**2. Back Up Big Data**

2.1. Take a database Snapshot

Execute the BackupUtility batch file "Snapshot.bat" to run.

  - BackupUtility: c:\\Program Files\\Intelligent Plant\\Big
    Data\\BackupUtility\\Snapshot.bat

![](/app_store_connect/backup01.png)

This creates a database restore point protecting against data corruption
or accidental loss.

The console window automatically closes after 10 seconds.

2.2 Archive back-up files

To protect against hardware failure, the contents of the back-up folder
should be copied to an alternative location.

  - BackUp Folder: C:\\Program Files\\Intelligent Plant\\Big
    Data\\es\\backup

## Manual Restore

**1. To recover App Store Connect configuration**

1.1 Stop Intelligent Plant Data Core windows service

1.2 Revert configuration files from archive

1.3 Re-start Intelligent Plant Data Core windows service

**2. Revert Big Data to a snapshot**

For advanced Snapshot management (create/delete/list/restore) open the
BackupUtility manager: double click "BackupUtility.exe".

![](/app_store_connect/backup04.png)

List returns all available snapshots. Note the snapshot id is actually a
time-stamp (format: YYYYMMddHHmmss).

Enter: Restore *SnapshotID* (e.g. Restore 20170131093011)

## Scheduled Backup

To configure a regular scheduled backup, create a Windows Scheduled Task
to execute one of following batch files:

  - **Snapshot.bat** - Execute a snapshot

<!-- end list -->

  - **SnapshotWithPurge.bat** - Execute a snapshot withpurge (purge is
    explained in the Data Retention Policy section below).

Below is a sample configuration.

NB. Remember to specify a valid account and adjust schedule to your own
preference.

``` xml

<?xml version="1.0" encoding="UTF-16"?>
<Task version="1.2" xmlns="http://schemas.microsoft.com/windows/2004/02/mit/task">
  <RegistrationInfo>
    <Date>2019-03-25T15:49:45.0817232</Date>
    <Author>Intelligent Plant</Author>
    <Description>Daily Big Data Backup</Description>
  </RegistrationInfo>
  <Triggers>
    <CalendarTrigger>
      <StartBoundary>2019-03-25T23:02:55</StartBoundary>
      <Enabled>true</Enabled>
      <ScheduleByDay>
        <DaysInterval>1</DaysInterval>
      </ScheduleByDay>
    </CalendarTrigger>
  </Triggers>
  <Principals>
    <Principal id="Author">
      <UserId></UserId>
      <LogonType>Password</LogonType>
      <RunLevel>HighestAvailable</RunLevel>
    </Principal>
  </Principals>
  <Settings>
    <MultipleInstancesPolicy>IgnoreNew</MultipleInstancesPolicy>
    <DisallowStartIfOnBatteries>true</DisallowStartIfOnBatteries>
    <StopIfGoingOnBatteries>true</StopIfGoingOnBatteries>
    <AllowHardTerminate>true</AllowHardTerminate>
    <StartWhenAvailable>false</StartWhenAvailable>
    <RunOnlyIfNetworkAvailable>false</RunOnlyIfNetworkAvailable>
    <IdleSettings>
      <StopOnIdleEnd>true</StopOnIdleEnd>
      <RestartOnIdle>false</RestartOnIdle>
    </IdleSettings>
    <AllowStartOnDemand>true</AllowStartOnDemand>
    <Enabled>true</Enabled>
    <Hidden>false</Hidden>
    <RunOnlyIfIdle>false</RunOnlyIfIdle>
    <WakeToRun>false</WakeToRun>
    <ExecutionTimeLimit>P3D</ExecutionTimeLimit>
    <Priority>7</Priority>
  </Settings>
  <Actions Context="Author">
    <Exec>
      <Command>"c:\Program Files\Intelligent Plant\Big Data\BackupUtility\SnapshotWithPurge.bat"</Command>
      <WorkingDirectory>c:\Program Files\Intelligent Plant\Big Data\BackupUtility</WorkingDirectory>
    </Exec>
  </Actions>
</Task>

```

## Data Retention Policy

Snapshot takes an incremental backup of the Big Data state. Incremental
means each snapshot is dependent on the others that have gone before it,
and thus may become inefficient if too many snapshots are maintained.
Therefore, it is advised to have an archiving and data retention policy
in place.

## Archiving Snapshots

Snapshots are saved to a backup folder. For a typical App Store Connect
installation, the location is:

\<code\> C:\\Program Files\\Intelligent Plant\\Big Data\\es\\backup
\</code\>

*For custom configuration, see [Big Data Service: Modify Data Storage
Location](/big_data_service/modify_data_storage_location)*

Providing a Snapshot is not actively being taken, it is safe to **copy**
the entire "Snapshots" folder to an achive location.

**Do not cut or delete files from Snapshots** as this will break the
incremental integrity of the files contained.

## Safely Removing Snapshots / Purge Command

Snapshots can be removed using the Backup Utility and executing the
**Purge** command. This will delete old snapshots according to the
retention policy defined in the config file.

The default snapshot retention is 14 days.

To modify the retention policy:

1\. Open the BackUp Utility config file.  
For a default installation, the config file is located:

    C:\Program Files\Intelligent Plant\Big Data\BackupUtility\BackupUtility.exe.config

2\. Refer to **AppSettings** section and modify **DayRetentionPolicy**
setting.

``` 

  <appSettings>
    <add key="BigDataUrl" value="http://localhost:9200"/>
    <add key="log4net.Internal.Debug" value="false"/>
    <add key="DayRetentionPolicy" value="14"/>
  </appSettings>

```

3\. Save file \\\\The new setting will take effect the next time the
BackupUtility is started.
