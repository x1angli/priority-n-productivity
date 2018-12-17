# A recitation lecture on Python and Data Science / 一节有关于Python和数据科学的实用讲座

## 1. 安装python与准备环境

### 1.0 远程的Jupyter，免去本地安装之苦
__直接运行[Google Colab](https://colab.research.google.com)__
是Google公司做的一款小产品，能够在浏览器里直接运行，这样就可以略过以下的内容……

### 1.1 安装Anaconda全家桶，并且相应地设置
Anaconda全家桶集成了Python语言，numpy+scipy+matplotlib等最常用的数学包，Jupyter交互式执行器，Spyder和VSCode的下载器，
__请一步步按照 [这篇cookbook](cookbook-setting_up-environment-for-data_science.md) 里完成__

### 1.2 更新和设置python
在管理员权限的Windows或者其他操作系统的命令行（cli）下，运行下列命令

     python -m ensurepip --default-pip
     python -m pip install --upgrade pip
     pip install pip -U
     pip config set global.index-url https://pypi.tuna.tsinghua.edu.cn/simple

### 1.3 其他
对于那些在windows下经常安装不了的包（比如tensorflow, openCV），建议从个人开发者那儿下载已经编译成二进制的包
Unofficial Windows Binaries for Python Extension Packages
https://www.lfd.uci.edu/~gohlke/pythonlibs/


## 2. 常见教程

### 2.1 Python教程
* [W3学校教程](https://www.w3schools.com/python/)
    * 看到“File Handling”就可以了
* [官方的python教程——全套](https://docs.python.org/3/tutorial/)
    * 注意：这是全套教程，所以特别详细（冗长），建议有的放矢
* [Python的技巧](http://book.pythontips.com)
    * 这是一个具备一定基础后的进阶教程，却很实用

### 2.2 numpy教程 与 数据科学
* [Numpy官方教程](https://docs.scipy.org/doc/numpy-1.15.0/user/quickstart.html)
* [TutorialsPoint的教程](https://www.tutorialspoint.com/numpy/numpy_arithmetic_operations.htm)
* [Python DataScience Handbook](https://jakevdp.github.io/PythonDataScienceHandbook/index.html)
    * 强烈推荐：里面介绍了几个重要模块，包括IPython的使用，NumPy和Pandas作为数据和统计的基础包，Matplotlib画图，还有最重要的机器学习，所以建议有兴趣的同学精读

### 2.3 卡尔曼卢滤波教程
* [rLabbe的Karlman Filters教程](https://github.com/rlabbe/Kalman-and-Bayesian-Filters-in-Python)
    * 注意：上面这个教程比较全面，建议有的放矢
* [图解卡尔曼滤波（英文）](http://www.bzarg.com/p/how-a-kalman-filter-works-in-pictures)
    * 强烈推荐：推荐的原因是把学习曲线比较陡的Kalman滤波给讲明白了
    * [图解卡尔曼滤波（中文翻译）](https://blog.csdn.net/u010720661/article/details/63253509)


## 3 关于Python的知识点：

### 3.1 矩阵操作的一些小例子（需要自己动手并实践）
```
import numpy as np 

list2d= [
    [1,2],
    [3,4],
    [5,6],    
]
array2d = np.array(list2d)
matrix2d = np.matrix(list2d)

# ========= #
print(list2d * 5)
print(array2d * 5)
print(matrix2d * 5)

# ========= #

# print(list2d + 3) # Error! 
print(list2d + [3])
print(array2d + 3)
print(array2d + [3])

# ========= #
print(np.matmul(array2d, array2d.T))
print(array2d.dot(array2d.T))
print(np.dot(array2d, array2d.T))
print(array2d @ array2d.T)
print(matrix2d @ matrix2d.T)

# --- but --- #
# print(array2d * array2d.T) # Error!!!
print(array2d * array2d) # Hadamard product (a.k.a entrywise product)
print(matrix2d * matrix2d.T) # still performing dot-product
```

### 3.2 “@”在函数定义的应用
在Python中，“@”表示一种Decorator（函数的装饰器），用了它就表示需要我们需要按照一种预定的方式去修改紧随其后的函数
具体可以以“Python decorator”关键字去Google搜索

### 3.3 List Comprehension列表推导式
（略）
