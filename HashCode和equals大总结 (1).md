# HashCode和equals大总结
---
---
![在这里插入图片描述](https://img-blog.csdnimg.cn/b26064148bb84ba1bb986c0ac25c44ea.png?x-oss-process=image/watermark,type_ZHJvaWRzYW5zZmFsbGJhY2s,shadow_50,text_Q1NETiBATkpVU1RaSkM=,size_20,color_FFFFFF,t_70,g_se,x_16)


![在这里插入图片描述](https://img-blog.csdnimg.cn/93909ba9746f4ca68f35730b16ce3ccd.png?x-oss-process=image/watermark,type_ZHJvaWRzYW5zZmFsbGJhY2s,shadow_50,text_Q1NETiBATkpVU1RaSkM=,size_20,color_FFFFFF,t_70,g_se,x_16)

![在这里插入图片描述](https://img-blog.csdnimg.cn/dcd534f84d1c4a6e8f7bcd4b79b1d1e6.png)
3) 不同的对象，有时也会有相同的哈希值。这个就叫做哈希冲突。

![在这里插入图片描述](https://img-blog.csdnimg.cn/059b1d14e78642acbe17a957f668b638.png)
![在这里插入图片描述](https://img-blog.csdnimg.cn/0e31cd7e3a304341b1d0e3336d63310c.png?x-oss-process=image/watermark,type_ZHJvaWRzYW5zZmFsbGJhY2s,shadow_50,text_Q1NETiBATkpVU1RaSkM=,size_20,color_FFFFFF,t_70,g_se,x_16)

![在这里插入图片描述](https://img-blog.csdnimg.cn/a6231496084c4d9281a8a3d1c1990305.png?x-oss-process=image/watermark,type_ZHJvaWRzYW5zZmFsbGJhY2s,shadow_50,text_Q1NETiBATkpVU1RaSkM=,size_20,color_FFFFFF,t_70,g_se,x_16)

![在这里插入图片描述](https://img-blog.csdnimg.cn/ffc907f4f60f48e7af80e2d743bbb2ef.png?x-oss-process=image/watermark,type_ZHJvaWRzYW5zZmFsbGJhY2s,shadow_50,text_Q1NETiBATkpVU1RaSkM=,size_20,color_FFFFFF,t_70,g_se,x_16)
- 反例
![在这里插入图片描述](https://img-blog.csdnimg.cn/e0859004adb64576b89e8d1c9a5fcc6f.png)


### 哈希冲突
![在这里插入图片描述](https://img-blog.csdnimg.cn/3af30456eb6a445084222ff5c8aa841a.png)
![在这里插入图片描述](https://img-blog.csdnimg.cn/dd3f681cd8d94287a8cdf67d23c61e69.png)


### 练习题
![在这里插入图片描述](https://img-blog.csdnimg.cn/50bb48ea4d63465799244f3e99b9af43.png?x-oss-process=image/watermark,type_ZHJvaWRzYW5zZmFsbGJhY2s,shadow_50,text_Q1NETiBATkpVU1RaSkM=,size_20,color_FFFFFF,t_70,g_se,x_16)

```java
import java.util.HashSet;
import java.util.Objects;
import java.util.Set;

public class test {
    public static void main(String[] args) {
        Set s = new HashSet();
        Birthday birth1 = new Birthday(1999,8,28);
        Birthday birth2 = new Birthday(2000,8,28);
        Birthday birth3 = new Birthday(1999,8,28);
        s.add(new dog(11,"jack",birth1));
        s.add(new dog(12,"david",birth2));
        s.add(new dog(11,"david",birth3));
        System.out.println(s);
    }
}



class dog{
    private int age;
    private String name;
    private Birthday birth;

    @Override
    public boolean equals(Object o) {
        if (this == o) return true;
        if (o == null || getClass() != o.getClass()) return false;
        dog dog = (dog) o;
        return age == dog.age && Objects.equals(birth, dog.birth);
    }

    @Override
    public int hashCode() {
        return Objects.hash(age,  birth);
    }

    public int getAge() {
        return age;
    }

    public void setAge(int age) {
        this.age = age;
    }

    public String getName() {
        return name;
    }

    public void setName(String name) {
        this.name = name;
    }

    public Birthday getBirth() {
        return birth;
    }

    public void setBirth(Birthday birth) {
        this.birth = birth;
    }

    public dog(int age, String name, Birthday birth) {
        this.age = age;
        this.name = name;
        this.birth = birth;
    }

    @Override
    public String toString() {
        return "dog{" +
                "age=" + age +
                ", name='" + name + '\'' +
                ", birth=" + birth +
                '}';
    }
}

class Birthday{
    private int year;
    private int month;
    private int day;

    public Birthday(int year, int month, int day) {
        this.year = year;
        this.month = month;
        this.day = day;
    }

    public int getYear() {
        return year;
    }

    public void setYear(int year) {
        this.year = year;
    }

    public int getMonth() {
        return month;
    }

    public void setMonth(int month) {
        this.month = month;
    }

    public int getDay() {
        return day;
    }

    public void setDay(int day) {
        this.day = day;
    }

    @Override
    public String toString() {
        return "Birthday{" +
                "year=" + year +
                ", month=" + month +
                ", day=" + day +
                '}';
    }

    @Override
    public boolean equals(Object o) {
        if (this == o) return true;
        if (o == null || getClass() != o.getClass()) return false;
        Birthday birthday = (Birthday) o;
        return year == birthday.year &&
                month == birthday.month &&
                day == birthday.day;
    }

    @Override
    public int hashCode() {
        return Objects.hash(year, month, day);
    }
}


```

