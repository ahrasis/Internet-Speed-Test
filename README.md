# speedtest
Script to test internet speed and exit accordingly

# How To Install Ookla Speedtest
Go to https://www.speedtest.net/apps/cli and follow the instructions there.

# How To Use With This Script
To use this script, simply copy and run in your terminal as root user:
```
rm -rf /usr/share/dlspeedtest /etc/cron.d/dlspeedtest
wget -O /usr/share/dlspeedtest https://raw.githubusercontent.com/ahrasis/autopdate/master/script
wget -O /etc/cron.d/dlspeedtest https://raw.githubusercontent.com/ahrasis/autopdate/master/cron
chmod +x /usr/share/dlspeedtest
```

# Log File
A log file will be created at /var/log/autopdate which may be disabled at your choice by editing the cron file.

# License
Feel free to modify and fork, as though it is set to BSD3, none is mentioned in the script / cron file.
