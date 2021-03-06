# Purple Air Watchdog

## Instructions
Replace the `SENDER` and `RECIPIENT` variables with strings of desired email accounts. They can be the same email for each variable. 
The `SENDER` must be a gmail account with the current script. The `Gmail` class may be modified in the future to work with different providers.

## Description
This is a simple python2 script designed to detect when the [Sustainable Atmospheres Research Lab](https://star.research.pdx.edu/)'s [PurpleAir sensors](https://www.purpleair.com/) stop uploading to their respective API. 

The script scans PurpleAir's API every 15 minutes. If a sensor goes offline for more than 1 hour, an email is sent to the user. The offending sensor ID is also appended to a list of `offline_sensors` to prevent multiple emails being sent per day. This list is cleared every 24 hours, to remind the user if a sensor has been offline over consecutive days. 

The email class was developed with gmail accounts in mind. It may not work with other `SENDER` addresses.

Getpass allows the user to privately enter the email `SENDER` password via commandline to avoid the security issues of a hardcoded password.

This work was funded by the USFS [Canopy Continuum project](https://canopycontinuum.org/). 
