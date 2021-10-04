# 循环控制的使用方法
---
---
- for循环
![在这里插入图片描述](https://img-blog.csdnimg.cn/c6f827d3e47a448385d59db0e5bbb795.png?x-oss-process=image/watermark,type_ZHJvaWRzYW5zZmFsbGJhY2s,shadow_50,text_Q1NETiBATkpVU1RaSkM=,size_20,color_FFFFFF,t_70,g_se,x_16)
流程图
![在这里插入图片描述](https://img-blog.csdnimg.cn/3017ce12b7d94e0faee6587950f19f76.png?x-oss-process=image/watermark,type_ZHJvaWRzYW5zZmFsbGJhY2s,shadow_50,text_Q1NETiBATkpVU1RaSkM=,size_20,color_FFFFFF,t_70,g_se,x_16)
PS：先执行循环操作，再进行循环变量迭代。

## for循环的写法:
![在这里插入图片描述](https://img-blog.csdnimg.cn/7c3c7e469bff4fc5877b6f18e392b976.png?x-oss-process=image/watermark,type_ZHJvaWRzYW5zZmFsbGJhY2s,shadow_50,text_Q1NETiBATkpVU1RaSkM=,size_20,color_FFFFFF,t_70,g_se,x_16)
此时变量==i==的作用域只在for循环体中，即==i==只能在循环体中使用。


- 为了在循环体外也能使用变量  ==i==。可以改成下面的循环写作方式 
![在这里插入图片描述](https://img-blog.csdnimg.cn/f54ad13304254d188a3146cdd76611d6.png?x-oss-process=image/watermark,type_ZHJvaWRzYW5zZmFsbGJhY2s,shadow_50,text_Q1NETiBATkpVU1RaSkM=,size_20,color_FFFFFF,t_70,g_se,x_16)
- 无限循环的写法：
![在这里插入图片描述](https://img-blog.csdnimg.cn/a3631a0c142c4fe7b2710ee1a5d6d6dd.png)
- 多条循环初值和多条循环迭代
![在这里插入图片描述](https://img-blog.csdnimg.cn/724170cf7548406fa8bb87d4e657cfeb.png)
![在这里插入图片描述](https://img-blog.csdnimg.cn/e97bb3ac2fbf4a83a3aae6efc2a20ca2.png)


练习：

- 体验化繁为简/先死后活的编程思想。
![在这里插入图片描述](https://img-blog.csdnimg.cn/77c945d0fad140d7838f41a4a42c2cc2.png)

```java
//打印1~100之间所有是9的倍数的整数，统计个数  及 总和.[化繁为简,先死后活]
		//两个编程思想(技巧)
		//1. 化繁为简 : 即将复杂的需求，拆解成简单的需求，逐步完成
		//2. 先死后活 : 先考虑固定的值，然后转成可以灵活变化的值
		//
		//思路分析
		//打印1~100之间所有是9的倍数的整数，统计个数  及 总和
		//化繁为简
		//(1) 完成 输出 1-100的值
		//(2) 在输出的过程中，进行过滤，只输出9的倍数  i % 9 ==0
		//(3) 统计个数 定义一个变量 int count = 0; 当 条件满足时 count++;
		//(4) 总和 , 定义一个变量 int sum = 0; 当条件满足时累积 sum += i;
		//先死后活
		//(1) 为了适应更好的需求，把范围的开始的值和结束的值，做出变量
		//(2) 还可以更进一步 9 倍数也做成变量 int t = 9;

		int count = 0; //统计9的倍数个数 变量
		int sum = 0; //总和
		int start = 10;
		int end = 200;
		int t = 5; // 倍数
		for(int i = start; i <= end; i++) {
			if( i % t == 0) {
				System.out.println("i=" + i);
				count++;
				sum += i;//累积
			}
		}

		System.out.println("count=" + count);
		System.out.println("sum=" + sum);

	}
}
```

