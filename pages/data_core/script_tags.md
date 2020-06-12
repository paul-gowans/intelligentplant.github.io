# Script Tags

Script Tags provide a highly configurable way to define calculation and
event raising tags.

Script tags can be written in:

  - C\#
  - FLEE (Fast Lightweight Expression Evaluation) - [more
    info](https://github.com/mparlak/Flee/wiki/Examples)
  - Javascript

## Script Tag Templates

A number of pre-configured script tags exist to perform the following
funcitons:

### Calculations

  - **Average Calculator**  
    Periodically calculates the average value of a process tag.

<!-- end list -->

  - **Delta Calculator**  
    Calculates the delta between the value of two input tags.

<!-- end list -->

  - **Gas Velocity Calculator**  
    Calculates gas velocity using flow rate and pressure.

### Sensor Quality Checks

  - **Bad Data Detection**  
    Data quality check that raises alert if monitored tag returns NaN or
    has a 'bad' status. 

<!-- end list -->

  - **Channel Deviation Detection**  
    Checks for deviation in output from a sensor with two data channels.
    An alert indicates that one or both of the channels is unreliable.
    The method is to regularly compare Channel A and Channel B and check
    if difference is within acceptable instrument error tolerance.
    Default configuration is to check 24hr average difference 4 times
    per day.

<!-- end list -->

  - **Flatline Detection**  
    Script tag that checks for flatlining data (i.e. process tags where
    the tag may be updating regularly, but the sensor value is not
    changing).

<!-- end list -->

  - **Frozen Signal Detection**  
    Script tag that periodically ensures that newer values are being
    received for a tag.

### Process Data Alerts

  - **Equipment Running Status Monitor**  
    Monitors the running status of a piece of equipment and triggers and
    resets events when the status changes. 

<!-- end list -->

  - **Fleeting Excursion Monitor**  
    Script tag template for monitoring sensors such as acoustic sand
    probes that can generate fleeting excursions.

<!-- end list -->

  - **Limit Monitor**  
    Script tag that periodically monitors a process tag value against a
    limit using MIN/MAX aggregated data.  
    *Use the FleetingExcursionMonitor template if you require a high
    degree of accuracy.*

<!-- end list -->

  - **Time Based Delta Monitor**  
    Monitors the rate of change of a process tag over a time period.
