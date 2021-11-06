# Comparator接口的理解
---
---

### 静态方法块

```java
public class comp {
    public static void bubble(int arr[], Comparator c){
        int temp = 0;
        for(int i = 0;i<arr.length-1;i++){
            for(int j = 0;j< arr.length-1-i;j++){
                if(c.compare(arr[j],arr[j+1])>0){
                    temp = arr[j];
                    arr[j] = arr[j+1];
                    arr[j+1] = temp;
                }
            }
        }
    }
}

```
### 主程序

```java
@SuppressWarnings({"all"})
public class main1{
    public static void main(String[] args) {
        int arrs [] = {23,1,233,2,0,-1,23,19};
        comp.bubble(arrs, new Comparator() {
            @Override
            public int compare(Object o1, Object o2) {
                return ((Integer) o1)-((Integer) o2);
            }
        });
        System.out.println(Arrays.toString(arrs));
    }
}

```

