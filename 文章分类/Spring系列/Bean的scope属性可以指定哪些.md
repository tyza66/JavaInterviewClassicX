# Bean的scope属性可以指定哪些
- singleton：单例模式，整个应用中只有一个唯一的可以被复用的实例（就是多次获得这个bean的时候拿到的是同一个引用）
- prototype：原型模式，每次请求都会创建一个新的bean（就是每次拿这样定义的bean的时候会获得一个新的实例，就是不同的引用）
- request：每次HTTP请求都会创建一个新的实例
- session：每次HTTP会话都会创建一个新的实例
- golbal-session：全局HTTP会话，仅适用于portlet的web应用