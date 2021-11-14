# Download Speed Test
Script to test internet download speed using Ookla Speedtest CLI and exit accordingly.

# How To Install Ookla Speedtest
Go to https://www.speedtest.net/apps/cli and follow the instructions there. This script requires Ookla Speedtest.

# Using This Script
To use this script, simply copy and run in your terminal as root user:
```
rm -rf /usr/share/dlspeedtest /etc/cron.d/dlspeedtest /var/log/dlspeedtest
wget -O /usr/share/ispspeedtest https://raw.githubusercontent.com/ahrasis/Internet-Speed-Test/main/script
wget -O /etc/cron.d/ispspeedtest https://raw.githubusercontent.com/ahrasis/Internet-Speed-Test/main/cron
chmod +x /usr/share/ispspeedtest
```

# Example For Monit
To use with monit refer to https://mmonit.com/monit/documentation/monit.html#PROGRAM-STATUS-TEST e.g. for restarting TP-Link router:
```
check program Internet-Speed-Test with path "/usr/share/ispspeedtest"
       with timeout 500 seconds
       if status != 0
          then exec "(/bin/sleep 2; echo username; /bin/sleep 2; echo password; /bin/sleep 2; echo dev reboot; /bin/sleep 2;) | telnet 192.168.100.100"
       if status = 1 then alert
       alert foo@baz
```

# Cron Time Setting
The time settings in the cron file is set to run autopdate at every hour at minute 30, so do change it to suit your needs.

# Log File
A log file will be created at /var/log/dlspeedtest which may be disabled at your choice by editing the cron file.

# License
Feel free to modify and fork, as though it is set to BSD3, none is mentioned in the script / cron file.
