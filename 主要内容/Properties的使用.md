# Properties的使用
----
----

Properties的父类是HashTable，所以其底层是HashMap
![在这里插入图片描述](https://img-blog.csdnimg.cn/f750f189a3484587b701f66ac403af92.png?x-oss-process=image/watermark,type_ZHJvaWRzYW5zZmFsbGJhY2s,shadow_50,text_Q1NETiBATkpVU1RaSkM=,size_20,color_FFFFFF,t_70,g_se,x_16)
对于setProperty方法
若没有这个key，则创建。
若有这个key，则是修改替换。


```java
    @Test
    public void out() throws IOException {
        Properties pp = new Properties();
        pp.load(new FileReader("C:\\Users\\NJUSTZJC\\Desktop\\JavaProjects\\Java projects\\firstProject\\src\\FirstZjc\\data.properties"));
        String user = pp.getProperty("user");
        pp.setProperty("id","121110023062");
        pp.setProperty("name","张佳成");
        pp.setProperty("pwd","999999999");
         //中文保存的时候，并不是直接保存中文，而是保存中文的unicode码值。
        pp.list(System.out);
        pp.store(new FileOutputStream(
                "C:\\Users\\NJUSTZJC\\Desktop\\JavaProjects\\Java projects\\firstProject\\src\\FirstZjc\\data.properties2"),
                null);
    }
```


