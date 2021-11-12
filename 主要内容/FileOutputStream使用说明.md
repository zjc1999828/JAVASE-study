# FileOutputStream使用说明
----
----

1. new FileOutputStream（filepath）是会重新创建文件，或者覆盖之前已经存在的内容。
```java

    @Test
    public void fileoutputstream(){
        String path = "D:\\out.txt";
        FileOutputStream fileOutputStream = null;
        try {
            fileOutputStream = new FileOutputStream(path);
            String aa = "the north face 小落叶太亮眼啦。而且不与黑色的撞衫，万事只求半称心。";
            fileOutputStream.write(aa.getBytes());
        } catch (IOException e) {
            e.printStackTrace();
        }finally {
            try {
                fileOutputStream.close();
            } catch (IOException e) {
                e.printStackTrace();
            }
        }
    }
```


2. 1. new FileOutputStream（filepath，true）是会追加到文件的末尾。

![在这里插入图片描述](https://img-blog.csdnimg.cn/32120667eb8f4cad8a86f881bb14aec0.png?x-oss-process=image/watermark,type_ZHJvaWRzYW5zZmFsbGJhY2s,shadow_50,text_Q1NETiBATkpVU1RaSkM=,size_20,color_FFFFFF,t_70,g_se,x_16)

```java
 @Test
    public void fileoutputstream(){
        String path = "D:\\out.txt";
        FileOutputStream fileOutputStream = null;
        try {
            fileOutputStream = new FileOutputStream(path,true);
            String aa = "人生哪能多如意。况且他妈的就是个衣服。";
            fileOutputStream.write(aa.getBytes());
        } catch (IOException e) {
            e.printStackTrace();
        }finally {
            try {
                fileOutputStream.close();
            } catch (IOException e) {
                e.printStackTrace();
            }
        }
    }
}
```

