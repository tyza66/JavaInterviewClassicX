# Spring中的Bean的生命周期有哪些步骤
- 推断构造方法
- 实例化
- 填充属性，也就是依赖注入
- 处理Aware回调
- 初始化前，处理@PostConstruct注解
- 初始化，处理InitializingBean接口
- 初始化之后，进行AOP