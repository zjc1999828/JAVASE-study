# Object-equals方法及其在子类中的重写
---
---

**== 运算符**用于基本数据类型，判断的是值是否相等
                       用于引用数据类型（对象），判断的是两者的地址是否相等，即判断两者是否是同一个对象。


---
---

equals方法。
如果在子类中不重写，则默认使用object类中的equals方法，即判断两个对象是否是同一个对象。
如果在子类中重写了，则使用的是子类中重写的equals方法。
![在这里插入图片描述](https://img-blog.csdnimg.cn/d16070b6d2ae4304bdcd31e2173d11f0.png?x-oss-process=image/watermark,type_ZHJvaWRzYW5zZmFsbGJhY2s,shadow_50,text_Q1NETiBATkpVU1RaSkM=,size_20,color_FFFFFF,t_70,g_se,x_16)

