# LinkedHashSet的使用及其方法
---
---


![在这里插入图片描述](https://img-blog.csdnimg.cn/f4830e48375640d9b863df2dc3cc1f0c.png?x-oss-process=image/watermark,type_ZHJvaWRzYW5zZmFsbGJhY2s,shadow_50,text_Q1NETiBATkpVU1RaSkM=,size_20,color_FFFFFF,t_70,g_se,x_16)


##### 第3点怎么理解？
即插入元素的顺序和取出元素的顺序是一致的。即先按照hash值来得到索引位置。然后插入到双向链表中。若equals方法后相等，则不添加。

- 底层结构是数组+双向链表。
![在这里插入图片描述](https://img-blog.csdnimg.cn/29b0c0a559ce470cb9c15afaded5c99e.png?x-oss-process=image/watermark,type_ZHJvaWRzYW5zZmFsbGJhY2s,shadow_50,text_Q1NETiBATkpVU1RaSkM=,size_20,color_FFFFFF,t_70,g_se,x_16)
- 例子图
![在这里插入图片描述](https://img-blog.csdnimg.cn/4e57864d93bd446d9422d8572ed57132.png?x-oss-process=image/watermark,type_ZHJvaWRzYW5zZmFsbGJhY2s,shadow_50,text_Q1NETiBATkpVU1RaSkM=,size_20,color_FFFFFF,t_70,g_se,x_16)

