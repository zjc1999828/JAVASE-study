# if-else的使用
---
---
## 单分支
![在这里插入图片描述](https://img-blog.csdnimg.cn/d24b476b441344d98ad9e027754c1201.png?x-oss-process=image/watermark,type_ZHJvaWRzYW5zZmFsbGJhY2s,shadow_50,text_Q1NETiBATkpVU1RaSkM=,size_20,color_FFFFFF,t_70,g_se,x_16)
![在这里插入图片描述](https://img-blog.csdnimg.cn/8879e711e38b44919507219f5374264d.png?x-oss-process=image/watermark,type_ZHJvaWRzYW5zZmFsbGJhY2s,shadow_50,text_Q1NETiBATkpVU1RaSkM=,size_20,color_FFFFFF,t_70,g_se,x_16)
## 双分支
![在这里插入图片描述](https://img-blog.csdnimg.cn/4e8372c1f37349b5bac441e766fc5498.png?x-oss-process=image/watermark,type_ZHJvaWRzYW5zZmFsbGJhY2s,shadow_50,text_Q1NETiBATkpVU1RaSkM=,size_20,color_FFFFFF,t_70,g_se,x_16)
![在这里插入图片描述](https://img-blog.csdnimg.cn/a2013cf266714e2f9cfd4d2703569bb7.png?x-oss-process=image/watermark,type_ZHJvaWRzYW5zZmFsbGJhY2s,shadow_50,text_Q1NETiBATkpVU1RaSkM=,size_20,color_FFFFFF,t_70,g_se,x_16)
## 多分支1
![在这里插入图片描述](https://img-blog.csdnimg.cn/560f15bd732d4391bbdcc8d03a6bce01.png?x-oss-process=image/watermark,type_ZHJvaWRzYW5zZmFsbGJhY2s,shadow_50,text_Q1NETiBATkpVU1RaSkM=,size_20,color_FFFFFF,t_70,g_se,x_16)
说明：
![在这里插入图片描述](https://img-blog.csdnimg.cn/5be818ee841941fb92c9dab9e1f7412b.png?x-oss-process=image/watermark,type_ZHJvaWRzYW5zZmFsbGJhY2s,shadow_50,text_Q1NETiBATkpVU1RaSkM=,size_20,color_FFFFFF,t_70,g_se,x_16)
==只能进入一个入口去执行，执行完之后则立即退出该多分支程序。==



## 多分支2
###### 该种多分支程序就等价于许多许多个单分支==if(){}==程序叠加在一起去判断。



- 双分支结构和多分支结构结合在一起使用，会有意想不到的效果：
![在这里插入图片描述](https://img-blog.csdnimg.cn/487f22a534e7432fa0dae23db25d41cf.png?x-oss-process=image/watermark,type_ZHJvaWRzYW5zZmFsbGJhY2s,shadow_50,text_Q1NETiBATkpVU1RaSkM=,size_20,color_FFFFFF,t_70,g_se,x_16)


## 嵌套分支
![在这里插入图片描述](https://img-blog.csdnimg.cn/152176a3e771478ab344171d6673a80c.png?x-oss-process=image/watermark,type_ZHJvaWRzYW5zZmFsbGJhY2s,shadow_50,text_Q1NETiBATkpVU1RaSkM=,size_20,color_FFFFFF,t_70,g_se,x_16)
==所谓的嵌套分支就是单分支/双分支/多分支1/多分支2这4个类别当中，任意几个组合在一起使用==

- 下面我们直接看一个例子

![在这里插入图片描述](https://img-blog.csdnimg.cn/dad66b3ec97d4221a2bf92bdb21028d0.png?x-oss-process=image/watermark,type_ZHJvaWRzYW5zZmFsbGJhY2s,shadow_50,text_Q1NETiBATkpVU1RaSkM=,size_20,color_FFFFFF,t_70,g_se,x_16)

- 代码如下
```java
import java.util.Scanner;
public class A1{
	public static void main(String[] args){
		Scanner MyScanner = new Scanner(System.in);
		System.out.println("请输入你的年龄:");
		int age = MyScanner.nextInt();
		int month = 5;
		double price = 60;
		if(month >= 4 && month <= 10){
			if(age >= 18 && age <= 60){
				System.out.println("票价为:"+price);
			}
			if(age < 18){
				System.out.println("票价为:"+price/2);
			}
			if(age > 60){
				System.out.println("票价为:"+price/3);
			}

		}
		else{
			if(age >= 18 && age <= 60){
				System.out.println("票价为:"+40);
			}
			else{
				System.out.println("票价为:"+20);
			}
		}
	}
}
```

