# buff-bot

## 项目功能
实现 Steam 第三方市场 [网易 BUFF](https://buff.163.com) 的自动发货。  

## 原理
登录 Steam 并监听交易报价接口，在获得新的报价请求后去 BUFF 方进行检查，如果报价 ID 匹配则接受报价并确认交易。

## 演示
您可以自行测试以下公开机器人，确定包括报价确认速度和对欺诈模拟报价的处理等能满足您的需求。
| 🤖 编号 | 🛒 BUFF 店铺 | 🆔 Steam 64 位 ID | 💱 报价链接 |
| --- | -- | --- | --- |

## 部署与卸载
💡 **注意事项**：  
请确保您部署机器人的网络环境能同时访问 BUFF 和 Steam，网易 UU 作为加速器并不能解决机器人访问 Steam 出错的问题。  
如果不熟悉网络和代理相关那么我推荐您把机器人部署在本地，同时购买腾讯云或者 AWS 的香港/日本服务器安装 SOCKS5 服务端，将代理信息填入 [config.ini](#) 第 [#](#) 行以同时确保能访问两个网站。  
💻 **部署方法**：
1. Docker 部署（推荐）
> Windows 下[安装 Docker](https://www.runoob.com/docker/windows-docker-install.html) 需要将系统升级至专业版以开启虚拟化。
```bash
docker pull ...
docker run buff-bot:v0.1
```  
2. 手动部署
```bash
...
``` 

## 流程图
![buff-bot](https://raw.githubusercontent.com/senjianlu/imgs/master/buff-bot.png)

## 特别鸣谢
- 感谢 [Steam 哨兵计划](https://github.com/Steam-Sentinel-Project)
