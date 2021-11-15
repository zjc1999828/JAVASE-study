# 获取Class类对象的方式
---
---
![在这里插入图片描述](https://img-blog.csdnimg.cn/6115ced38b35404a9178eb9e0014f84f.png?x-oss-process=image/watermark,type_ZHJvaWRzYW5zZmFsbGJhY2s,shadow_50,text_Q1NETiBATkpVU1RaSkM=,size_20,color_FFFFFF,t_70,g_se,x_16)

```java
        String allPath = "FirstZjc.cat";
        Class cls1 = Class.forName(allPath);
```
![在这里插入图片描述](https://img-blog.csdnimg.cn/b430f40cbec54d22999017530694c25a.png)
多用于参数传递的例子：
![在这里插入图片描述](https://img-blog.csdnimg.cn/fe9f62f5fd844083b12396fc694fb539.png?x-oss-process=image/watermark,type_ZHJvaWRzYW5zZmFsbGJhY2s,shadow_50,text_Q1NETiBATkpVU1RaSkM=,size_20,color_FFFFFF,t_70,g_se,x_16)



```java
        Class cls4 = cat.class;
        System.out.println(cls4);
```
![在这里插入图片描述](https://img-blog.csdnimg.cn/b1bb24c46df54a34a7d980fdb41b1979.png?x-oss-process=image/watermark,type_ZHJvaWRzYW5zZmFsbGJhY2s,shadow_50,text_Q1NETiBATkpVU1RaSkM=,size_20,color_FFFFFF,t_70,g_se,x_16)
前提一定是已经有了某个类的对象实例！！

```java
 cat c = new cat();
        Class cls2 = c.getClass();
```


类加载器的方式来获取类对象
![在这里插入图片描述](https://img-blog.csdnimg.cn/771f8e4bcf89496fae2f448aaf4952f0.png)
前提也是一点要有一个类的对象实例。不然无法调用getClass（）方法

```java
cat shili = new cat();
        ClassLoader cl =shili .getClass().getClassLoader();
        Class cls3 = cl.loadClass(allP
```


![在这里插入图片描述](https://img-blog.csdnimg.cn/5fb826de27d647b9a98e09d489b1e007.png?x-oss-process=image/watermark,type_ZHJvaWRzYW5zZmFsbGJhY2s,shadow_50,text_Q1NETiBATkpVU1RaSkM=,size_20,color_FFFFFF,t_70,g_se,x_16)

```java
        Class<Integer> integerClass = int.class;
        Class<Boolean> booleanClass = boolean.class;
        Class<Integer> integerClass1 = Integer.class;
        Class<Boolean> type = Boolean.TYPE;
```

