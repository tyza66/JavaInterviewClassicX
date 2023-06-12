# HashMap和HashTable之间的不同
- HashMap方法没有syncronized修饰，线程不安全，HashTable方法有syncronized修饰，线程安全
- HashMap允许Key和Value的值为null，而HashTable不允许
- 他们底层使用数组+链表来实现
- 在JDK8开始，链表高度到8，数组长度达到64的时候，链表会转换为红黑树，内部元素就以节点的形式存在