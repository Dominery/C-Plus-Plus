# this

`this`是一个指向对象的指针。在成员函数内部，可以通过`this`来调用成员变量和其他成员函数。

* 友元函数没有`this`指针

```c++
class Line{
    public:
    double getLength();
    bool compare(Line line);
    Box(double length);
 	private:
    double length;
}
double Line::getLength(void){
    return length;
}
bool Line::compare(Line line){
    return this->getLength()>line.getLength();
}
Box::Box(double length){
    this->length = length;
}
```

