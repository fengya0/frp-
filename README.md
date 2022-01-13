# fro改造
主要修改以下功能点
* 流量认证特征
* 修改默认盐值salt
* 非TLS特征明显
* frp建立TLS连接的第一个字节是0x17
* frp版本信息
* Frp字符串特征
* 客户端的留存配置文件


frpc的运行参数，-a指定frps的地址，-p指定端口。默认开启tls支持
![2022-01-13 at 23 04](https://user-images.githubusercontent.com/97685204/149355083-6ea4e3b6-eac8-4be4-b21e-33016ac20661.png)

frps.ini需要配置以下参数
[common]
bind_port = 7000
token = 1q2w3e!@#
kcp_bind_port = 7000
tls_enable = true
