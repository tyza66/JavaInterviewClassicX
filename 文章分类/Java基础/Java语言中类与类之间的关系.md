# Java语言中类与类之间的关系
- 类与类之间有这五种关系：继承、实现、并联、聚合、依赖
- 继承：一个类可以从另一个类继承属性和方法，继承的类被称为子类或派生类
- 实现：一个类可以实现多个接口，成为接口的实现类，每个接口中都可以定义一组自己的方法
- 并联：一个类可以包含另一个类实例化的对象作为成员变量或方法参数，这种关系可以通过类之间的链接来建立
- 聚合：一个类可以包含另一个类实例化的对象作为成员变量或方法参数，但是这种关系是暂时的，当聚合的对象销毁的时候聚合的对象也会被销毁
- 依赖：一个类使用另一个类实例化的对象作为方法的参数或返回值，这种关系是一种临时性的关系，随着使用的结束而结束