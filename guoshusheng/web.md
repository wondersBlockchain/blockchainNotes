https://www.bilibili.com/video/av21012197

orderer多少取决于 共识算法 
如果是solo就是一个 
如果是kafka就是4个

----------------------------------------
### 典型交易流程
 * 创建交易提案并发送给背书节点
 * 背书节点模拟交易并生产背书签名
 * 收集交易的背书
 * 构造交易请求并发送给排序服务节点
 * 排序服务节点对交易进行排序并生成区块
 * 排序服务节点以广播给组织的主节点
 * 记账节点验证区块内容并写入区块
   > 1. 交易数据的验证
   > 2. 记账节点与VSCC
   > 3. 基于状态数据的验证和MVCC检查
   > 4. 无效交易的处理
 * 在组织内部同步最新的区块
