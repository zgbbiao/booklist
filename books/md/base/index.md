# 基础

## 安装pip 和 easy_install

pip 和 easy_install是下载python包的一个下载器

1. 下载easy_install

下载地址：https://pypi.python.org/pypi/ez_setup
![image.png](https://upload-images.jianshu.io/upload_images/13943027-ae25907d077e4c71.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

2. 进入包目录， 然后运行下面程序

```
python setup.py install
```
当出现Finished的时候表明安装成功了
![image.png](https://upload-images.jianshu.io/upload_images/13943027-33bbac0b39bed94c.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

3. 查看是否安装成功

```
easy_install --version
```
这时候发现，命令不正确， 因为没有配置环境变量
![image.png](https://upload-images.jianshu.io/upload_images/13943027-b14282d36f5aa8ee.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
配置完环境变量后， 再看看， 如果不行， 就重启电脑， 就可以用了。

3.  查看安装的包
![image.png](https://upload-images.jianshu.io/upload_images/13943027-62165729d3901024.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
在这里，可以看到我们安装的包是否安装进去。

4. Pip也安装好了
上面的步骤执行完毕， Pip也就安装好了。
```
pip --version
```

## NumPy环境

```javascript
pip install numpy
```


## numpy 特点

1. 多维数组
  可以多维间切换，比如二维切换成三维，三维切换成二维， 三行四列换成6行两列等功能。
2. 查询速度快
  是python中List的速度的几倍
3. 切片运算
  可以通过多维下标迅速找到值。
  


##  ndarray

1. 创建array 它从暴露数组接口的任何对象或任何返回数组的方法创建一个ndarray。

```
numpy.array(object, dtype = None, copy = True, order = None, subok = False, ndmin = 0)
```

具体可参考![参考网站](http://codingdict.com/article/8216)

### NumPy数据类型 dtype

对于匹配的字符串
```
int8 == 'i1'

int16 == 'i2'

int32 == 'i4'

int64 == '<i8'
```

// 类型和字符串转换
```
dt = np.dtype(np.int8)
dt2 = np.dtype('i1')
print(dt)  # int8
print(dt2)  # int8

dt = np.dtype([('age', np.int64)])
print(dt)  # [('age', '<i8')]
```

// 提取数据
```
a = np.array([(10,),(20,),(30,)], dtype = [('age', '<i8')])
print(a) #[(10,) (20,) (30,)]
print(a['age'])  # [10 20 30]
```

### NumPy数组属性

1. ndarray.shape形状（行和列）

返回形状

``` python
import numpy as np
a = np.array([[1,2,3],[4,5,6]])
print a.shape # (2, 3)
```

调整数组大小

```
a.shape = (3,2)
print a
# [[1, 2]
 [3, 4]
 [5, 6]]
```

```
b = a.reshape(3,2)
print b
# [[1, 2]
    [3, 4]
    [5, 6]]
```


