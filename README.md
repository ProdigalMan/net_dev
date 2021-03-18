# 记录下Linux内核网络驱动相关的知识



## architecture(框架)

![image](https://github.com/ProdigalMan/net_dev/blob/main/img/net_architecture.png)

1. **协议接口层** 向网络协议栈提供统一的数据包发送接口,上层任何形式的协议都可以通过dev_queue_xmit()发送,通过netif_rx()接收,都使用skb_buff作为数据的载体. 

