# finalize的使用
---
---

## 预备知识
对象在没有引用指向它的时候，就会被垃圾回收器给销毁。

- 例子
```java
car bmw = new car();
bmw = null;
```

finalize（）方法就是在对象被销毁之前，jvm调用的一种方法，常用来做释放资源等一些任务。
![在这里插入图片描述](https://img-blog.csdnimg.cn/b9e353513a2d4fc7b5a211537c08d0ea.png)
### 注意
1. 并不是说一个对象没有引用指向它后，系统就会立即对它进行垃圾回收。
2. ![在这里插入图片描述](https://img-blog.csdnimg.cn/4b0e0e555a45408f996c066cde7a8b78.png)

