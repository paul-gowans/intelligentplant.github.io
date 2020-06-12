### Instructions

**1. Prepare Big Data Service for Backups**

Before we can take a back-up, a configuration change is required. This
modification is only required on initial set-up.

If you have already downloaded, deployed and configured the Back-Up
utility (or installed "App Store Connect" which includes the back-up
utility) proceed to step 3.

**1.1. Stop the Big Data Service**

![](/app_store_connect/backup00.png)

Open Windows Services.

Find “Intelligent Plant Big Data Service”.

Right click, then select “Stop”.

**1.2. Set a back-up location**

Edit Elasticsearch configuration file: C:\\Program Files\\Intelligent
Plant\\Big Data\\es\\config\\elasticsearch.yml

*This is a text file using YAML format and can be edited using Wordpad.*

``` 

#Define Physical Repo for snapshots
#More info: <https://www.elastic.co/guide/en/elasticsearch/reference/current/modules-snapshots.html>
path.repo: ["backup"]

```

Uncomment the path.repo entry (remove hash) and enter a back up location
(e.g. "backup").

*NB. The suggested location ("backup") is relative to the big data
service. To store data to an explicit location use format
"c:\\\\temp\\\\Backup" (with double back-slashes).*

**1.3. Restart the Big Data Service**

![](/app_store_connect/backup02.png)

Open Windows Services. Find “Intelligent Plant Big Data Service”. Right
click, then select “Start”.

**2. Download the Big Data Back Up Utility**

Download and unzip the contents of the BackupUtility to your App Store
Connect server.

  - [Download
    BackupUtility](https://appstore.intelligentplant.com/nuget/downloads/BackupUtility.zip)

We suggest deploying the back-up utility to the Intelligent Plant
programs folder:

  - C:\\Program Files\\Intelligent Plant\\BackupUtility

\*\*3. Take a Snapshot \*\*

Open the BackupUtility folder and double click "Snapshot.bat" to run.

![](/app_store_connect/backup01.png)

This creates a database restore point protecting against data corruption
or accidental loss.

The console window automatically closes after 10 seconds.

\*\* 3.1 Manage Snapshots (optional) \*\*

For advanced Snapshot management (create/delete/list/restore) open the
BackupUtility manager: double click "BackupUtility.exe".

![](/app_store_connect/backup04.png)

### 3 Archive back-up files

To protect against hardware failure, the contents of the back-up folder
should be copied to an alternative location.

  - BackUp Folder: C:\\Program Files\\Intelligent Plant\\Big
    Data\\es\\backup
