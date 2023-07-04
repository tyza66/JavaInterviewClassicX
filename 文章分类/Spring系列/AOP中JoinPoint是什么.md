# AOP中JoinPoint是什么
- JoinPoint是一个程序执行点，表示被拦截的方法或代码片段的特定位置
- JoinPoint可以是一方法调用、字段访问、构造函数的调用、异常处理等程序的执行点
- 在AOP框架中，JoinPoint通常由一个JoinPoint对象表示，JoinPoint对象包含了拦截到的执行点的相关信息（返回值、方法名、类名等）