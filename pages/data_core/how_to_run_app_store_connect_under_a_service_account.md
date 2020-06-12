# How to Run App Store Connect under a Service Account

When configuring a Data Source Connection in **App Store Connect** you
have the option to specify username and password credentials. However,
this may not always be desired.

Rather than specify explicit credentials in the connection object, you
may prefer to have the underlying App Store Connect Windows Service
employ an account that has data access permissions.

*The following instructions describe how to enable this process:*

**1. Do not specify user credentials in Data Source Connection**

If left blank the default behaviour is to use App Store Connect service
account.

![](/data_core/ServiceAcct03.png)

**2. Service Account Security**

As well as PI Access, the service account should have rights configured
on the local server folder:

  - Read & Execute: %ProgramFiles%/Intelligent Plant
  - Full Control: %ProgramData%/Intelligent Plant

**3. Modify the App Store Connect Service Account**

3.1 In Windows Services, select: **Intelligent Plant Data Core Service**

![](/data_core/ServiceAcct01.png)

3.2. Change default Local System account to preferred alternative.

![](/data_core/ServiceAcct02.png)
