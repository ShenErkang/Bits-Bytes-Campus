### **第一章：计算机网络基础概述**

**🌐 从比特流动到全球互联：网络的基石解析**

------

#### 1. 互联网基础概念

**📌 核心定义**

> **互联网本质** ：
> *“网络之网络（Network of Networks）”* , 通过协议（TCP/IP等）与RFC标准实现异构网络互连。
>
> **关键协议举例** ：
> `HTTP`（应用层）、`TCP`（传输层）、`IP`（网络层）、`Ethernet`（链路层） 

**💻 互动测试题**
**Q1** ：下列哪些设备属于互联网的“边缘部分”？

A) 家庭路由器

B) 智能手机

C) 数据中心服务器

D) 核心路由器

答案：B、C ✅（解析：边缘设备指主机，核心路由器属于核心部分）

------

#### 2. 互联网的组成

**🔵 架构可视化**

边缘设备 → 接入网 → 核心路由器网络 → 全球互联

**📊 C/S与P2P对比**

| **模式**    | **通信方向**  | **典型场景**     |
| ----------- | ------------- | ---------------- |
| 客户-服务器 | 单向请求/响应 | 网页浏览、云存储 |
| 对等连接    | 双向平等交互  | 文件共享、区块链 |

**🛠 分组交换案例**
假设发送报文长度：`5000字节`，MTU：`1500字节`
分片计算：

- 首部长度：`20字节`
- 数据分片数：`5000 / (1500-20) ≈ 4片`
  分片结果：`4个分组（每片数据1480字节）`

------

#### 3. 性能与非性能指标

**📊 性能指标速查表**

| **指标**   | **公式/定义**                    | **示例值** |
| ---------- | -------------------------------- | ---------- |
| 带宽       | 通道最大传输能力                 | `100 Mbps` |
| 时延（总） | 发送+传播+处理+排队时延          | `50 ms`    |
| RTT        | 发送时延 + 2×传播时延 + 处理时延 | `120 ms`   |

**⚖ 非性能权衡案例**
某企业选择网络方案时需考虑：

- **费用** ：￥10万/年 vs ￥15万/年
- **可扩展性** ：支持未来5年设备扩容 ✅
- **标准化** ：符合IEEE协议 ✅

------

#### 4. 分层模型

**🛠 五层协议类比**

> **航空旅行五步骤** ： 
>
> 1. **物理层** → 跑道起飞（比特传输）
> 2. **链路层** → 机舱间通信（相邻节点帧传递）
> 3. **网络层** → 航线规划（全局路由）
> 4. **传输层** → 乘客座位分配（进程间数据传输）
> 5. **应用层** → 机上服务（具体应用）

**🔗 PDU封装流程**

应用层数据 → 传输层（TCP头） → 网络层（IP头） → 链路层（MAC帧） → 物理层比特流

**💻 分层模型测试题**
**Q2** ：OSI模型中表示层的作用是？

A) 数据加密

B) 数据格式转换

C) 会话管理

答案：B ✅
