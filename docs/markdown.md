---
sidebar_position: 1
---

[教程](https://www.w3cschool.cn/markdownyfsm/ "Markdown 语法说明")

说明：
- 任意文本器都可以编写markdown
- 在线编辑器


### 标题
```markdown
atx 样式
# 一级标题 {#head1}
## 二级标题  {#head2}
### 三级标题  {#head3}
#### 四级标题  {#head4}
##### 五级标题  {#head5}
###### 六级标题 {#head6}

settext 样式
一级标题
=

二级标题
-
```

### 分割线
```markdown
***
---
___
```
效果：

***
---
___

### 引用
```markdown
> 引用内容
>> 引用内容
>>>引用内容
>>>>引用内容
```
效果：

> 引用内容
>> 引用内容
>>>引用内容
>>>>引用内容

### 高亮
```markdown
==高亮内容==
`你好`
```
效果：

==高亮内容==
`你好`

### 文本
```markdown
*斜体*  _斜体_  
**加粗**  __加粗__  
***斜体加粗***  ___斜体加粗___  
~~删除线~~  <u>下划线</u>  
H~2~O  X^2^
```
效果：

*斜体*  _斜体_  
**加粗**  __加粗__  
***斜体加粗***  ___斜体加粗___  
~~删除线~~  <u>下划线</u>  
H~2~O  X^2^

### 列表
```markdown
把大象放进冰箱需要几个步骤：
1. 打开冰箱
2. 把大象塞进去
3. 关上冰箱

无序列表：  
- 苹果
- 西瓜
* 柠檬
* 哈密瓜
+ 葡萄
+ 西瓜

1. 水果：  
    - 葡萄
    - 西瓜
2. 素菜：
    - 土豆
    - 西红柿
```
效果：

把大象放进冰箱需要几个步骤：
1. 打开冰箱
2. 把大象塞进去
3. 关上冰箱

无序列表：  
- 苹果
- 西瓜
* 柠檬
* 哈密瓜
+ 葡萄
+ 西瓜

1. 水果：  
    - 葡萄
    - 西瓜
2. 素菜：
    - 土豆
    - 西红柿

### 选择框
```markdown
明天要做得事情
- [ ] 吃饭
- [x] 睡觉
- [x] 打豆豆
```
效果：

明天要做得事情
- [ ] 吃饭
- [x] 睡觉
- [x] 打豆豆

### 表格
```markdown
|姓名(靠右)|年龄(居中)|成绩(靠左)|
|:-|:-:|-:|
|小明|18|90|
|小红|16|60|
```
效果：

|姓名(靠右)|年龄(居中)|成绩(靠左)|
|:-|:-:|-:|
|小明|18|90|
|小红|16|60|

### 脚注
```markdown
峨眉山 [^峨眉山] 月歌  
峨眉山月半轮秋 [^半轮秋]，影入平羌江水流。    
夜发清溪向三峡，思君不见下渝州。  

[^峨眉山]: 在今四川省峨眉山市西南，有两山峰相对，望之如蛾眉，故名。
[^半轮秋]: 谓秋夜的上弦月形似半个车轮。
```
效果：

峨眉山 [^峨眉山] 月歌  
峨眉山月半轮秋 [^半轮秋]，影入平羌江水流。    
夜发清溪向三峡，思君不见下渝州。  

[^峨眉山]: 在今四川省峨眉山市西南，有两山峰相对，望之如蛾眉，故名。
[^半轮秋]: 谓秋夜的上弦月形似半个车轮。

### 链接
```markdown
[菜鸟Markdown 教程](https://www.runoob.com/markdown/md-tutorial.html "Markdown 教程")

[菜鸟Markdown 教程][c]
[c]:https://www.runoob.com/markdown/md-tutorial.html "Markdown 教程"

URL:https://www.runoob.com/markdown/md-tutorial.html
  
<https://www.runoob.com/markdown/md-tutorial.html>
```
效果：

[菜鸟Markdown 教程](https://www.runoob.com/markdown/md-tutorial.html "Markdown 教程")

[菜鸟Markdown 教程][c]
[c]:https://www.runoob.com/markdown/md-tutorial.html "Markdown 教程"

URL:https://www.runoob.com/markdown/md-tutorial.html

<https://www.runoob.com/markdown/md-tutorial.html>

### 图片
```
![百度logo 图标](https://www.baidu.com/img/PCtm_d9c8750bed0b3c7d089fa7d55720d6cf.png "百度的logo")

<img decoding="async" title="百度的logo" src="https://www.baidu.com/img/PCtm_d9c8750bed0b3c7d089fa7d55720d6cf.png" width="20%" />
```
效果：
 
![百度logo 图标](https://www.baidu.com/img/PCtm_d9c8750bed0b3c7d089fa7d55720d6cf.png "百度的logo")

<img decoding="async" title="百度的logo" src="https://www.baidu.com/img/PCtm_d9c8750bed0b3c7d089fa7d55720d6cf.png" width="20%" />

