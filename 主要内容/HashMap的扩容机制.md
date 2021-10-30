# HashMap底层源码机制
---
---
![在这里插入图片描述](https://img-blog.csdnimg.cn/4b18041cec2a4448936bce861f4bcb94.png?x-oss-process=image/watermark,type_ZHJvaWRzYW5zZmFsbGJhY2s,shadow_50,text_Q1NETiBATkpVU1RaSkM=,size_20,color_FFFFFF,t_70,g_se,x_16)
一开始定义了加载因子==loadfactor 为0.75==，且数组里面是空的，该数组类型为==HashMap$Node[ ]==。在添加第一个对象的时候，会通过resize（）方法初始化数组的容量为16.此时的阈值threshold为==0.75*16 == 12== 。每次添加完Node都会判断是否超过阈值，若超过阈值，则通过resize（）进行数组扩容（变为原来的2倍），且threshold 也变为原来的两倍。






6. 注解：
链表和红黑树是可以同时存在的，即一条链是链表，另外一条链变为红黑树。
