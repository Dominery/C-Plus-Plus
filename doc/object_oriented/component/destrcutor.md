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

