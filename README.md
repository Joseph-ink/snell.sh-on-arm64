#### 甲骨文云Oracle建议安装Ubuntu，然后开启内置额外防火墙

#### 建议使用mack-a一键脚本开启bbr加速，申请证书并架设代理协议（包含Vmess、Vless、Trojan）；

```
wget -P /root -N --no-check-certificate "https://raw.githubusercontent.com/mack-a/v2ray-agent/master/install.sh" && chmod 700 /root/install.sh && /root/install.sh
```

### Snell一键脚本,支持x86、ARM64架构,支持ipv4，ipv6网络；Snell Server更新至v3.0.1正式版

#### ARM64 Debian & Ubuntu IPv4 请运行

```
wget --no-check-certificate -O snell.sh https://raw.githubusercontent.com/Joseph-ink/snell.sh-on-arm64/master/snell_arm64.sh
chmod +x snell.sh
./snell.sh
```
#### ARM64 Debian & Ubuntu IPv6 请运行
```
wget --no-check-certificate -O snell.sh https://raw.githubusercontent.com/Joseph-ink/snell.sh-on-arm64/master/snell_arm64_ipv6.sh
chmod +x snell.sh
./snell.sh
```

#### AMD64 Debian & Ubuntu IPv4 请运行

```
wget --no-check-certificate -O snell.sh https://raw.githubusercontent.com/Joseph-ink/snell.sh-on-arm64/master/snell_amd64.sh
chmod +x snell.sh
./snell.sh
```

#### AMD64 Debian & Ubuntu IPv6 请运行

```
wget --no-check-certificate -O snell.sh https://raw.githubusercontent.com/Joseph-ink/snell.sh-on-arm64/master/snell_amd64_ipv6.sh
chmod +x snell.sh
./snell.sh
```


首次安装默认端口号989，如需修改请
在所有脚本运行结束后运行

```
vi /etc/snell/snell-server.conf
```

自行修改并重启
```
systemctl restart snell
```

查看运行状态：

```
systemctl status snell
```

卸载方法：

```
wget --no-check-certificate -O uninstall-snell.sh https://raw.githubusercontent.com/Joseph-ink/snell.sh-on-arm64/master/uninstall-snell.sh
chmod +x uninstall-snell.sh
./uninstall-snell.sh
```
