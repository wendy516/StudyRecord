### Handler 底层原理

定义： 

>

**什么是handler?**



**线程间如何通讯的呢？**

​	Handler通讯实现的方案实际上是**内存共享**的方案。

**为什么线程不会干扰？**

​	内存管理设计优秀。

**为什么wait/notify用武之地不大？**

​	因为handler已经将我们需要的功能进行了Linux层的封装。





#### 学习记录

1. lancher(app) ：zygote -> jvm ->**ActivityThread**.main
2. 



