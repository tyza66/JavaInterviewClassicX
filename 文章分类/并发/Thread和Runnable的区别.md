# Thread和Runable的区别
- Thread和Runnable实质上是继承关系，没有可比性。无论使用Runnable还是Thread，都得实现run()方法，new Thread。用法上，如果没有复杂的线程操作需求，那就选择继承Thread，如果只是简单的执行一个任务，那就实现runnable