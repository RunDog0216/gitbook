# 任务拒绝策略

## 1、RejectedExecutionHandler

1. AbortPolicy：直接抛出异常
2. CallerRunsPolicy：只用调用者所在线程来运行任务
3. DiscardOldestPolicy：丢弃队列里最近一个任务，并执行当前任务
4. DiscardPolicy：不处理，不丢弃





