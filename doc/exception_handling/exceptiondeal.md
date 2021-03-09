# 处理异常

C++中异常处理只存在一种方式，异常捕获。

如果某段代码会抛出异常，该异常通过`try/catch`关键字进行捕获处理，那么称这种异常处理方式为异常捕获。

异常捕获时`catch`语句需要匹配异常的类型。

```c++
int main(int argc, char const *argv[])
{
    try{
        CnfFileParser("sat-20.cnf").parse();
    }catch(IOException &e){
        cout<<e.what()<<endl;
    }
    return 0;
}
```

