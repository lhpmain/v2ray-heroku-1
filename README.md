## v2ray-heroku
[![](https://www.herokucdn.com/deploy/button.png)](https://heroku.com/deploy?template=https://github.com/lhpmain/v2ray-heroku-1.git)

### heroku上部署v2ray
- [x] 支持vmess和vless两种协议
- [x] 支持自定义websocket路径
- [x] 伪装首页（3D元素周期表）
- [x] HTMl5测速
- [x] 使用v2ray最新版构建

请求`/`，返回3D元素周期表

![image](https://cdn.jsdelivr.net/gh/libsgh/v2ray-heroku@main/doc/1.png)

请求`/speedtest/`，html5-speedtest测速页面

![image](https://cdn.jsdelivr.net/gh/libsgh/v2ray-heroku@main/doc/2.png)

请求`/test/`，文件下载速度测试

![image](https://cdn.jsdelivr.net/gh/libsgh/v2ray-heroku@main/doc/3.png)

请求`/ray`（可配置）v2ray websocket路径


### 环境变量说明

|  名称 | 值  | 说明  |
| ------------ | ------------ | ------------ |
|  APP_NAME |就是你 heroku 项目的名字 |   |
|  EMAIL |heroku 账户的 email |   |
|  HEROKU_API_KEY |heroku API key | 在 account 设置下可以找到  |
|  HEROKU_V2RAY_WS_PATH |路径 | 默认为/ray  |
|  APP_NAME |就是你 heroku 项目的名字 |   |
|  HEROKU_V2RAY_PROTOCOL |  vmess<br>vless（可选） |  协议：nginx+vmess+ws+tls或是nginx+vless+ws+tls |
|  HEROKU_V2RAY_UUID |  [uuid在线生成器](https://www.uuidgenerator.net "uuid在线生成器") | 用户主ID  |

### 进阶
heorku可以绑卡（应用一直在线，不扣费），绑定域名，套cf，[uptimerobot](https://uptimerobot.com/) 定时访问防止休眠