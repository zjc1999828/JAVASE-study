# enum关键字枚举类的应用
---
---
![在这里插入图片描述](https://img-blog.csdnimg.cn/410a584dbb7f473495600b5833c40cf9.png?x-oss-process=image/watermark,type_ZHJvaWRzYW5zZmFsbGJhY2s,shadow_50,text_Q1NETiBATkpVU1RaSkM=,size_20,color_FFFFFF,t_70,g_se,x_16)
5. 解读：即枚举对象必须放在枚举类的第一行。否则就编译出错！

```java
package FirstZjc;

public class main1 {
    public static void main(String[] args) {
        System.out.println(Season.SPRING);
    }
}


enum Season{

    SPRING("春天","sdsd"),SUMMER("夏天","撒旦撒旦"),what;

    private String name;
    private String description;

    private Season(String name, String description) {
        this.name = name;
        this.description = description;
    }

    private Season() {
    }

    public String getName() {
        return name;
    }

    public String getDescription() {
        return description;
    }

    @Override
    public String toString() {
        return "Season{" +
                "name='" + name + '\'' +
                ", description='" + description + '\'' +
                '}';
    }
}



```

