# markdownpad简明使用教程 #
## 标题 ##
	## 二级标题（ctrl+2） ##
	### 三级标题（ctrl+3） ###
## 列表 ##
### 有序列表 ###
1. 有序列表（Ctrl+shift+o）
2. 在文字前加上1. 2. 3.（注意与文字间要加空格）
### 无序列表 ###
- 无序列表（ctrl+u）
- 在文字前加上-或者*（注意与文字间要加空格）
## 引用 ##
> 使用引用
> 在文字前加上>（注意与文字间要加空格）
> CTRL+Q
## 图片与链接 ##
- 图片为：!()[]
- 链接为: ()[]
- 图片 （CTRL+g）
- 链接 （CTRL+l）
- eg:[美女图片](http://baidu.com)
- [pdf](file:///C:/Users/Administrator/Desktop/markdownpad简明教程.html)
- ![c](C:\Users\Administrator\Desktop\2.jpg)
## 粗体与斜体 ##
1. 粗体
	- 两个*包含一段文本
	- **粗体**
	- CTRL+B
2. 斜体
	- 一个*包含一段文本
	- *斜体*
	- CTRL+I
## 代码框 ##
- 用```包含文本
- ```public static main(String[] args) ```
- CTRL+k
## 横线 ##
- 用三个*号
***
## 转义字符 ##
- \

## 流程图 ##
```flow
st=>start: 开始|past:>http://www.google.com[blank]
e=>end: 结束:>http://www.google.com
op1=>operation: 操作1|past
op2=>operation: 操作2|current
sub1=>subroutine: My Subroutine（子程序）|invalid
cond=>condition: Yes or No?|approved:>http://www.google.com
c2=>condition: 是否号idea|rejected
io=>inputoutput: catch something…|request

st->op1(right)->cond
cond(yes, right)->c2l
cond(no)->sub1(left)->op1
c2(yes)->io->e
c2(no)->op2->e
```
```sequence
Andrew->China: Says Hello
Note right of China: China thinks\nabout it
China-->Andrew: How are you?
Andrew->>China: I am good thanks!
```
