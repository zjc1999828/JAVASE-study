# Hashtable的扩容机制
---
---

一开始数组初始为11个。
threshold为7个。

当元素个数大于等于threshold的时候开始扩容。

后面扩容是 (oldcapacity *2 +1)
![在这里插入图片描述](https://img-blog.csdnimg.cn/f5459cb205e247d79683780d00e37b9e.png?x-oss-process=image/watermark,type_ZHJvaWRzYW5zZmFsbGJhY2s,shadow_50,text_Q1NETiBATkpVU1RaSkM=,size_20,color_FFFFFF,t_70,g_se,x_16)
 
