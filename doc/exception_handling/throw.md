# 抛出异常

如果需要在某个方法中抛出异常，跟据抛出的异常类型是否是异常类，存在两种方式：

1. 异常类实例化抛出法

   1. 找到合适的异常类
   2. 创建该异常类的对象
   3. 通过`throw`关键字将对象抛出

   ```c++
   CnfFileParser::CnfFileParser(string filename)
   {
       fin.open(filename);
       if(!fin.is_open())throw IOException("error",filename+":not found");
   }
   ```

2. 非异常类实例化抛出法

   1. 找到适合抛出的对象，`int`、`string`等

   2. 通过`throw`关键字将对象抛出

   ```c++
   double division(int a,int b){
       if(b==0) throw "division by zero";
       return a/b;
   }
   ```



​      

