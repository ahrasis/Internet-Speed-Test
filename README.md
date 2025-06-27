# Internet Speed Test
Script to test internet download speed using Ookla Speedtest CLI.

# How To Install & Setup Ookla Speedtest
Go to https://www.speedtest.net/apps/cli and follow the instructions there. This script requires Ookla Speedtest.

Since there may be some errors, below is the modified way:
```
curl -fsSL https://packagecloud.io/ookla/speedtest-cli/gpgkey | gpg --dearmor > /usr/share/keyrings/ookla_speedtest-cli-archive-keyring.gpg
apt remove speedtest-cli -y
apt install speedtest -y
```

Add Sources "list" file - The Old Way (Single Line Format)
```
echo "deb [signed-by=/usr/share/keyrings/ookla_speedtest-cli-archive-keyring.gpg] https://packagecloud.io/ookla/speedtest-cli/ubuntu jammy main
deb-src [signed-by=/usr/share/keyrings/ookla_speedtest-cli-archive-keyring.gpg] https://packagecloud.io/ookla/speedtest-cli/ubuntu jammy main" | sudo tee -a /etc/apt/sources.list.d/ookla_speedtest-cli.list
```

Just use "sources" file - The New Way (DEB822 Source Format)
```
echo "Types: deb
URIs: https://packagecloud.io/ookla/speedtest-cli/ubuntu/
Suites: jammy
Components: main
Signed-By: /usr/share/keyrings/ookla_speedtest-cli-archive-keyring.gpg" | sudo tee -a /etc/apt/sources.list.d/ookla_speedtest-cli.sources
```

# Using This Script
To use this script, simply copy and run in your terminal as root user:
```
wget -O /usr/share/ispspeedtest https://raw.githubusercontent.com/ahrasis/Internet-Speed-Test/main/script
wget -O /etc/cron.d/ispspeedtest https://raw.githubusercontent.com/ahrasis/Internet-Speed-Test/main/cron
chmod +x /usr/share/ispspeedtest
```

# Example For Monit
To use with monit refer to https://mmonit.com/monit/documentation/monit.html. The easiest would be to print one word result in a file and then use monit to check that file with if content = "result" then...

# Cron Time Setting
The time settings in the cron file is set to run autopdate at every 15 minutes, so do change it to suit your needs.

# Log File
A log file will be created at /var/log/ispspeedtest which may be disabled at your choice by editing the cron file.

# License
Feel free to modify and fork, as though it is set to BSD3, none is mentioned in the script / cron file.
