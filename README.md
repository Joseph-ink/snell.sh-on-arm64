# Snell on ARM64

## 主要用于甲骨文云Oracle ARM64 Ubuntu系统

Snell默认使用TLS加密，使用前需设定域名解析并完全使用SSL/TLS加密；

### 推荐使用以下脚本开放全部端口，然后使用mack-a一键脚本开启bbr加速，申请证书并架设代理协议（包含Vmess、Vless、Trojan）；

- [YG-tsj/CFWarp-Pro](https://github.com/YG-tsj/CFWarp-Pro)


实际测试在甲骨文云上使用Snell没有太多速度优势，仅仅多一种协议支持；

Debian & Ubuntu 用户请运行

```
wget --no-check-certificate -O snell.sh https://raw.githubusercontent.com/azurerayID/snell.sh/master/snell.sh
chmod +x snell.sh
./snell.sh
```



首次安装默认端口号13254，如需修改请
在所有脚本运行结束后运行

```
vi /etc/snell/snell-server.conf
systemctl restart snell
```

自行修改。

查看运行状态：

```
systemctl status snell
```

卸载方法：

```
wget --no-check-certificate -O uninstall-snell.sh https://raw.githubusercontent.com/azurerayID/snell.sh/master/uninstall-snell.sh
chmod +x uninstall-snell.sh
./uninstall-snell.sh
```
