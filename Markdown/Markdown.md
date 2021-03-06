# Markdown语法
1-4是段落布局，5开始是文字修饰。  
确认一个普通段落是在尾部加两个空格。  
普通段落是不需要任何布局描述的，只有碰到代码、引用这样的特殊段落才需要描述一下这个段落的特殊性。  

----

1. 标题
2. 列表
3. 代码（兼文字强调）
4. 引用（兼段落强调）
5. 普通段落

## 1.标题
标题对内容做显式划分。  
快捷键是Ctrl+数字，最多到6。  
约定在标题前面放一个空行吧，标题后可以紧跟各种正文，因为不需要两个空格来确认段落。  
一级标题和二级标题除了用#之外，还可以在下面用=线或者-线来标记。  

### 三级标题
#### 四级标题
##### 五级标题
###### 六级标题

## 2.列表
- 无序列表
- 无序列表

----

1. 有序列表
2. 有序列表

----

- [ ] 复选框
- [x] 复选框

## 3.代码
行内代码：`var a=1`  
代码块：
```ruby
print 'hello world'
```
代码的本质是着色，所以常常用行内代码和引用两种描述来作为文字强调。加粗、斜体以及这里的两种底色是强调文字的常用手段。

## 4.引用
> 这是引用的文字  
> 引用内可以嵌套标题、列表等

## 5.强调
**粗体**  
*斜体*

## 6.图片
![描述](xxx.jpg)

## 7.链接
[描述](url)

## 8.表格
| Item     |    Value | Qty  |
| :------- | -------: | :--: |
| Computer | 1600 USD |  5   |

## 9.LaTex公式
行内公式：$ y=x+1 $
整行公式：$$ a^2+b^2=c^2 $$

## 10.目录
[TOC]

