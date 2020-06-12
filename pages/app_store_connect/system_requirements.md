# App Store Connect: System Requirements

App Store Connect consists of a base windows service with data
connection drivers and components. Each has its own minimum system
requirements.

### App Store Connect Windows Service

*Base windows service on which App Store Data Connections are hosted.*

  - Windows Server 2008 x64 or above 
  - 8GB RAM
  - 1.4 Ghz Dual Core Processor or above
  - .Net Framework 4.6.2
  - Active internet connection permitting access to App Store
  - Data Volume Disk Space: +5GB (depending on your requirements)
  - Port 443 (HTTPS) access to appstore.intelligentplant.com

### Intelligent Plant Alarm Analysis Data Source Driver

  - If actively recording alarm events, allocate approx 3GB per 1
    million events.

### Intelligent Plant Historian Data Source Driver

  - If actively recording process data, allocate approx 60MB per 1
    million records.

### Matrikon ProcessNet Data Source Driver

  - No additional requirements

### OPC DA/HDA Data Source Driver

  - OPC Foundation Core Components (provided by OPC vendor)

### OSIsoft Asset Framework Data Source Driver

  - PI AF Client 2014
    (<https://techsupport.osisoft.com/Products/PI-Server/PI-AF/System-Requirements>)

### OSIsoft PI Data Source Driver

  - PI AF Client 2014
    (<https://techsupport.osisoft.com/Products/PI-Server/PI-AF/System-Requirements>)
