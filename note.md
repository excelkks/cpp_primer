## charpter3

### **直接初始化** 和 **拷贝初始化**
直接初始化直接将值写入对象中，拷贝初始化先创建一个中间变量，再拷贝到对象中。例如
```c++
string s1(10, 'c'); // 直接初始化
string s2 = 'hello';  // 拷贝初始化

// string s2 = 'hello'; 等价于
string temp('hello');
string s2 = temp;
```

### 理解复杂的数组声明
由内向外
```c++
int *ptrs[10];    // ptrs是含有10个整型指针的数组
int &refs[10] = /* ? */    // 错误：不存在引用的数组
int (*Parray)[10] = &arr;  // Parray指向一个含有10个整型的数组
int (&arrRef)[10] = arr;   // arrRef引用一个含有10个整型的数组
```
