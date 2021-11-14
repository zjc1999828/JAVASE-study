# BufferedInputStream和BufferedOutputStream的使用极其方法
---
---
```c
@Test
    public void BufferedInputS()throws IOException{
        String inpath = "D:\\ZJC-in\\video2.wmv";
        String outpath = "D:\\ZJC-out\\video1.wmv";
        int readline = 0;
        byte b[] = new byte[1024];
        BufferedInputStream  bi  = new BufferedInputStream(new FileInputStream(outpath));
        BufferedOutputStream bo = new BufferedOutputStream(new FileOutputStream(inpath));
        while((readline = bi.read(b)) != -1 ){
            bo.write(b,0,readline);
        }
        if(bi != null){
            bi.close();
        }
        if(bo != null){
            bo.close();
        }
```

