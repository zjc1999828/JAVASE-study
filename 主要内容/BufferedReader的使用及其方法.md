# BufferedReader的使用及其方法
---
---
![在这里插入图片描述](https://img-blog.csdnimg.cn/54b602e6e279468babac285320771f29.png?x-oss-process=image/watermark,type_ZHJvaWRzYW5zZmFsbGJhY2s,shadow_50,text_Q1NETiBATkpVU1RaSkM=,size_20,color_FFFFFF,t_70,g_se,x_16)
在关闭包装流的时候，其底层会自动关闭包装的节点流。


源码如下：
![在这里插入图片描述](https://img-blog.csdnimg.cn/6c1fb53479f64715b4c8dff319f9ca96.png?x-oss-process=image/watermark,type_ZHJvaWRzYW5zZmFsbGJhY2s,shadow_50,text_Q1NETiBATkpVU1RaSkM=,size_20,color_FFFFFF,t_70,g_se,x_16)




read方法的详解：

![在这里插入图片描述](https://img-blog.csdnimg.cn/b0777bb47fe84a9c86fc31bc7ce14df3.png?x-oss-process=image/watermark,type_ZHJvaWRzYW5zZmFsbGJhY2s,shadow_50,text_Q1NETiBATkpVU1RaSkM=,size_20,color_FFFFFF,t_70,g_se,x_16)

```c
    @Test
    public void filewriter()throws IOException{
        String path = "D:\\note.txt";
        String rl;
        BufferedReader br = new BufferedReader(new FileReader(path));
        while((rl = br.readLine()) != null ){
            System.out.println(rl);
        }
        br.close();
    }
```

