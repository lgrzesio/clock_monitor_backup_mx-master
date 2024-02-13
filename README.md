# NOTE:This script doesn't support SCBE3!!
# Description

    This script hourly checks 19.44MHz central clock failure on backup CB.
    Syslog message '19.44 MHz clock failure on backup CB' would be shown up on master RE when backup clock failes.
    Target platform: MX240/480/960/2010/2020

# Installation

 - Copy this file as /var/db/scripts/event/clock_monitor_backup_mx.slax under both REs.

 - Configuration.
 
    set event-options event-script file clock_monitor_backup_mx.slax

 - Recommended optional configuration

    set event-options event-script optional
    set system scripts synchronize


# Version History
- V1.0 initial release
- V1.1/V1.2 Added support for SCBE3
- V1.3 Added timeout (-t5) to rsh to avoid dead lock when backup RE is not responding
