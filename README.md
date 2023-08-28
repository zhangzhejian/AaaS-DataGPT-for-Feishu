# Feishu DataGPT(Code Interpreter)

这是一个将[Code Interpreter](https://github.com/shroominic/codeinterpreter-api)接入飞书的尝试。在demo中，后端执行python的Codebox容器使用的是未开源的[Codebox](https://github.com/shroominic/codebox-api/tree/main)。 后续自研的Codebox也将更新后同步。
## Demo 
支持与飞书中文档的交互（需要确保机器人有权限）。同时也支持上传文档、文件的交互。
### 与云文档交互
![](imgs/feishu_file.gif)

### 使用python画图
![](imgs/plot.gif)

## 使用Docker部署服务端 

### 配置环境变量

### docker启动
```
docker-compose -f docker_dev.yml build
docker-compose -f docker_dev.yml up
```

## 部署飞书机器人及接口
1. 使用[飞书开放平台](https://open.feishu.cn/app/)，创建企业自建应用
2. 添加应用能力：机器人
3. 权限管理中，开通“消息与群组”和“云文档”中的所有权限
4. 事件订阅中填写请求地址配置。添加事件：接收消息im.message.receive_v1
5. 发布版本后在飞书中搜索使用

APP相关信息：
![app信息凭证](imgs/app_info.png)

增加清空会话按钮
![事件订阅](imgs/events.png)
![button](imgs/renew_session_btn.png)

## 快速试用
免费试用api，可以填充到事件订阅地址中。
url：
```
http://aaas.world:5004/feishu_robot_webhook_trial?openai_api_key=YOUR_OPENAI_API_KEY&app_id=YOUR_FEISHU_APP_ID&app_secret=YOUR_FEISHU_APP_SECRET
```


## 联系方式
微信:zjajzzj1996
Email: [zhangzhehian@gmail.com](zhangzhehian@gmail.com)
