(1)```https://www.webq.top/2020/11/14/linux/kcptun/```


(2)```https://muyexi.im/shadowsocks_with_kcptun/```

```
# cat /etc/shadowsocks.json 
{
    "server":"0.0.0.0",
    "server_port":49966,
    "local_address":"127.0.0.1",
    "local_port":1080,
    "password":"teddyok123",
    "timeout":300,
    "method":"aes-256-cfb",
    "fast_open":false
}

# cat /usr/lib/systemd/system/ss-server.service
[Unit]
Description=shadowsocks server daemon
After=syslog.target network.target

[Service]
Type=simple
User=nobody
Group=nobody
ExecStart=/usr/bin/ssserver -c /etc/shadowsocks.json

[Install]
WantedBy=multi-user.target
[root@104 ~]# ^C
[root@104 ~]# cat /usr/lib/systemd/system/ss-server.service
[Unit]
Description=shadowsocks server daemon
After=syslog.target network.target

[Service]
Type=simple
User=nobody
Group=nobody
ExecStart=/usr/bin/ssserver -c /etc/shadowsocks.json

[Install]
WantedBy=multi-user.target

# cat /usr/lib/systemd/system/ss-server.service
[Unit]
Description=shadowsocks server daemon
After=syslog.target network.target

[Service]
Type=simple
User=nobody
Group=nobody
ExecStart=/usr/bin/ssserver -c /etc/shadowsocks.json

[Install]
WantedBy=multi-user.target
```

app kcptun
```
key=hongye123;crypt=none;mode=fast2;mtu=1350;sndwnd=512;rcvwnd=512;datashard=10;parityshard=3;dscp=0;nocomp
```

