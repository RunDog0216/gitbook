# 线程池的参数

## 1、核心参数

1. corePoolSize：核心池的大小。在创建了线程池之后，默认情况下，线程池中没有任何线程，而是等待有任务来才创建线程去执行任务，除非调用了preStartAllCoreThreads\(\)或者presentCoreThread\(\)方法来预创建核心线程。默认情况下，创建了线程池后，线程池中的线程数为0，当任务来之后，就会创建一个线程去执行任务。当线程池中的线程数目达到corePoolSize后，就会把任务放到缓存队列中。
2. maximumPoolSize：线程池最大线程数，这是一个非常重要的参数，表示在线程池中最多能创建多少个线程，最大线程数&gt;线程数&gt;核心线程数的线程会被自动释放掉。而小于corePoolSize的不会。
3. keepAliveTime：表示线程没有任务执行时最多保持多久时间时间会终止。默认情况下，只有当线程池中的线程数大于corePoolSize是，keepAliveTime才会起到作用，知道线程池的线程数不大于corePoolSize。如果调用了allowCoreThreadTimeOut\(boolean\)方法，在线程池中的线程数不大于核心线程数时，keepAllowTime参数也会起作用，知道线程池中的线程数为0。
4. TimeUnit：keepAllowTime的时间单位。
5. BlockingQueue：一个阻塞队列。用来存储等待执行的任务。ArrayBlockingQueue、LinkedBlockingQueue、SynchronousQueue
6. RejectedExecutionHandler：拒绝处理任务策略，也可以是自定义的。

```text
SynchronousQueue是无界的，是一种无缓冲的等待队列，但是由于该Queue本身的特性，在某次添加元素后必须等待其他线程取走后才能继续添加；可以认为SynchronousQueue是一个缓存值为1的阻塞队列，但是 isEmpty()方法永远返回是true，remainingCapacity() 方法永远返回是0，remove()和removeAll() 方法永远返回是false，iterator()方法永远返回空，peek()方法永远返回null。
LinkedBlockingQueue是无界的，是一个无界缓存的等待队列。
ArrayListBlockingQueue是有界的，是一个有界缓存的等待队列。
```



