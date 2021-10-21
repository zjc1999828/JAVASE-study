# 实现Runnable接口来创建多线程
---


![在这里插入图片描述](https://img-blog.csdnimg.cn/c69a90996c224f98932ac82fe40b170f.png?x-oss-process=image/watermark,type_ZHJvaWRzYW5zZmFsbGJhY2s,shadow_50,text_Q1NETiBATkpVU1RaSkM=,size_20,color_FFFFFF,t_70,g_se,x_16)

Thread的底层源码分析

```java
public class main{
    public static void main(String[] args){
        dog do2 = new dog();
        Thread thread0 = new Thread(do2);
        thread0.start();
    }
}

class dog implements Runnable{
    @Override
    public void run() {
        System.out.println("当前的线程为:"+Thread.currentThread().getName());
    }
}


//Thread的底层源码是如下面所示的：
class thread implements Runnable{
    private Runnable target;//因为向上转型，所以可以用接口类型的引用指向实现了接口的类的对象实例。

    public thread(Runnable target){
        this.target = target;
    }

    @Override
    public void run() {
        if(target != null){
            target.run();
        }
    }



    public void start(){
        this.start0();
    }
    public void start0(){
        this.run();
    }
}
```

