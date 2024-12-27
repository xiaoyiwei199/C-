# 语法注意点
C++语法注意点

## 指针
  - 如果是两个指针做减法，p1-p2的值是两者之间元素的个数，而不是地址的差
    - 比如int array[] = {1,2,3,4,5}; p1 = array; p2 = &array[2]; 那么p2-p1 = 2，而不是8（一个int占4个字节）
    - const int* p代表不能修改p所指向的元素的值
    - int* const p代表这个指针不能retarget，就是这个指针不能指向其他的元素，也就代表他自己本身的值不能修改。
    - 为什么需要用指针？用引用不就好了吗？
      - Chili以链表举例，比如最后一个链表的Next必须是指针，因为引用是必须初始化的，不能为空，而指针可以为空
      - 并且对于链表添加和删除来说，都需要使用指针的Retarget，而引用则不能Retarget。
      - 再比如说你使用的库，他就给你返回一个指针，那你是不是只能用指针？这也是为什么要用指针的一个强找的理由。
