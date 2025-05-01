# Discord 自动聊天 2.0 介绍
为什么要写Discord 自动聊天脚本呢？撸毛人最痛苦的就是领水和dc聊天获取OG角色，于是Discord 自动聊天和Discord 自动领水脚本就诞生了！

# Discord 自动聊天 2.0 使用教程
## 1、抓取token
安装chrome插件：https://chromewebstore.google.com/detail/discord-get-user-token/accgjfooejbpdchkfpngkjjdekkcbnfd

打开dc页面：https://discord.com/channels/@me

点击插件的``Get token``就获取了

![image](https://github.com/user-attachments/assets/25f49dfc-80c9-4bf8-847c-0648dd81d3d3)

## 2、设置配置文件``setup.json``
```json
{
    "use_ai": true, # true开启ai聊天，根据最后一个聊天记录自动回复，fals关闭ai聊天，启用messages.txt，通常拿来自动领水用
    "api_key": "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", # 这个是ai的key，dandan这里使用的是免费的。
    "default_text_file": "config/messages.txt", #这个是自定义聊天的文本位置
    "conversation_interval_seconds": 10 #这里是间隔时间
}
```

## 3、设置代理池``proxy_config.json``（没有代理池的可以跳过）
```json
{
    "ip": "192.168.2.7", #代理池ip
    "port_range": {
        "start": 50000, #开始端口
        "end": 50100 #结束端口
    },
    "max_ips": 2 #想要抓取多个ip
}
```

## 4、tokens.txt
抓取到的tokens放这里，一行一个

## 5、proxy.txt 
代理一行一个，支持sk5（但是容易出错）

## 6、channels.json是dc频道
例如：https://discord.com/channels/1182177005337325598/1218231474587963514
那么我们只要：1218231474587963514这个数字
```json
{
  "general": "1218231474587963514"
}
```
这样就可以自动聊天了，多个频道怎么做呢？
```json
{
  "general": "1218231474587963514",
  "general": "1218231474587963514",
  "general": "1218231474587963514",
  "general": "1218231474587963514",
  "general": "1218231474587963514"
}
```
记得json格式最后一个不能有逗号，不能有逗号，不能有逗号！


