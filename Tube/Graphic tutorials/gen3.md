# 写在前面

## &emsp;联系方式：  

## &emsp;&emsp;<u>[微信公众号](https://raw.githubusercontent.com/ssooenftzero/0X/master/YouTube/icon/%E5%BE%AE%E4%BF%A1%E5%85%AC%E4%BC%97%E5%8F%B7.JPG)</u>

## &emsp;&emsp;<u>[YouTube](https://www.youtube.com/channel/UCS6QM2n96qXmqURNikf3ceA?view_as=subscriber)</u>
==============================================		

# 谷歌云搭建Trojan科学上网，用cloudflare代理保护我们的IP地址不被墙。

## 创建实例，详情请跟着视频做。
------------------------------------
## SSH链接实例[视频中用到的xshell链接](https://pan.baidu.com/s/1z_gB9DUuAQYGDL8eVyrX1w)提取码：lvte 

## trojan一键脚本，开启TLS1.3，系统支持centos7+/debian9+/ubuntu16+

### curl -O https://raw.githubusercontent.com/atrandys/trojan/master/trojan_mult.sh && chmod +x trojan_mult.sh && ./trojan_mult.sh

### 执行以上过程时详细教程跟随视频。

### 以上代码执行完毕，窗口显示一串下载链接eg：

### 复制以上链接到浏览器下载即可，可能需要扶墙。
------------------------------------
## 另外建议安装bbr加速，建议锐速。

## 第一次执行脚本安装锐速

### cd /usr/src && wget -N --no-check-certificate "https://raw.githubusercontent.com/chiakge/Linux-NetSpeed/master/tcp.sh" && chmod +x tcp.sh && ./tcp.sh

## 第二次执行脚本开启锐速

### cd /usr/src && wget -N --no-check-certificate "https://raw.githubusercontent.com/chiakge/Linux-NetSpeed/master/tcp.sh" && chmod +x tcp.sh && ./tcp.sh

## 至此vps上操作完毕。

## 愉快的使用Trojan吧！！！
------------------------------------
# 如果你不会使用Trojan客户端，请参照这期视频使用Trojan[客户端](https://youtu.be/jx7BlLwpAl0)
------------------------------------
# 附加

## trojan服务端修改密码

### vi /usr/src/trojan/server.conf

### 修改完成后，重启trojan服务端即可，同时客户端的密码也要同步修改

### systemctl restart trojan

# 如有纰漏，请联系up反馈！！！