---
layout: post
title: MD文件格式范例
category: 学习
keywords: 例子，MD
---


This article has summarized the common MD(Markdown) grammar for reference.

****
## Contents

* [Title](#Title)
* [Text](#Text)
    * normal text
    * single line
    * multiple lines
    * highlight
    * new line command
    * Itatic, bold & delete line
* [Table & List](#Table & List)
* [Block](#Block)
* [Code](#Code)

## Title
------
# Level 1  
## Level 2  
### Level 3  
#### level 4  
##### level 5  
###### level 6  

##Text
------
### Normal text
This is an example of the normal text.  
### Single line text
	This is a single line text  
Input one tab or 4 spaces at the start of the text. 

### Multiple lines
Input one tab or 4 spaces at the start of each line.  
	Welcome
	Nice to meet you
	Best Wishes

### Text highlight
use a pair of apostrophe  
`linux` `lammps` 
suitable for displaying as tags of an article 

#### New line command
we can create a new line by entering two spaces after the end of the last sentence 

It can also be done by leaving a blank line between two texts, but the distance is a bit larger than the former method. 

#### Italic, bold & delete line
| grammar                          |                         output |
| :------------------------------- | -----------------------------: |
| `*Italic1*`                      |                      *Italic1* |
| `_Italic2_`                      |                      _Italic2_ |
| `**bold1**`                      |                      **bold1** |
| `__bold2__`                      |                      __bold2__ |
| `This is a ~~delete~~`           |           This is a ~~delete~~ |
| `***Italic bold 1***`            |            ***Italic bold 1*** |
| `___Italic bold 2___`            |            ___Italic bold 2___ |
| `***~~Italic bold delete 1~~***` | ***~~Italic bold delete 1~~*** |
| `~~***Italic bold delete 2***~~` | ~~***Italic bold delete 2***~~ |


## List
### Unordered list
* Nickname: Jay
- Official name: Jian
* English name: Jay

### Multi-level unordered list
* Programming language
    * Script tools
        * Python

### Ordered list
#### Normal type
Number + point + space:  
1. Clarify
2. Verify
3. Modify


#### Multi-level ordered list
1. level 1
   1. level 2
      1. Level 3

### Special type

- [x] Non-dimensional analysis
- [x] Grid setup
- [x] Algorithm design
- [ ] Coding
- [ ] Debuging
- [ ] Validation

> Tip:
> > This function can be used to label the work which has been done

## Block

### 常用于引用文本
#### 文本摘自《深入理解计算机系统》P27
　令人吃惊的是，在哪种字节顺序是合适的这个问题上，人们表现得非常情绪化。实际上术语“little endian”（小端）和“big endian”（大端）出自Jonathan Swift的《格利佛游记》一书，其中交战的两个派别无法就应该从哪一端打开一个半熟的鸡蛋达成一致。因此，争论沦为关于社会政治的争论。只要选择了一种规则并且始终如一的坚持，其实对于哪种字节排序的选择都是任意的。
> **“端”（endian）的起源**  
> 以下是Jonathan Swift在1726年关于大小端之争历史的描述：  
> “……下面我要告诉你的是，Lilliput和Blefuscu这两大强国在过去36个月里一直在苦战。战争开始是由于以下的原因：我们大家都认为，吃鸡蛋前，原始的方法是打破鸡蛋较大的一端，可是当今的皇帝的祖父小时候吃鸡蛋，一次按古法打鸡蛋时碰巧将一个手指弄破了，因此他的父亲，当时的皇帝，就下了一道敕令，命令全体臣民吃鸡蛋时打破较小的一端，违令者重罚。”

### Multi-structure block
> Hydrodynamics
> > Stable case
> > > High Reynolds number case
> > > > Turbulence model
> > > > > K-epsilon model, SA model

代码高亮
----------
在三个反引号后面加上编程语言的名字，另起一行开始写代码，最后一行再加上三个反引号。
```Java
public static void main(String[]args){} //Java
```
```c
int main(int argc, char *argv[]) //C
```
```Bash
echo "hello GitHub" #Bash
```
```javascript
document.getElementById("myH1").innerHTML="Welcome to my Homepage"; //javascipt
```
```cpp
string &operator+(const string& A,const string& B) //cpp
```
表格
--------

| 表头1  | 表头2  |      |
| ---- | ---- | ---- |
| 表格单元 | 表格单元 |      |
| 表格单元 | 表格单元 |      |

| 表头1  | 表头2  |
| ---- | ---- |
| 表格单元 | 表格单元 |
| 表格单元 | 表格单元 |

### 对齐
表格可以指定对齐方式

| 左对齐           |       居中        |   右对齐 |
| :------------ | :-------------: | ----: |
| col 3 is      | some wordy text | $1600 |
| col 2 is      |    centered     |   $12 |
| zebra stripes |    are neat     |    $1 |

### 混合其他语法
表格单元中的内容可以和其他大多数GFM语法配合使用，如：  
#### 使用普通文本的删除线，斜体等效果

| 名字    | 描述                           |
| ----- | ---------------------------- |
| Help  | ~~Display the~~ help window. |
| Close | _Closes_ a window            |

#### 表格中嵌入图片（链接）
其实前面介绍图片显示、图片链接的时候为了清晰就是放在在表格中显示的。

| 图片                   | 描述   |
| -------------------- | ---- |
| ![baidu][baidu-logo] | 百度   |




