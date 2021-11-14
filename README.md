# Download Speed Test
Script to test internet download speed using Ookla Speedtest CLI and exit accordingly.

# How To Install Ookla Speedtest
Go to https://www.speedtest.net/apps/cli and follow the instructions there. This script requires Ookla Speedtest.

# How To Use With This Script
To use this script, simply copy and run in your terminal as root user:
```
rm -rf /usr/share/dlspeedtest /etc/cron.d/dlspeedtest
wget -O /usr/share/dlspeedtest https://raw.githubusercontent.com/ahrasis/dlspeedtest/master/script
wget -O /etc/cron.d/dlspeedtest https://raw.githubusercontent.com/ahrasis/dlspeedtest/master/cron
chmod +x /usr/share/dlspeedtest
```

# Log File
A log file will be created at /var/log/dlspeedtest which may be disabled at your choice by editing the cron file.

# License
Feel free to modify and fork, as though it is set to BSD3, none is mentioned in the script / cron file.
