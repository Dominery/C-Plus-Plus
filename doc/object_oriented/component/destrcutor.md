# 析构函数

当类创建的对象被删除时，析构函数会被调用，用于释放资源。

```c++
#include <iostream>
using namespace std;
class Line{
    Public:
    ~Line();
}
Line::~Line(void){
    cout<<"delete object"<<endl;
}
```

* 只有当对象成功创建后被删除，析构函数才会被调用，如果在构造函数中发生异常，析构函数不会被调用。