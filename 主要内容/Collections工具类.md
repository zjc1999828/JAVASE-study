# Collections工具类
---
---
1. Collection.reverse方法。即翻转List中元素的顺序
![在这里插入图片描述](https://img-blog.csdnimg.cn/6ea7a036ba6545e2a10e4689f2f8b5e8.png)
```java
        ArrayList<Object> li = new ArrayList<Object>();
        li.add("tom1");
        li.add("tom2");
        li.add("tom3");
        li.add("tom4");
        Collections.reverse(li);
```

2. Collection.shuffle方法。即对List集合元素进行随机排序
![在这里插入图片描述](https://img-blog.csdnimg.cn/28e2d4327b944357911fc18f34061c98.png)

```java
        ArrayList<Object> li = new ArrayList<Object>();
        li.add("tom1");
        li.add("tom2");
        li.add("tom3");
        li.add("tom4");
        Collections.shuffle(li);
        System.out.println(li);
```

3. Collections.sort(List，Comparator（))方法

```java
 ArrayList<Object> li = new ArrayList<Object>();
        li.add("tom1");
        li.add("tom2");
        li.add("tom3");
        li.add("tom4");
        Collections.sort(li, new Comparator<Object>() {
            @Override
            public int compare(Object o1, Object o2) {
                String o11 = (String)o1;
                String o22 = (String)o2;
                return o22.charAt(3)-o11.charAt(3);
            }
        });
        System.out.println(li);
```
4. Collections.swap(List,int,int)
交换两处索引的元素顺序
![在这里插入图片描述](https://img-blog.csdnimg.cn/997af46b77cf41dab5e967f64599ffd0.png?x-oss-process=image/watermark,type_ZHJvaWRzYW5zZmFsbGJhY2s,shadow_50,text_Q1NETiBATkpVU1RaSkM=,size_20,color_FFFFFF,t_70,g_se,x_16)
5. Collection.max（List,new comparator）
![在这里插入图片描述](https://img-blog.csdnimg.cn/b76966a378b34da6b65e3abbf3bee8ca.png?x-oss-process=image/watermark,type_ZHJvaWRzYW5zZmFsbGJhY2s,shadow_50,text_Q1NETiBATkpVU1RaSkM=,size_20,color_FFFFFF,t_70,g_se,x_16)
6. Collections.frequency
返回指定集合中某元素的出现次数。

```java
  ArrayList<Object> li = new ArrayList<Object>();
        li.add("tom1");
        li.add("tom2");
        li.add("tom3");
        li.add("tom4");
        System.out.println(Collections.frequency(li,"tom1"));
```
7. Collections.replaceAll 即替换某些特定的元素
![在这里插入图片描述](https://img-blog.csdnimg.cn/c1a11bca5db84e3d8e5fc8e7356887d5.png?x-oss-process=image/watermark,type_ZHJvaWRzYW5zZmFsbGJhY2s,shadow_50,text_Q1NETiBATkpVU1RaSkM=,size_20,color_FFFFFF,t_70,g_se,x_16)

