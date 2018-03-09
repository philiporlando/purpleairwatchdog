# Purple Air Watchdog

This is a simple python2 script designed to detect when Portland State University's [Sustainable Atmospheres Research Lab](https://star.research.pdx.edu/) [PurpleAir sensors](https://www.purpleair.com/) stop uploading to their respective API. 

The script scans PurpleAir's API every 15 minutes. If a sensor goes offline for more than 1-hour, an email is sent to the user. The offending sensor ID is also appended to a list of offline_sensors to prevent multiple emails being sent per day. This list is cleared every 24 hours, to remind the user if a sensor has been offline fore consecutive days. 

The email class was developed with gmail accounts in mind. It may not work with other SENDER addresses.

Getpass allows the user to privately enter the email SENDER password via commandline to avoid the security issues of a hardcoded password.

This work was funded by the USFS [Canopy Continuum project](https://canopycontinuum.org/). 
