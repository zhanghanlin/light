# Linux 使用整理

## sudo 免输入密码
sudo的执行顺序是先到/etc/sudoers 中查找用户是否有权限执行sudo命令，如果用户有权限执行则要求用户输入**自己的密码（非root密码）**然后执行
如果想免输入密码只要修改/etc/sudoers文件
```
%sudo ALL=(ALL:ALL) NOPASSWD: ALL
```
## 注册服务chkconfig
```
# 注册服务
sudo chkconfig --add /etc/init.d/nexus
# 开机启动
sudo chkconfig nexus on

sudo service nexus start
```

## 重启网卡
```
ifdown {网卡名}
ifup {网卡名}
```
