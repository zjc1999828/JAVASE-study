# ObjectOutputStream的使用方法
---
---
![在这里插入图片描述](https://img-blog.csdnimg.cn/7cb0def02ef04ccba2e9d455b7f79911.png)

```c
 @Test
    public void ObjectOutputStream()throws IOException{
        String inpath = "D:\\data.dat";
        ObjectOutputStream oo = new ObjectOutputStream(new FileOutputStream(inpath));
        //整型数
        oo.writeInt(100);
        //布尔型数
        oo.writeBoolean(true);
       //字符串数
        oo.writeUTF("sdsd");
        //对象数
        oo.writeObject(new cat("sd",12));
```

