# InputStreamReader对象
---
---
字节流转换成了字符流，并且可以指定处理的编码方式。
![在这里插入图片描述](https://img-blog.csdnimg.cn/f3b1c2c6531649f382c4f5d151daae14.png?x-oss-process=image/watermark,type_ZHJvaWRzYW5zZmFsbGJhY2s,shadow_50,text_Q1NETiBATkpVU1RaSkM=,size_20,color_FFFFFF,t_70,g_se,x_16)

```c
    @Test
    public void in()throws IOException{
        String path = "D:\\ZCJ.txt";
        String rl;
        InputStreamReader isr = new InputStreamReader(new FileInputStream(path), "gbk");
        BufferedReader br = new BufferedReader(isr);
        while((rl = br.readLine() )!= null){
            System.out.println(rl);
        };
        if(br != null)br.close();
    }
```

