# STW是什么
- STW是Stop The World的缩写，实在垃圾回收算法执行的过程中，需要将JVM内存冻结的一种状态。
- 在这种状态下，除了GC进程和native方法以外的所有线程都是停止执行的
- 但是执行的native方法不能与JVM交互
- GC各种算法优化的重点就是减少STW
- 减少STW也是JVM调优的重点