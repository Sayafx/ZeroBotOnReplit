# 由于 2024年1月1日 replit 更改政策，此方案已过时。

replit中创建bash语言

在console里粘贴

```
git clone https://github.com/Sayafx/ZeroBotOnReplit.git && mv -b ZeroBotOnReplit/* ./ && mv -b ZeroBotOnReplit/.[^.]* ./ && rm -rf *~ && rm -rf ZeroBotOnReplit
```

回车

在console里输入

```
sh install.sh
```

回车等待输出完毕

修改`main.sh`，`./gocqzbp` bot的名字 主人qq号

```
chmod +x ./gocqzbp
./gocqzbp Sagiri 1145140721
```



点击绿色run按钮



耐心等待，如网络报错后再重试即可。

出现下面的情况无反应时，点击stop再run重启

```
 bash main.sh
INFO[0000] [web] 本机不支持ipv6                              
INFO[0000] [file]加载md5数据库...                            
INFO[0001] [file]md5数据库已是最新                             

======================[ZeroBot-Plugin]======================
* OneBot + ZeroBot + Golang
* Version v1.6.1-beta3 - 2022-12-26 13:45:09 +0800 CST
* Copyright © 2020 - 2022 FloatTech. All Rights Reserved.
* Project: https://github.com/FloatTech/ZeroBot-Plugin
----------------------[ZeroBot-公告栏]----------------------
        QQ群:1048452984, 2群:915103207
        开发群:752669987, 进阶开发群:705749886

            禁止用于违法用途
============================================================

未找到配置文件，正在为您生成配置文件中！
请选择你需要的通信方式:
> 0: HTTP通信
> 1: 云函数服务
> 2: 正向 Websocket 通信
> 3: 反向 Websocket 通信
请输入你需要的编号(0-9)，可输入多个，同一编号也可输入多个(如: 233)
您的选择是:INFO
[0008] [thesaurus]加载 116 条kimoi                     
INFO
[0008] [thesaurus]加载 4775 条傲娇词库 12209 条可爱词库         


```

这时候就可以输入选择了，选择http通信，编辑`config.yml`配置文件之后重启。（一定要先stop再编辑，否则将无法保存配置文件）

只填写账号密码即可，如下

```
# go-cqhttp 默认配置文件

account: # 账号相关
  uin: 1919810 # QQ账号
  password: '1919810' # 密码为空时使用扫码登录
  encrypt: false  # 是否开启密码加密
  status: 0      # 在线状态 请参考 https://docs.go-cqhttp.org/guide/config.html#在线状态
  relogin: # 重连设置
    delay: 3   # 首次重连延迟, 单位秒
    interval: 3   # 重连间隔
    max-times: 0  # 最大重连次数, 0为无限制

  # 是否使用服务器下发的新地址进行重连
  # 注意, 此设置可能导致在海外服务器上连接情况更差
  use-sso-address: true
  # 是否允许发送临时会话消息
  allow-temp-session: false
```

点击Run运行

```
[2023-01-06 15:11:23] [INFO]: 子进程已启动, pid: 2861 
[2023-01-06 15:11:23] [INFO]: 当前版本:(devel) 
[2023-01-06 15:11:23] [WARNING]: 虚拟设备信息不存在, 将自动生成随机设备. 
[2023-01-06 15:11:23] [INFO]: 已生成设备信息并保存到 device.json 文件. 
[2023-01-06 15:11:23] [INFO]: Bot将在5秒后登录并开始信息处理, 按 Ctrl+C 取消. 
[2023-01-06 15:11:26] [INFO]: [thesaurus]加载 116 条kimoi 
[2023-01-06 15:11:26] [INFO]: [thesaurus]加载 4775 条傲娇词库 12209 条可爱词库 
[2023-01-06 15:11:28] [INFO]: [thesaurus]加载 116 条kimoi 
[2023-01-06 15:11:28] [INFO]: [thesaurus]加载 4775 条傲娇词库 12209 条可爱词库 
[2023-01-06 15:11:28] [INFO]: 开始尝试登录并同步消息... 
[2023-01-06 15:11:28] [INFO]: 使用协议: iPad 
[2023-01-06 15:11:32] [INFO]: Protocol -> connect to server: xx.xxx.xxx.xx:8080 
[2023-01-06 15:11:33] [WARNING]: 登录需要滑条验证码, 请选择验证方式:  
[2023-01-06 15:11:33] [WARNING]: 1. 使用浏览器抓取滑条并登录 
[2023-01-06 15:11:33] [WARNING]: 2. 使用手机QQ扫码验证 (需要手Q和gocq在同一网络下). 
[2023-01-06 15:11:33] [WARNING]: 请输入(1 - 2)： 

```

输入1，回车

```
[2023-01-06 15:11:33] [WARNING]: 登录需要滑条验证码, 请选择验证方式:  
[2023-01-06 15:11:33] [WARNING]: 1. 使用浏览器抓取滑条并登录 
[2023-01-06 15:11:33] [WARNING]: 2. 使用手机QQ扫码验证 (需要手Q和gocq在同一网络下). 
[2023-01-06 15:11:33] [WARNING]: 请输入(1 - 2)： 
1
[2023-01-06 15:12:28] [WARNING]: 请前往该地址验证 -> https://captcha.go-cqhttp.org/captcha?id=cxxxxxx&style=simple&aid=16&uin=xxxxxxxxxxxxxxxx&sid=xxxxxxxxxxxxxx&cap_cd=bb535N6jNy3kDlsyrBdkxxxxxxxxxxxxxxxxxmlrewDdA**&clientype=1&apptype=2 <- 或输入手动抓取的 ticket：（Enter 提交） 
```

对链接点右键，通过滑块验证，之后会显示未验证，对新出现的链接验证，手机扫码授权

```
[2023-01-06 15:13:36] [WARNING]: 账号已开启设备锁，请选择验证方式: 
[2023-01-06 15:13:36] [WARNING]: 1. 向手机 152*******1 发送短信验证码 
[2023-01-06 15:13:36] [WARNING]: 2. 使用手机QQ扫码验证. 
[2023-01-06 15:13:36] [WARNING]: 请输入(1 - 2) (将在10秒后自动选择2)： 
[2023-01-06 15:13:46] [WARNING]: 账号已开启设备锁，请前往 -> https://accounts.qq.com/safe/verify?_wv=2&_wwv=128&envfrom=double-check&uin=1264223554&sig=W3du6RZ5EeQPs05uPxxxxxxxxxxxxxxxxxxxxxNNwPXTAuZ3igL7guZ5mqnxTBemWYkkIiXQRXcCHN4jjaQaMsF8E00A%3D <- 验证后重启Bot. 
```

扫码之后再次通过滑块验证，登录成功

```
[2023-01-06 15:16:01] [INFO]: 登录成功 欢迎使用: Sagiri 
[2023-01-06 15:16:01] [INFO]: 开始加载好友列表... 
[2023-01-06 15:16:01] [INFO]: 共加载 3 个好友. 
[2023-01-06 15:16:01] [INFO]: 开始加载群列表... 
[2023-01-06 15:16:02] [INFO]: 共加载 6 个群. 
[2023-01-06 15:16:02] [INFO]: 资源初始化完成, 开始处理信息. 
[2023-01-06 15:16:02] [INFO]: アトリは、高性能ですから! 
[2023-01-06 15:16:02] [INFO]: 正在检查更新. 
[2023-01-06 15:16:02] [WARNING]: 检查更新失败: 使用的 Actions 测试版或自编译版本. 
[2023-01-06 15:16:02] [INFO]: 开始诊断网络情况 
[2023-01-06 15:16:02] [INFO]: CQ HTTP 服务器已启动: [::]:5700 
[2023-01-06 15:16:02] [INFO]: 连接funcall对端成功 
[2023-01-06 15:16:02] [INFO]: CQ funcall 服务器 zbp 已启动 
[2023-01-06 15:16:03] [INFO]: [job]本地环回初始化完成 
[2023-01-06 15:16:10] [INFO]: 网络诊断完成. 未发现问题 
```

在QQ群中发送`/响应`，bot即可运行

最后一步，我们需要在网络监控中添加上方的网址，比如我的网址，以防止replit休眠

```
https://bottest.sayafx.repl.co
```

[网络监控](https://uptimerobot.com/)

