# newFixedThreadPool

## 1、newFixedThreadPool的使用

1. 创建一个可重用固定线程数的线程池，以共享的无界队列来运行这些线程。在任意点，在大多数nThreads线程会处于处理任务的活动状态。如果在所有线程处于活动状态时提交附加的任务，则正在由可用线程之前，附加任务都将在队列中等待。如果在关闭前的执行期间由于失败导致任何线程终止，那么一个新的线程将代替它执行后续的任务（如果需要）。在某个线程被显示地关闭之前，池中的线程一直都在。

