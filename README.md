# Internet Speed Test
Script to test internet download speed using Ookla Speedtest CLI.

# How To Install Ookla Speedtest
Go to https://www.speedtest.net/apps/cli and follow the instructions there. This script requires Ookla Speedtest.

# Using This Script
To use this script, simply copy and run in your terminal as root user:
```
wget -O /usr/share/ispspeedtest https://raw.githubusercontent.com/ahrasis/Internet-Speed-Test/main/script
wget -O /etc/cron.d/ispspeedtest https://raw.githubusercontent.com/ahrasis/Internet-Speed-Test/main/cron
chmod +x /usr/share/ispspeedtest
```

# Example For Monit
To use with monit refer to https://mmonit.com/monit/documentation/monit.html:

# Cron Time Setting
The time settings in the cron file is set to run autopdate at every 30 minutes, so do change it to suit your needs.

# Log File
A log file will be created at /var/log/ispspeedtest which may be disabled at your choice by editing the cron file.

# License
Feel free to modify and fork, as though it is set to BSD3, none is mentioned in the script / cron file.
