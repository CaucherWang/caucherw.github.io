---
layout: wiki
title: C++__vector
categories: [Tools]
description: 收录一些常用的vector方法和属性
keywords: C++,vector
---

- 二维数组初始化办法

  ```C++
  vector<vector<bool>>dp(len, vector<bool>(len));
  ```

  第一个形参是size，第二个形参是值，这里用了匿名变量
  
- 删除指定区间（左闭右开）的元素

  ```c++
  vector<int>ve(10,1);
  ve.erase(ve.begin()+2,ve.begin()+5);
  ```

  删除了vector的第三个元素、第四个元素和第五个元素

- 插入一些元素（一般都是同类型STL互相添加）

  ```
  vector<int>old(10,1);
  vector<int>new(10,2);
  old.insert(old.begin()+2,new.begin()+1,new.begin()+3);
  ```

  从old第三个位置开始，把new的从第二个元素到第三个元素添加进去

