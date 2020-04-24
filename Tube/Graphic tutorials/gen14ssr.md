------------------

### 准备工作

#### 服务器

#### 域名

#### 静态网页模板[下载](https://www.free-css.com/)

-------------------------

### 开始安装

#### **Caddy[简介](https://zh.wikipedia.org/wiki/Caddy)一键安装脚本**

```
wget -N --no-check-certificate https://raw.githubusercontent.com/ToyoDAdoubi/doubi/master/caddy_install.sh && chmod +x caddy_install.sh && bash caddy_install.sh
```



#### 域名解析

##### 域名后台解析到服务器IP

#### 域名注入

##### ssh客户端输入

```
cd /usr/local/caddy
```

###### *查看/usr/local/caddy目录下有没有Caddyfile

```
echo "http://sjp2.hqkjw.xyz:80 {
redir https://sjp2.hqkjw.xyz:1234{url}
}
https://sjp2.hqkjw.xyz:1234 {
gzip
tls xqhssgg@gmail.com
root /var/www/
redir https://域名{uri} 301
}" > /usr/local/caddy/Caddyfile
```

###### *此段代码意思，直接新建Caddyfile文件并写入“引号内信息”

#### 静态网页模板放置

##### **在var/www/路径下放置网页**

##### 其他caddy命令

```
启动：service caddy start
停止：service caddy stop
重启：service caddy restart
查看状态：service caddy status
查看Caddy启动日志： tail -f /tmp/caddy.log
Caddy配置文件位置：/usr/local/caddy/Caddyfile
```

##### 测试访问，浏览器地址栏输入域名，看是否能够正常访问静态网页

------

#### **SSR一键搭建脚本**

```
wget --no-check-certificate -O shadowsocks-all.sh https://raw.githubusercontent.com/teddysun/shadowsocks_install/master/shadowsocks-all.sh
chmod +x shadowsocks-all.sh
./shadowsocks-all.sh 2>&1 | tee shadowsocks-all.log
```

##### 其他ssr命令

```
启动SSR：
/etc/init.d/shadowsocks-r start
退出SSR：
/etc/init.d/shadowsocks-r stop
重启SSR：
/etc/init.d/shadowsocks-r restart
SSR状态：
/etc/init.d/shadowsocks-r status
卸载SSR：
./shadowsocks-all.sh uninstall
```

##### 更改ssr的相关配置参数，配置文件路径

```
/etc/shadowsocks-r/config.json
```

------

#### 修改配置文件

```
vi /etc/shadowsocks-r/config.json
```

##### “server_port”: 端口改为443

```
eg:“server_port”:443,
```

##### "redirect": ["*:443#[127.0.0.1:前面caddy用到的端口]

```
eg:"redirect":["*:443#127.0.0.1:1234],
```

#####  重启SSR服务

#### 自愿安装bbr

```
cd /usr/src && wget -N --no-check-certificate "https://raw.githubusercontent.com/chiakge/Linux-NetSpeed/master/tcp.sh" && chmod +x tcp.sh && ./tcp.sh
```

