# friend

* 友元函数

  如果一个非成员函数在类中`friend`修饰声明，在类外定义，那么该函数称为这个类的友元函数。

  * 友元函数方法体中可以访问类的所有成员变量。

* 友元类

  如果一个类B在另一个类A中通过`friend`修饰声明，在类A外定义，那么称类B为类A的友元类。

```c++
#include <iostream>
using namespace std;
class Line{
    public:
    friend void printLength(Line line);
    private:
    double length;
}
void printLength(Line line){
    cout<< line.length <<endl;
}
```

