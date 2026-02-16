#### Decoys
```bash
nmap -sS -Pn -D 10.10.10.1,10.10.10.2,ME -F MACHINE_IP
```
```bash
nmap -sS -Pn -D RND,RND,ME -F MACHINE_IP
```

#### Proxy
```bash
nmap -sS -Pn --proxies PROXY_URL -F MACHINE_IP
```

#### Spoofed MAC Address
```bash
--spoof-mac MAC_ADDRESS
```
#### Spoofed IP Address
```bash
-S IP_ADDRESS
```
#### Fixed Source Port Number
```bash
nmap -sS -Pn -g 8080 -F MACHINE_IP
```

## This is a quick summary of the Nmap options discussed in this task.

| Evasion Approach                              | Nmap Argument                             |     |
| --------------------------------------------- | ----------------------------------------- | --- |
| Hide a scan with decoys                       | `-D DECOY1_IP1,DECOY_IP2,ME`              |     |
| Hide a scan with random decoys                | `-D RND,RND,ME`                           |     |
| Use an HTTP/SOCKS4 proxy to relay connections | `--proxies PROXY_URL`                     |     |
| Spoof source MAC address                      | `--spoof-mac MAC_ADDRESS`                 |     |
| Spoof source IP address                       | `-S IP_ADDRESS`                           |     |
| Use a specific source port number             | `-g PORT_NUM` or `--source-port PORT_NUM` | ry  |




