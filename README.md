# TS3Proxy

TS3Proxy aims to be a complete solution for proxy ts3. It allows you to hide the original location of your teamspeak server and may be a good choice to defeat DDoS-Attacks. Just use multiple instances for different kind of people (like admins, moderators, members and guests) on different virtual machines (in different data centers of course). And it's ideal for users that want to hide their original client IP address.

  - Proxy TS3 UDP Port
  - Proxy TS3 Filetransfer Port
  - Proxy TS3 Serverquery Port

## HowTo configure

Just open the "config.yml" and change the "remoteAddr" to the hostname OR IP of the teamspeak3 server you want to connect to. Please also adjust the ports if they differ. At least the filetransfer ports (relayport and remoteport) need to be exactly the same! Otherwise the filetransfer will not work. All other ports can be adjusted the way you want. There is no need to keep them the same.

### Blacklist / Whitelist

The blacklist or whitelist can be used to ban proxy users by IP or only allow specific users to use the proxy. If you use the whitelist the blacklist will be ignored. All entries in the whitelist will be able to use the proxy, every other IP will be blocked.

There will be a file called "whitelist.txt" and "blacklist.txt" in the root folder. Just type one IP address per line in it and the user won't be able to use the proxy any more.

## HowTo install

Just unzip the latest release (or master branch) zip file and open a terminal in the unzipped folder:

```bash
sudo ./setup.sh
```

And just run it afterwards with an NON-ROOT user via command line:

```bash
ts3proxy
```

## HowTo run (Alternative)

Install all dependencies:

```bash
apt-get install python3-yaml
```

Run the ts3proxy

```bash
python3 -m ts3proxy.ts3proxy
```
