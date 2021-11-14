# PrintWriter的使用方法
---
---
##### 作用为修改打印的输出位置

```bash
    @Test
    public void out()throws IOException{
        PrintWriter pw = new PrintWriter("D:\\zjc.txt");
        pw.print("asdasdas");
        pw.close();//一定要记住close流，否则无法显示
    }
```

