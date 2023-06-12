# ArrayList和LinkedList的区别
- 他们在底层的数据结构不同，ArrayList底层是由数组实现的，LinkedList底层是由链表实现的。
- 他们由于底层实现不同，所以在不同的应用场景下，他们的性能表现也不同。ArrayList更适合随即查找，LinkedList更适合插入和删除。
- 他们之间添加、查询、删除的时间复杂度不相同
- List都是线程不安全的
- ArrayList和LinkedList都实现了List接口，但是LinkedList还实现了Deque接口，所以LinkedList还可以当做队列和栈来使用