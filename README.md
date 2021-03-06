# 正交测试用例生成工具
该软件的主要功能为生成正交表设计测试用例。用户可以按照输入规范(正文会给出)输入水平数和因子数，根据查询的正交表生成相对应的正交表设计测试用例。

具体正交表信息可以查看软件根目录的ts723_Designs.txt文件，或者直接查询http://support.sas.com/techsup/technote/ts723_Designs.txt。

# 内容列表

- [软件介绍](#软件介绍)

- [安装](#安装)

- [使用说明](#使用说明)

  - [输入规范](#输入规范)
  - [操作示范](#操作示范)
  - [没有对应正交表情况处理](#没有对应正交表情况处理)

- [维护者](#维护者)
# 背景
`正交测试用例生成工具`的软件目的是为了节省测试人员设计用例时查询正交表的时间，该软件的主要功能为生成正交表设计测试用例。用户可以按照输入规范(正文会给出)输入水平数和因子数，根据查询的正交表生成相对应的正交表设计测试用例。
具体正交表信息可以查看软件根目录的ts723_Designs.txt文件，或者直接查询
[此处](http://support.sas.com/techsup/technote/ts723_Designs.txt)

# 安装

该仓库为软件源码，可直接运行bin目录下的exe文件，或者使用vs2019打开

# 使用说明

为了能够成功生成测试用例，需要按照输入规范输入水平数和因子数

## 输入规范

`[因素]:[水平1],[水平2]...[水平n] (回车换行,写下个因素,注意尽量用英文标点符号)`

例如

```
a:a0,a1,a2
b:b0,b1,b2
c:c0,c1,c2
d:d0,d1,d2
```

## 操作示范

第一步，按照输入规范，输入水平数和因子数，此次示范输入为

```
a:a0,a1,a2,a3
b:b0,b1,b2,b3
c:c0,c1,c2,c3
d:d0,d1,d2,d3
e:e0,e1,e2,e3
f:f0,f1,f2,f3
g:g0,g1,g2,g3
h:h0,h1,h2,h3
i:i0,i1,i2,i3
j:j0,j1,j2,j3
k:k0,k1,k2,k3
l:l0,l1,l2,l3,l4,l5,l6,l7,l8,l9,l10,l11
m:m0,m1,m2,m3,m4,m5,m6,m7,m8,m9,m10,m11
```



![输入](https://github.com/yescco126/Orthogonal-Form-tool/raw/master/images/input.png)

第二步，点击生成按钮，生成测试用例

![结果](https://github.com/yescco126/Orthogonal-Form-tool/raw/master/images/result.png)

## 没有对应正交表情况处理

如果输入水平数或因子数没有对应的正交表(输入的水平数或因子数与正交表的水平数或因子数不相等)，则会显示“没有对应正交表的情况”。例如输入:

```
操作系统:2000,XP,2003
浏览器:IE6.0,IE7.0,TT
杀毒软件:卡巴,金山,诺顿
```

提示出现

![提示](https://github.com/yescco126/Orthogonal-Form-tool/raw/master/images/tip.png)

此时可用正交表的因子数或水平数大于输入的因子数或水平数的正交表，例如

```
操作系统:2000,XP,2003
浏览器:IE6.0,IE7.0,TT
杀毒软件:卡巴,金山,诺顿
:,,
```

此时结果为

![修改后](https://github.com/yescco126/Orthogonal-Form-tool/raw/master/images/after.png)

# 维护者

[@yescco](https://github.com/yescco126)








