# MySQL中遇到过死锁问题吗，如何解决
- 程序出现死锁，是因为在多线程环境里面两个或两个以上给的线程同时满足条件、请求保持条件、不可抢占条件、循环等待条件
- 出现死锁之后可以通过jstack命令去导出dump日志，然后从dump日志里面定位到具体死锁的程序代码
- 通过修改去破坏者四个条件里面的任意一个，就可以解决死锁的问题
- 注意其中互斥条件是锁本身的特性，不能被破坏