---
layout: wiki
title: C++__string
categories: [Tools]
description: 收录一些常用的string方法和属性
keywords: C++,string
---

- 取子串类方法:substr

  ```c++
  return s.substr(start, length)
  ```

  第一个形参表示开始的索引，第二个表示子串长度
  
- 删除方法：erase

  ```c++
  string x="Fudan";
  x.erase(x.begin());	//删除第一个元素
  x.erase();	//删空
  x.erase(3);	//从第三个位置开始，往后删空
  x.erase(3,2);	//从第三个位置开始，删除两个元素
  x.erase(x.begin()+1,x.end()-1);	//按迭代器范围，左闭右开，删除
  ```

- 增补方法：append

  ```c++
  string a="Fudan",b="University";
  char *x="Zhangjiang";
  a.append(x);
  a.append(x,5);	//只加C字符串的前几个字符
  a.append(b);
  a.append(b,6,4);	//从第六个位置，长度为4
  a.append(b.begin()+6,b.end());
  a.append(2,'!');	//添加多个单字符
  ```

  