# Thread创建线程
---
---

```java
public class main{
    public static void main(String[] args){
        A a = new A();
        a.start();
        
            int i = 0;
            while (i<=80){
                System.out.println(Thread.currentThread().getName()+i);
                try {
                    Thread.sleep(1000);
                } catch (InterruptedException e) {
                    e.printStackTrace();
                }
                i++;
            }



    }
}

class A extends Thread{
    @Override//方法的重写
    public void run() {
        while (true){
            System.out.println("当前的线程为:"+Thread.currentThread().getName());
            try {
                Thread.sleep(1000);
            } catch (InterruptedException e) {
                e.printStackTrace();
            }
        }
    }
}
```


![在这里插入图片描述](https://img-blog.csdnimg.cn/d7261bbc7513471ca0d45455f96a012b.png?x-oss-process=image/watermark,type_ZHJvaWRzYW5zZmFsbGJhY2s,shadow_50,text_Q1NETiBATkpVU1RaSkM=,size_20,color_FFFFFF,t_70,g_se,x_16)

