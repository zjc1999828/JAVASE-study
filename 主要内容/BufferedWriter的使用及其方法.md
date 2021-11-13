# BufferedWriter的使用及其方法
---
---

```c
@Test
    public void Bufffilewriter()throws IOException{
        String path = "D:\\zjc.txt";
        BufferedWriter bw = new BufferedWriter(new FileWriter(path,true));
        bw.write("hello,NJUSTZJC1");
        bw.write('\n');
        bw.write("hello,NJUSTZJC2");
        bw.write('\n');
        bw.write("hello,NJUSTZJC3");
        bw.write('\n');
        bw.write("hello,NJUSTZJC4");
        bw.write('\n');
        bw.close();
    }
```

