## Snell一键脚本,支持x86、ARM64架构,支持ipv4，ipv6网络；
### Snell Server版本更新至v3.0.1正式版

#### 甲骨文云Oracle ARM64建议安装Ubuntu，然后直接DD系统，方便使用

以下为Debian 11 64位，支持aarch64
```
wget -N --no-check-certificate https://raw.githubusercontent.com/veip007/dd/master/InstallNET.sh && chmod +x InstallNET.sh && ./InstallNET.sh -d 11 -v 64 -p "自定义root密码" -port "自定义ssh端口"
```

#### 然后使用mack-a一键脚本开启bbr加速，申请证书并架设代理协议（包含Vmess、Vless、Trojan）；

```
wget -P /root -N --no-check-certificate "https://raw.githubusercontent.com/mack-a/v2ray-agent/master/install.sh" && chmod 700 /root/install.sh && /root/install.sh
```

实际测试在甲骨文云上使用Snell没有太多速度优势，仅仅多一种协议支持；

#### ARM64  Debian & Ubuntu 请运行

```
wget --no-check-certificate -O snell.sh https://raw.githubusercontent.com/Joseph-ink/snell.sh-on-arm64/master/snell_arm64.sh
chmod +x snell.sh
./snell.sh
```

#### x86  Debian & Ubuntu 请运行

```
wget --no-check-certificate -O snell.sh https://raw.githubusercontent.com/Joseph-ink/snell.sh-on-arm64/master/snell_amd64.sh
chmod +x snell.sh
./snell.sh
```

#### x86 ipv6  Debian & Ubuntu 请运行

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
