#

# 写在前面

## &emsp;联系方式：  

## &emsp;&emsp;<u>[微信公众号](https://raw.githubusercontent.com/ssooenftzero/0X/master/YouTube/icon/%E5%BE%AE%E4%BF%A1%E5%85%AC%E4%BC%97%E5%8F%B7.JPG)</u>

## &emsp;&emsp;<u>[YouTube](https://www.youtube.com/channel/UCS6QM2n96qXmqURNikf3ceA?view_as=subscriber)</u>
==============================================		
#

# iOS 使用解锁 TikTok （国际版）区域限制【QuantumultX 篇】

## &emsp;&emsp;文章开始

## &emsp;&emsp;感谢[花姐](https://github.com/ConnersHua/Profiles)

## &emsp;&emsp;感谢[NobyDa](https://github.com/NobyDa)

# -----------------------------------------------------------

# 解锁 Tiktok 操作前必看

## &emsp;&emsp;iMazing 备份TikTok，避免后续不小心更新Tiktok；

## &emsp;&emsp;请使用正版圈x软件，如何查看正版

## &emsp;&emsp;如下【绿色对勾为正版标识】：

## &emsp;&emsp;![正版圈x标识](https://raw.githubusercontent.com/ssooenftzero/0X/master/YouTube/icon/zbbs.png)

## &emsp;&emsp;下期教大家fiddler抓包下载旧版tiktok，绝对正版软件的旧版，不是破解版！！！

## &emsp;&emsp;本人现在使用AppStore最新版tiktok(15.5.6)，仍能完美使用。

## &emsp;&emsp;![tiktok版本](https://raw.githubusercontent.com/ssooenftzero/0X/master/YouTube/icon/tiktok.png)

# -----------------------------------------------------------

# 使用QuantumultX 解锁 TikTok 区域限制

## &emsp;详细步骤

### &emsp;&emsp;第一步，下载脚本配置文件

### &emsp;&emsp;分别复制脚本配置文件链接

#### （NobyDa） https://raw.githubusercontent.com/NobyDa/Script/master/QuantumultX/Js.conf

#### （花姐） https://raw.githubusercontent.com/ConnersHua/Profiles/master/Quantumult/X/Rewrite.conf

### &emsp;&emsp;进入QuantumultX，点击页面右下角三菱按钮，找到Rewrite模块，点击引用，粘贴刚刚复制的链接，右上角点击确定，点击全部同步就可以下载脚本配置文件

### &emsp;&emsp;再次进入QuantumultX，点击页面右下角三菱按钮，找到配置文件-点击编辑-找到[rewrite_local]，并在下方粘贴以下代码；

```python
(?<=(carrier|sys)_region=)CN url 307 JP
(?<=version_code=)\d{1,}.\d{1}\.\d{1} url 307 14.0.0
```

## 美区为14.0.0，港区则将代码14.0.0改为8.4.0即可

### &emsp;&emsp;复制api*.tiktokv.com, api*.musical.ly, api*.amemv.com, aweme*.snssdk.com，

### &emsp;&emsp;进入QuantumultX，点击页面右下角三菱按钮，找到配置文件模块，点击编辑，滑至页面末尾；

### &emsp;&emsp;（注意：在Rewrite模块引用的远程脚本配置文件js.con中包含了此项，所以这一步可以省略，大致明白原理即可）

### &emsp;&emsp;找到[mitm]，在 hostname 后面粘贴，粘贴后效果大致如下：

```
hostname = api*.tiktokv.com, api*.musical.ly, api*.amemv.com, aweme*.snssdk.com
```

# 注意， ;hostname 前面的; 符号（注释符号），如果有这个符号，务必删掉；这一步其实跟Shadowrocket/Surge配置证书步骤等是一模一样的；在配置文件模块-编辑-下可以看到你所有配置的文本配置（即以文本样式进行配置），包括你的节点订阅，分流规则等等；

# -----------------------------------------------------------

# 生成证书

### &emsp;&emsp;1.进入QuantumultX，点击页面右下角三菱按钮，找到MinM模块，点击生成证书，提示生成成功，点击安装证书此时会跳转至 Safari，提示此网站...下载一个配置描述文件。您要允许吗？，点击允许，网页提示已下载描述文件；

### &emsp;&emsp;2.进入 iOS 系统设置- 通用-描述文件-已下载的描述文件-选中，并安装，输入密码...完成描述文件安装；

### &emsp;&emsp;3.进入 iOS 系统设置- 通用-关于本机-证书信任设置-针对根证书启用完全信任-选中刚刚安装的并启用即可；

# -----------------------------------------------------------

# 享用Tiktok

## &emsp;&emsp;1.进入QuantumultX，点击页面右下角三菱按钮

## &emsp;&emsp;2.开启 Rewrite & MinM ；

# -----------------------------------------------------------
 
# QuantumultX Tiktok 换区操作

# 如想切换到其他地区，进入QuantumultX，点击页面右下角三菱按钮，找到Rewrite模块，点击添加，复制

```
(?<=(carrier|account|sys)_region=)CN url 307 JP
将JP修改成其他地区英文缩写即可，其他国家或地区代码。
```


