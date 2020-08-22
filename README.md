# Cloudflare Dynamic DNS Update

[![N|Solid](https://img.icons8.com/color/2x/cloudflare.png)](https://github.com/OnlyHardOfficial/cloudflare-ddns-update)

[![Build Status](https://travis-ci.org/joemccann/dillinger.svg?branch=master)](https://travis-ci.org/joemccann/dillinger)

Cloudflare API v4 Dynamic DNS Update in Bash.
 >  This file allows the auto update of the cloudflare dns in a paratic and intuitive way --> working perfectly in [22/08/2020]

  - The script only change only a especific destination on cloudflare record
  - Unlike other scripts, if there are several records, all would be changed.
While with this method only the mentioned record will be changed
  - [KISS principle](https://en.wikipedia.org/wiki/KISS_principle)

# [All Features]


```sh
 Folder --> SecureWay
```
This folder /SecureWay/cfupdate move to /bin/*  --> Executes scripts in an improved way
This folder /SecureWay/cfconfig move to /etc/* --> This directory is secure where you can put something like credentials
It is a way,  implement same script more and safely via cronjob "crontab -e":
```sh
@reboot /bin/cfupdate
*/10 * * * * /bin/cfupdate
```
This cron will run when system is @rebooted and every 10 minutes
##############################################################################################
#############################################################################################

# Based on benkulbertis/cloudflare-update-record.sh
```sh
auth_email="your-email@example.com"                # The email used to login 'https://dash.cloudflare.com'
auth_key="0000000000000000000000000000000000000"   # Top right corner, "My profile" > "Global API Key"
zone_identifier="00000000000000000000000000000000" # Can be found in the "Overview" tab of your domain
sleep_seconds=300                                  # Run every 5 minutes
```
  - create a file nameyouwant on -->/etc/init.d/    with folow content:
```sh
#!/bin/bash
@reboot /home/username/foldername/cloudflare-update-record.sh
```

 
 
  - This way the script will be called every time the system is restarted
  
