Title: 如何在一个bat批处理文件中调用另一个bat批处理文件？
Date: 2010-12-03 10:20
Modified: 2010-12-05 19:30
Category: Tech
Tags: pelican, publishing
Slug: tech2
Authors: Quan
Summary: Short version for index and feeds

我们有两个批处理文件outter和批处理文件inner，其内容如下：
outter.bat
```
echo "start to call inner bat here"
inner.bat                   //第2行
echo "Back to outter bat"    //注意这一行，它并未运行
```
inner.bat
```
echo "inner bat has been called."
```
如果像上面的在outter.bat调用inner.bat。我们发现outter.bat的第3行未执行。
即inner完成后并不会把控制权交回outter。

## 正确的方法应该是：在所调用的批处理文件名前加上call，把文件的第2行变为call inner.bat即可，如下：
outter.bat
```
echo "start to call inner bat here"
call inner.bat                   //第2行
echo "Back to outter bat"    //注意这一行，它并未运行
```

所以Django的测试server启动脚本应该是：
```

```