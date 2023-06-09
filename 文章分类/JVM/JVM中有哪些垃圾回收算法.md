# JVM中有哪些垃圾回收算法
- MarkSweep标记清除法：分为两个阶段，标记阶段将垃圾内存标记出来，清除阶段直接将垃圾内存回归。这种算法是比较简单的，但是有个很严重的问题就是会产生内存碎片，导致大对象无法分配到连续的内存空间，从而导致频繁的FullGC，影响系统的性能
- Copying拷贝算法：为了解决MarkSweep算法的内存碎片的问题，就产生了拷贝算法。将内存非为大小相等的两半，每次只使用其中的一半，在垃圾回收的时候，将当前这一块的内存中存活的对象全部拷贝到另一半，然后当前这一半内存就可以清除，这种算法没有内存碎片，但是它的问题就在于浪费空间，而且它的效率跟存货对象的数量有关
- MarkCompack标记压缩算法：为了解决拷贝算法的缺陷，就提出了标记压缩法。这种算法在标记阶段跟标记清除法一样，但是在完成标记后，不直接清理内存，而是将存活的对象往一端移动，然后将端边界以外的多有内存直接清除
- 这三种算法各有利弊，各自有各自的使用场景