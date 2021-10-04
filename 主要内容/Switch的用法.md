# Switch的用法
----
----
- 简介
![在这里插入图片描述](https://img-blog.csdnimg.cn/c7f16232c0bd4f82a83466f21192e345.png?x-oss-process=image/watermark,type_ZHJvaWRzYW5zZmFsbGJhY2s,shadow_50,text_Q1NETiBATkpVU1RaSkM=,size_20,color_FFFFFF,t_70,g_se,x_16)
- 流程图
![在这里插入图片描述](https://img-blog.csdnimg.cn/c18f8a25451f478ab1f35e4962451829.png?x-oss-process=image/watermark,type_ZHJvaWRzYW5zZmFsbGJhY2s,shadow_50,text_Q1NETiBATkpVU1RaSkM=,size_20,color_FFFFFF,t_70,g_se,x_16)
## Switch用法的细节
![在这里插入图片描述](https://img-blog.csdnimg.cn/5de917fe07984ea98f5463f382be3625.png)
==例子==
![在这里插入图片描述](https://img-blog.csdnimg.cn/26481f2f53414ee3b81ced7e92359850.png?x-oss-process=image/watermark,type_ZHJvaWRzYW5zZmFsbGJhY2s,shadow_50,text_Q1NETiBATkpVU1RaSkM=,size_20,color_FFFFFF,t_70,g_se,x_16)

2.
![在这里插入图片描述](https://img-blog.csdnimg.cn/3119c8b7bcfe4a209f5ecef15975f5e8.png?x-oss-process=image/watermark,type_ZHJvaWRzYW5zZmFsbGJhY2s,shadow_50,text_Q1NETiBATkpVU1RaSkM=,size_20,color_FFFFFF,t_70,g_se,x_16)



3. 

![在这里插入图片描述](https://img-blog.csdnimg.cn/e4e097edf6194ba795e86853778c0444.png)
常量表达式:2+3/4+5/等等等等

4. 
![在这里插入图片描述](https://img-blog.csdnimg.cn/058dd6063145493fae912d378b6d5478.png)

5. 
![在这里插入图片描述](https://img-blog.csdnimg.cn/24daa36c7faa4bd2964e7bbd930293ae.png?x-oss-process=image/watermark,type_ZHJvaWRzYW5zZmFsbGJhY2s,shadow_50,text_Q1NETiBATkpVU1RaSkM=,size_20,color_FFFFFF,t_70,g_se,x_16)

## 具有代表性的练习题
![在这里插入图片描述](https://img-blog.csdnimg.cn/d74fc4c0681a4fa98a906216fb21f9fd.png?x-oss-process=image/watermark,type_ZHJvaWRzYW5zZmFsbGJhY2s,shadow_50,text_Q1NETiBATkpVU1RaSkM=,size_20,color_FFFFFF,t_70,g_se,x_16)
涵盖一个非常好的转换的编程思路。
```java
	double score = 1.1;

		//使用if-else 保证输入的成绩有有效的 0-100
		if( score >= 0 && score <= 100) {
			switch ((int)(score / 60)) {
				case 0 :
					System.out.println("不合格");
					break;
				case 1 :
					System.out.println("合格");
					break;
				// default :
				// 	System.out.println("输入有误");
			}
		} else {
			System.out.println("输入的成绩在0-100");
		}

```




![在这里插入图片描述](https://img-blog.csdnimg.cn/f8f9998a792f44e699484fe9c7127c75.png)
包含一个重要的==穿透方法==的使用



```java
Scanner myScanner = new Scanner(System.in);
		System.out.println("输入月份");
		int month = myScanner.nextInt();
		switch(month) {
			case 3:
			case 4:
			case 5: 
				System.out.println("这是春季");
				break;
			case 6:
			case 7:
			case 8: 
				System.out.println("这是夏季");
				break;
			case 9:
			case 10:
			case 11: 
				System.out.println("这是秋季");
				break;
			case 1:
			case 2:
			case 12: 
				System.out.println("这是冬季");
				break;
			default :
				System.out.println("你输入的月份不对(1-12)");
		}


	}
}
```

