# do-while循环控制语句
---
----
![在这里插入图片描述](https://img-blog.csdnimg.cn/22807cd2b6174642a4eb91c57ba325f8.png?x-oss-process=image/watermark,type_ZHJvaWRzYW5zZmFsbGJhY2s,shadow_50,text_Q1NETiBATkpVU1RaSkM=,size_20,color_FFFFFF,t_70,g_se,x_16)
==先执行，再判断==。即do-while是一定会执行一次循环体的。而while和for中，是先判断，再执行，循环体有可能一次都不执行。

==先执行，再迭代==。

## 最后while后面有一个分号，千万不能忘记。忘记等于死路一条！！！


![在这里插入图片描述](https://img-blog.csdnimg.cn/34aeba910f2a4485887f38bc3e534064.png)
要债的人上门先把你打一顿，然后再问你还不还钱，这种属于==do-while==
要债的人问你还不还钱，不还钱的话才打你，这种属于==while==

练习：
![在这里插入图片描述](https://img-blog.csdnimg.cn/1e8be22de02d4a89ab1dbb7e7fd10988.png)

```java
public class A1{
	public static void main(String[] args){
		int count = 0,i = 1;
		do{
			if(i % 5 == 0 && i % 3 != 0){
				count++;
			}
			i++;
		}
		while(i <= 200);//最后while后面有一个分号，千万不能忘记。忘记等于死路一条
		输出count
	}
}
```

