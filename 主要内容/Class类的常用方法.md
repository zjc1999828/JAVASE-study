

# Class类的常用方法

```java
    public static void main(String args []) throws Exception {
        //类的全路近。
        String path = "FirstZjc.cat";
        Class cls = Class.forName(path);
        System.out.println(cls);//cls这个类对象是哪个类的
        System.out.println(cls.getClass());//cls这个类对象的运行类型->java.lang.Class
        System.out.println(cls.getPackage().getName());//包名
        System.out.println(cls.getName());//得到全类名
        cat o = (cat)cls.newInstance();//创建对象实例。
        System.out.println(o);
        Field age = cls.getField("age");//private修饰的成员变量是无法获取的。
        System.out.println(age);//这样只是获得了age这个成员变量对应的对象。
        System.out.println(age.get(o));//只有.get()才能获得该成员变量的具体信息
        age.set(o,1000);//改变某个成员变量的值。
        System.out.println(age.get(o));
        //获得所有成员变量的名称
        Field[] fields = cls.getFields();
        for(Field f:fields){
            System.out.println(f.getName());
        }
    }
```



