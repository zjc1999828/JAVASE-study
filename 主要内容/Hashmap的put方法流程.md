# Hashmap的put方法流程
---
---


因为一开始是数组里面是空的，所以添加第一个元素的时候，直接根据计算出的索引值放入对应的位置。然后会判断此时数组里面的size数是否超过threshold（阀值），如果超过了。则会进行resize（）扩容，很明显，现在没超过。
下面继续添加元素，还是先计算该元素的hash值，如果hash不冲突，同第一个元素。如果hash冲突了。则分为三种情况。
1.	新添加的元素与该链表的表头结点的hash值一样且通过equals（）方法判断下来也一样，则不添加，直接覆盖掉value。
2.	添加的地方是一个红黑树，则将新元素直接挂载到树上。
3.	遍历整个链表，如果链表中新添加的元素已经存在，则不再添加；若不存在，则在遍历过后，将新添加的元素添加在链表的最后。注意：把新元素添加到链表的最后之后，立即判断，如果该链表的结点数>=8，但数组元素个数<64，则会进行数组扩容（乘以2）；如果该链表的结点数>=8，但数组元素个数>=64，则会将该链表转化为红黑树。；

