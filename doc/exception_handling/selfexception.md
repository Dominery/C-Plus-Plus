# 定义异常

如果某个方法需要抛出异常，现有的异常类皆不能满足想要抛出的异常的需求，且想要通过以异常类实例化的形式抛出，那么可以自定义异常类，其步骤如下：

1. 继承现有的异常体系，`runtime_error`、`logic_error`
2. 重载`what`虚函数

```c++
class IOException:public runtime_error{
    private:
    string info;
    public:
    IOException(string s,string info);
    const char* what();
    ~IOException(){};
};
IOException::IOException(string s,string info):runtime_error(s){
    this->info = info;
}
const char* IOException::what(){
    return info.c_str();
}
```



