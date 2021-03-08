# 构造函数

当类创建一个对象时，构造函数会被调用，用于初始化某些成员变量。

类的默认构造函数无参数，每个类都至少有一个构造函数。

```c++
class Line{
    public:
    Line(double len);
    Line();
    private:
    double length;
}
Line::Line(void){
    length = 1;
}
Line::Line(double len){
    length = len;
}
```

初始化成员变量可以通过初始化列表实现。

```c++
Line::Line(double len):length(len){} //equals to the code above
```

