# OutputStreamReader的使用方法
----
----

```c
  @Test
    public void out()throws IOException{
        String path = "D:\\SDSD.txt";
        BufferedWriter bw = new BufferedWriter(new OutputStreamWriter(new FileOutputStream(path),"gbk"));
        bw.write("the north face小落叶真式越看越有味啊");
        if(bw != null)bw.close();
        System.out.println("gbk");
    }
```

