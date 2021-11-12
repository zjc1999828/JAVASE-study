# InputStream常用子类讲解之FileInputStream
---
---
![在这里插入图片描述](https://img-blog.csdnimg.cn/ba4c94771a394871b046136d28502c11.png?x-oss-process=image/watermark,type_ZHJvaWRzYW5zZmFsbGJhY2s,shadow_50,text_Q1NETiBATkpVU1RaSkM=,size_20,color_FFFFFF,t_70,g_se,x_16)

1. FileInputStream:文件输入流

read方法详解：
1. 
![在这里插入图片描述](https://img-blog.csdnimg.cn/8a23e1f2bea148d5958c764f523b4c73.png?x-oss-process=image/watermark,type_ZHJvaWRzYW5zZmFsbGJhY2s,shadow_50,text_Q1NETiBATkpVU1RaSkM=,size_20,color_FFFFFF,t_70,g_se,x_16)

在读取完毕之后，应该要关闭文件。

```java
    @Test
    public void fileinputstream(){
        String path = "D:\\opop.txt";
        int readdata = 0;
        FileInputStream fileInputStream = null;
        try {
            fileInputStream = new FileInputStream(path);
            while((readdata = fileInputStream.read()) != -1){
                System.out.println((char)readdata);
            }
        } catch (IOException e) {
            e.printStackTrace();
        }finally {
            try {
                fileInputStream.close();
            } catch (IOException e) {
                e.printStackTrace();
            }
        }
    }
}

```
2. 
![在这里插入图片描述](https://img-blog.csdnimg.cn/99782b924781478a99c4f40ca9dbc97a.png?x-oss-process=image/watermark,type_ZHJvaWRzYW5zZmFsbGJhY2s,shadow_50,text_Q1NETiBATkpVU1RaSkM=,size_20,color_FFFFFF,t_70,g_se,x_16)
该方法最终返回实际读取的总字节数。
![在这里插入图片描述](https://img-blog.csdnimg.cn/c01d6e4f932b4445a3e06c7657903b76.png?x-oss-process=image/watermark,type_ZHJvaWRzYW5zZmFsbGJhY2s,shadow_50,text_Q1NETiBATkpVU1RaSkM=,size_20,color_FFFFFF,t_70,g_se,x_16)

```java
    @Test
    public void fileinputstream(){
        java.lang.String path = "D:\\opop.txt";
        byte buf[] = new byte [3];
        int readLength ;
        FileInputStream fileInputStream = null;
        try {
           fileInputStream = new FileInputStream(path);
            while((readLength = fileInputStream.read(buf)) != -1){
                java.lang.String a = new java.lang.String(buf,0,readLength);
                System.out.println(a);
            }
        } catch (IOException e) {
            e.printStackTrace();
        }finally {
            try {
                fileInputStream.close();
            } catch (IOException e) {
                e.printStackTrace();
            }
        }
    }
}
```

