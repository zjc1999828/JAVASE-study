# FileReader的使用及其方法
----
----
1. 一次性读取一个字符

```java
    @Test
    public void filereader(){
        String path = "D:\\zjc.txt";
        FileReader fr = null;
        int data = 0;
        try {
            FileReader fileReader = new FileReader(path);
            while((data = fileReader.read()) != -1){
                System.out.println((char)data);
            }
        } catch (IOException e) {
            e.printStackTrace();
        }finally {
            do {
                filereader().close()
            } while (true);
        }
    }
}



```




![在这里插入图片描述](https://img-blog.csdnimg.cn/7944a8c2d8c44ea0a0274e21145d745e.png?x-oss-process=image/watermark,type_ZHJvaWRzYW5zZmFsbGJhY2s,shadow_50,text_Q1NETiBATkpVU1RaSkM=,size_20,color_FFFFFF,t_70,g_se,x_16)
2. read（ch[]），一次性读取多个字符
```java
    @Test
    public void filereader(){
        String path = "D:\\zjc.txt";
        FileReader fr = null;
        char ch[] = new char[6];
        int re = 0;
        try {
            fr = new FileReader(path);
            while((re = fr.read(ch) )!= -1){
                System.out.print(new String(ch,0,re) );
            }
        } catch (IOException e) {
            e.printStackTrace();
        }finally {
            try {
                fr.close();
            } catch (IOException e) {
                e.printStackTrace();
            }
        }
    }
}




```

