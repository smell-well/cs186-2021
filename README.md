### 实现B+树索引

#### 难点
1. 每次在内存中处理好page后，需要刷盘到sync
2. B+树的插入过程中所有子树的维护
3. 实现遍历树的接口，需要控制与硬盘IO的次数
4. 实现快速初始化的批量装载接口

### 实现join和查询优化

#### join
1. 基于 Page 和 Block 的循环遍历实现连接
2. 递归的分区实现哈希连接
3. 归并排序的连接

#### 查询优化
1. 实现单表查询的耗时估计
2. 多表连接的动态规划方法优化
3. 实现执行计划的查询

### 多粒度的锁控制
1. 读锁、写锁、意向锁等锁之间的兼容和升级关系
2. 锁管理器实现锁的请求、释放等操作
3. 锁上下文实现锁与实际控制对象的绑定
4. 实现两阶段锁的控制

### 恢复机制
1. 前向过程，对常见的增删改查添加相应的日志更新和checkpoint日志
2. 重启过程，重建事务状态表和脏页表
3. redo命令执行相应的redo操作
4. undo通过一些条件判断是否需要进行撤销
