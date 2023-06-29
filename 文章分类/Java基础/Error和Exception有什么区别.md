# Error和Exception有什么区别
- Error和Exception都是继承Throwable类的子类
- Error表示不是不可能大但是很困难的严重问题，比如内存溢出等问题，不能指望程序能处理这样的情况
- Exception表示一种设计或实现问题，可以被程序本身处理，比如空指针，网络连接中断等问题