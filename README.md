# 实验名称
Bitcoin parse tx

# 实验简介
自行书写脚本发送tx到某一个区块链浏览器上，并解析tx数据

# 实验完成人
权周雨 

学号：202000460021 

git账户名称：baekhunee

# 代码说明
```
from requests_html import HTMLSession

#创建Session对象
session = HTMLSession()

#某区块浏览器的链接
url = 'https://api.blockcypher.com/v1/btc/test3/addrs/miAMpCdoM3SuRMRoEVHp8smFdDAz29WA9g'

#GET请求访问指定的url
response = session.get(url)

with open("parse result.txt","w") as f:
    f.write(response.html.full_text)
```

导入requests_html库后创建session对象，指定url，实际中存在很多类似的区块浏览器，任选其一即可。接下来调用GET请求访问指定的url，并将收到的响应信息写入"parse result.txt"文件即可。

# 运行截图
![image](https://user-images.githubusercontent.com/105578152/181005767-29b4523e-4938-4a70-a9b8-41a05f296b11.png)
仓库中也已放入parse result.txt文件
