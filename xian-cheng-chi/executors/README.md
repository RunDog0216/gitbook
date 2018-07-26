# Executors

## 1、Executors

1. java.util.concurrent.Executors
2. Executors是个线程的工厂类，方便快速创建线程池，也就是一个线程池的工具类。对线程池原理不清楚的时候，配置一个线程池的性能有可能不是最优的。Executors类里面提供了一些静态工厂，生成一些常用的线程池。常见的三种创建方法：

```text
newSingleThreadExecutor：创建一个单线程的线程池
newFixedThreadPool：创建固定大小的线程池
newCachedThreadPool：创建一个可缓存的线程池
```



