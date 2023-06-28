# short s1 = 1; s1 = s1 + 1;有什么错
- 当short、byte、char三种类型进行运算时，会自动转换为int类型
- 而s1定义支出就是short类型，分配了固定的内存空间，不会因此发生改变
- 计算结果为int类型，再赋值给short类型的s1就会报错