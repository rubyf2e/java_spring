# java_spring
java spring 練習


```
sudo apt-get install default-jre
```
```
ufw allow 8080
```
```
netstat -aon
```
```
sudo ln -s /var/www/java_spring/java_spring.jar /etc/init.d/java_spring
```


```
vi /etc/systemd/system/java_spring.service
```


```
[Unit]
Description=java_spring
After=syslog.target

[Service]
User=java_spring
ExecStart=/var/www/java_spring/java_spring.jar
SuccessExitStatus=143

[Install]
WantedBy=multi-user.target

```


```
vim .bashrc
```
#在.bashrc檔案內增加此行 export LC_ALL="en_US.UTF-8"

```
sudo locale-gen zh_TW.UTF-8
```
```
sudo dpkg-reconfigure locales
```
```
systemctl enable java_spring.service
```
```
/etc/init.d/java_spring start
```
