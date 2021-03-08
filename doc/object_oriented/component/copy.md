# 拷贝构造函数

当通过一个已存在的对象创建新的对象时，拷贝构造函数会被调用，其用途如下：

1. 使用一个同类型的对象初始化新创建的对象
2. 复制对象把其作为参数传递给函数
3. 复制对象作为函数返回值

如果类带有指针变量，并有动态内存分配，那么该类必须定义拷贝构造函数。

```c++
#include <iostream>
using namespace std;
class Line{
    public:
    Line(const Line &obj);
    private:
    int *ptr;
}
Line::Line(const Line &obj){
    ptr = new int;
    *ptr = *obj.ptr;
}
```

