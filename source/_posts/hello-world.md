---
title: 搭建Hexo并部署至Linux(centos)云服务器上
---
[已部署]().

## 环境配置

### 本地环境配置

1. Git安装

2. Nodejs安装

3. Hexo安装

   ###### 第一步和第二步安装完成后,进行一些操作

   ###### 生成ssh公钥(公钥作用：设置SSH公钥认证，pull,push不需要每次都输入密码)

   ###### 桌面右键点击Git Bash Here,在打开的页面输入ssh-keygen -t rsa连续敲击回车三次

![](http://img.lmdream.cn/img/blog/hexo/hexo_01.jpg)

###### 		出现如下内容就证明就是成功

![](http://img.lmdream.cn/img/blog/hexo/hexo_02.jpg)

### Centosh环境配置

###### 安装git

``` bash
yum install git
```

###### 创建Git账户

```
adduser git
```

###### 添加账户权限

```
chmod 740 /etc/sudoers
vim /etc/sudoers
```

###### 找到

```
root ALL=(ALL) ALL
```

###### 添加以下内容

```
git ALL=(ALL) ALL
```



### Generate static files

``` bash
$ hexo generate
```

More info: [Generating](https://hexo.io/docs/generating.html)

### Deploy to remote sites

``` bash
$ hexo deploy
```

More info: [Deployment](https://hexo.io/docs/one-command-deployment.html)

