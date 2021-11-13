# FileWriter的使用及其方法
---
---
![在这里插入图片描述](https://img-blog.csdnimg.cn/b321fa3908904e2ea8668d8989049dd7.png?x-oss-process=image/watermark,type_ZHJvaWRzYW5zZmFsbGJhY2s,shadow_50,text_Q1NETiBATkpVU1RaSkM=,size_20,color_FFFFFF,t_70,g_se,x_16)
![在这里插入图片描述](https://img-blog.csdnimg.cn/e5afa89549b94121bcfddd8cadd4754a.png?x-oss-process=image/watermark,type_ZHJvaWRzYW5zZmFsbGJhY2s,shadow_50,text_Q1NETiBATkpVU1RaSkM=,size_20,color_FFFFFF,t_70,g_se,x_16)

##### write常用的几种形式：
![在这里插入图片描述](https://img-blog.csdnimg.cn/d61501d1b85b497fa4b826434d6146f5.png?x-oss-process=image/watermark,type_ZHJvaWRzYW5zZmFsbGJhY2s,shadow_50,text_Q1NETiBATkpVU1RaSkM=,size_20,color_FFFFFF,t_70,g_se,x_16)

```c
    @Test
    public void filewriter(){
        String path = "D:\\note.txt";
        FileWriter fw = null;
        char ch [] = {'a','2','c'};


        try {
            fw = new FileWriter(path);
            fw.write(ch,0,2);
        } catch (IOException e) {
            e.printStackTrace();
        }finally {
            try {
                fw.close();
            } catch (IOException e) {
                e.printStackTrace();
            }
        }
    }
}


```

