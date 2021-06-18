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
wget --no-check-certificate -O uninstall-snell.sh https://raw.githubusercontent.com/primovist/snell.sh/master/uninstall-snell.sh
chmod +x uninstall-snell.sh
./uninstall-snell.sh
```
