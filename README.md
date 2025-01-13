# Openledger脚本
Openledger Bot 是一个简单的工具，旨在自动化节点交互。

## 功能
- **自动化节点交互**
- **代理支持**

## 环境要求
- Python3.11及以上

## 安装

1. 将仓库克隆到本地机器：
   ```bash
   git clone https://github.com/Vantone/openledger.git
   ```
2. 进入项目目录：
   ```bash
   cd openledger
   ```
3. 安装必要的依赖：
   ```bash
   pip install -r requirements.txt
   ```

## 使用方法

1. 在运行脚本之前，设置 `wallets.txt` 和 `proxy.txt`（可选是否使用代理）。


   - 首先注册账户，您可以 [点击这里注册](https://testnet.openledger.xyz/?referral_code=djoqykghxi)
   - 下载 [扩展程序](https://chromewebstore.google.com/detail/teneo-community-node/emcclcoaglgcpoognfiggmhnhgabppkm)


3. 如果您想使用代理，请修改 `proxy.txt` 文件，格式如下：
   ```
   username:password@ip:port
   ```

4. 运行脚本：
   ```bash
   python main.py或者python3 main.py
   ```

##  docker 启动方式
```
docker pull python:3.11-alpine3.21
docker run -itd  --restart always  --name openledger  -v /root/openledger:/root/openledger  -w /root/openledger   python:3.11-alpine3.21  sh -c 'pip install -r requirements.txt && python main.py '
```

## PS:不要删除 `data.json`！
