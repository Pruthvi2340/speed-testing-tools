# speed-testing-tools

# Speedtest by Ookla
```
sudo apt-get install curl
curl -s https://packagecloud.io/install/repositories/ookla/speedtest-cli/script.deb.sh | sudo bash
sudo apt-get install speedtest
speedtest
```
# fast by Netflix
```
wget https://github.com/ddo/fast/releases/download/v0.0.4/fast_linux_amd64
sudo install fast_linux_amd64 /usr/local/bin/fast
which fast
fast
```

# nethogs
```
sudo apt-get install nethogs
nethogs -V
sudo nethogs
```

# iperf
```
sudo apt-get install iperf3 -y
iperf3 -s -p 2323                            # Start listen specific port on server
iperf3 -c 192.168.149.69 -p 2323             # Start client mode with listen port on the server
iperf3 -c 192.168.149.69 -p 2323 -P 3 -t 30  # set time in seconds to transmit for (default 10 secs) as follows
```

# Check Ports lintening same server
```
sudo ss -tunl  # same server
sudo netstat -tunpl
sudo lsof -nP -iTCP -sTCP:LISTEN
sudo lsof -nP -iUDP:53
```
# Check Ports lintening remote server (replace localhost with <remote-ip>)
```
sudo nmap -n -PN -sT -sU -p- localhost               # nmap to check listening ports on localhost or remote
nc -z -v localhost 1-65535                           # netcat to check listening 1-65535 ports on localhost or remote
nc -z -v -u localhost 1-65535 2>&1 | grep succeeded  # netcat to check listening ports which are opened on remote or localhost
```
