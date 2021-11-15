# Class/Fileld/Method/Constructor的常用方法
---
---
![在这里插入图片描述](https://img-blog.csdnimg.cn/3e6f04c754e34799ad005b5a7e0f0a79.png?x-oss-process=image/watermark,type_ZHJvaWRzYW5zZmFsbGJhY2s,shadow_50,text_Q1NETiBATkpVU1RaSkM=,size_20,color_FFFFFF,t_70,g_se,x_16)
![在这里插入图片描述](https://img-blog.csdnimg.cn/b0e6edb433a94988997bba713d590a6f.png?x-oss-process=image/watermark,type_ZHJvaWRzYW5zZmFsbGJhY2s,shadow_50,text_Q1NETiBATkpVU1RaSkM=,size_20,color_FFFFFF,t_70,g_se,x_16)
![在这里插入图片描述](https://img-blog.csdnimg.cn/ad7bc7c355154343897c1d46ce6fafc9.png?x-oss-process=image/watermark,type_ZHJvaWRzYW5zZmFsbGJhY2s,shadow_50,text_Q1NETiBATkpVU1RaSkM=,size_20,color_FFFFFF,t_70,g_se,x_16)
![ ](https://img-blog.csdnimg.cn/48b6602e9b314e00a1ef1d415d68c4c9.png?x-oss-process=image/watermark,type_ZHJvaWRzYW5zZmFsbGJhY2s,shadow_50,text_Q1NETiBATkpVU1RaSkM=,size_20,color_FFFFFF,t_70,g_se,x_16)


```java
 public static void main(String args []) throws Exception {
        Class catcls = Class.forName("FirstZjc.cat");

        System.out.println(catcls.getName());//获取全类名

        System.out.println(catcls.getSimpleName());//获取简单类名

        Field[] fields = catcls.getFields();//获得所有public权限的属性，包括本类及父类的。
        for(Field f:fields){
            System.out.println(f.getName()+
                    "该类的属性修饰符值为:"+f.getModifiers()+
                    "该属性的数据类型所对应的Class对象为:"+f.getType());
        }
        catcls.getDeclaredFields();//获得所有权限修饰的属性，但是仅仅包括本类的。

        catcls.getMethods();//获得所有public权限的属性，包括本类及父类的，且父类不仅局限于直接父类

        Method[] declaredMethods = catcls.getDeclaredMethods();//获得所有权限修饰的属性，但是仅仅包括本类的。
        for(Method method:declaredMethods){
            System.out.println(method.getName()+
                    method.getModifiers()+
                    "该方法返回类型所对应的Class对象为"+method.getReturnType());
            Class<?>[] parameterTypes = method.getParameterTypes();
            for (Class<?> parameterType : parameterTypes) {
                System.out.println("该方法的形参类型为:"+parameterType)  ;
            }
        }

        catcls.getConstructors();//获得所有public权限的构造器，但是仅仅包括被雷的



        Constructor[] declaredConstructors = catcls.getDeclaredConstructors();//获得所有权限修饰的构造器，但是仅仅包括本类的。
        for (Constructor declaredConstructor : declaredConstructors) {
            System.out.println(declaredConstructor.getName()+declaredConstructor.getModifiers());
            Class[] parameterTypes = declaredConstructor.getParameterTypes();
            for (Class parameterType : parameterTypes) {
                System.out.println(parameterType);
            }
        }

        catcls.getPackage();//获得这个类对象的包信息。
        catcls.getSuperclass();//获得这个类对象的父类的Class对象的信息
    }
    }

```

