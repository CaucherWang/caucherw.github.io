---
layout: wiki
title: C++__STL
categories: [Tools]
description: 收录一些基本STL方法
keywords: C++,STL
---

## 通用的成员函数

- size()：返回容器中元素数目
- swap()：交换两个容器的内容
- begin()：返回指向容器第一个元素的迭代器
- end()：返回一个表示容器尾的迭代器

## 非成员函数

<u>**需要包含头文件<algorithm>**</u>

- swap()：交换两个容器中的元素

- for_each()：遍历容器元素，用于替代for循环

  ```c++
  vector<int>v(10,1);
  for_each(v.begin(),v.end()-1,show);
  ```

  前两个参数为两个迭代器定义区间，最后一参数是函数对象，可以只接受一个int变量。

  

  ------

  类似的还有C++11中的基于范围的for循环

  ```c++
  vector<int>v(10,1);
  for(auto x:v)	
  {
  	show(x);
  	……
  }
  ```

  代码灵活性更高，坏处就是只能全部遍历一次

  ------

  

- random_shuffle()：乱序函数，使用这个函数，容器必须可以随机访问

  ```c++
  vector<int>v(10,1);
  random_shuffle(v.begin(),v.end()-2);
  ```

  将迭代器范围内的元素随机排列

- sort()：排序函数，使用这个函数，容器必须可以随机访问

  ```c++
  vector<int>v(10,1);
  sort(v.begin(),v.begin()+5);
  sort(v.begin()+5,v.end(),new_defined);
  ```

  - 用法一，容器内部元素必须可以进行<运算符的比较，内置也好，自己定义也罢；自己定义的类型，友元与否也不重要，只要能用<就可以
  - 用法二，自己定义一个函数，能够接受两个int类型变量，返回一个bool值