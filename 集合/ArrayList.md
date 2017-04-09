# ArrayList  
ArrayList 是日常中使用最多一个集合，内部通过数组实现。  
**ArrayList 是线程不安全的。** 如果多个线程同时访问，会出现不可预料的错误，此时必须保持同步，可以使用如下方法创建： `List list = Collections.synchronizedList(new ArrayList(...));`，或者使用 `Vector`。

ArrayList中有两个变量，一个是存储元素的数组（ Object[] elementData ），另一个是ArrayList的大小（int size ）。数组可以存储null元素，而 `size <= elementData.length()`,size的实际意义是已经存入ArrayList的元素的个数。

构造函数
---
* `ArrayList()`  
  空的elementDatea，size = 0
* `ArrayList(int initialCapacity)`    
  传入一个初始容量，会new一个Object数组赋给elementData,数组的大小为initialCapacity，size=0
* `ArrayList(Collection<? extends E> c)`  
  传入一个集合  

方法
---
  添加元素共有四个  



疑问
---
1. Arrays.copyOf() 为什么是浅复制  
1. 检查是否超出索引的时候有两个方法，rangeCheck(int index) 和 rangeCheckForAdd(int index),为什么前者不检查 index < 0 的情况
