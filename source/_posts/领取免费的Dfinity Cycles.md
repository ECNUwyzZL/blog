---
title: 领取免费的Dfinity Cycles
---
fleek官方为了推广开发者使用Dfinity来构建应用，(https://fleek.co/) 推出活动所有90天以上的github账户用户都可以通过绑定领取价值100美元的Dfinity cycles代币，该代币可以用作购买Dfinity的计算资源容器，来部署应用。

## 安装Dfinity SDK
环境：科学上网，命令行配置http_proxy
系统偏好设置-网络-高级-代理-SOCKS5代理
![image.png](https://intranetproxy.alipay.com/skylark/lark/0/2021/png/281366/1627371678013-953bc79a-bd93-4eb8-9e27-9611e6b461a2.png#align=left&display=inline&height=282&margin=%5Bobject%20Object%5D&name=image.png&originHeight=564&originWidth=1198&size=349818&status=done&style=none&width=599)
执行
```shell
export http_proxy=socks5h://127.0.0.1:13659
export https_proxy=socks5h://127.0.0.1:13659
```
执行 
```shell
sh -ci "$(curl -fsSL https://sdk.dfinity.org/install.sh)"
```
全程回车确定
```shell
dfx -V
```
看一下是否安装成功，成功后会显示
![image.png](https://intranetproxy.alipay.com/skylark/lark/0/2021/png/281366/1627362169621-7c2922e7-4e0b-4d0d-8ed9-5df7bd977141.png#align=left&display=inline&height=91&margin=%5Bobject%20Object%5D&name=image.png&originHeight=182&originWidth=450&size=37437&status=done&style=none&width=225)
## 生成DFX Principal ID
命令行执行
```shell
dfx identity get-principal
```
![image.png](https://intranetproxy.alipay.com/skylark/lark/0/2021/png/281366/1627362302787-fc3e5899-18be-440d-bf6b-cbe210414c2c.png#align=left&display=inline&height=89&margin=%5Bobject%20Object%5D&name=image.png&originHeight=178&originWidth=1622&size=144154&status=done&style=none&width=811)
复制生成ID
p436z-nnjpp-sbqgw-ggatw-4ozwr-fmekk-zvwko-lg3j7-boxd5-6ltq4-fae
该ID作为后续绑定服务器cycles钱包的设备标识码，在进行项目部署时仅有绑定钱包的机器可部署到公网网络
### 领取服务器Cycles
访问[https://faucet.dfinity.org/](https://faucet.dfinity.org/)
1、输入Principal ID
2、选择Cycles wallet
3、生成新Cycles wallet
![image.png](https://intranetproxy.alipay.com/skylark/lark/0/2021/png/281366/1627362625348-2a48de2e-7e0d-4d0a-86dc-551cb95bd990.png#align=left&display=inline&height=670&margin=%5Bobject%20Object%5D&name=image.png&originHeight=1340&originWidth=1022&size=444881&status=done&style=none&width=511)
最后在Principal ID对应的机器上执行
```shell
dfx identity --network ic set-wallet --force 7we6l-cqaaa-aaaah-aakmq-cai
```
即可完成钱包绑定
## 部署项目
[https://sdk.dfinity.org/docs/quickstart/network-quickstart.html](https://sdk.dfinity.org/docs/quickstart/network-quickstart.html)

