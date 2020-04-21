#  Markdown基本语法学习笔记

# 写在前面

这是一篇关于Markdown的~~科（扫）普（盲）推文~~学习笔记。

[Markdown](https://zh.wikipedia.org/wiki/Markdown)是一种轻量级标记语言，允许用户使用易读易写的纯文本格式编写文档，支持即时渲染技术。Markdown语言由[John Gruber]([https://zh.wikipedia.org/wiki/%E7%B4%84%E7%BF%B0%C2%B7%E6%A0%BC%E9%AD%AF%E4%BC%AF](https://zh.wikipedia.org/wiki/約翰·格魯伯))于2004年创建，其编写的文档后缀名为`.md`.和`.markdown`格式。

***

[toc]

##  1 基本操作

###  1.1 标题

用`#`表示标题，一级标题对应一个`#`号，二级标题对应两个`#`号，最多至六级标题。也可使用快捷键`Ctrl+1`表示一级标题，依次类推。

### 1.2 目录

用`[toc]`语法生成内容目录。

### 1.3 字体

+ 斜体：`*斜体*`或`_斜体_`或`ctrl+I`快捷键
+ 加粗：`**加粗**`或`__加粗__`或`ctrl+B`快捷键
+ 粗斜体：`***粗斜体***`，`___粗斜体___`或`ctrl+B与ctrl+I`
+ 字体大小：`<font size=5>我是5号字体</font>`
+ 字体颜色：`<font color=red>我是红色字体</font>`
+ 字体类型：`<font face="黑体">我是黑体</font>`
+ 高亮：`==我是高亮字体==`
+ 下划线：`<u>我是字体下划线</u>`或`ctrl+U`快捷键
+ 删除线：`~~我是字体删除线~~`
+ 分割线：`***`或`---`或`___`
+ 居中：`<center>我是居中字体</center>`
+ 脚注：`Markdown[^1]` <br>           `[^1] A simple language`
+ 上标：`$x^2$`表示$x^2$
+ 下标：`$S_n$`表示$S_n$，`$S_{n-1}$`表示$S_{n-1}$

### 1.4 列表

#### 1.4.1 无序列表

用`*`，`+`或`-`表示无序列表，标记符号后**添加一个空格**，利用`Tab键`进行列表嵌套。

#### 1.4.2 有序列表

用**数字加`.`再加空格**表示有序列列表，利用`Tab键`进行列表嵌套。

#### 1.4.3 任务列表

+ 基本语法：

```
-[ ] 摄影
-[x] 看书
-[ ] 运动
```

需要特别注意的是：<font color=red>**每个符号之间均有一个空格**。</font>

+ 效果：

- [ ] 摄影
- [x] 看书 
- [ ] 运动

### 1.5 区块

使用**`>`加空格**来表示区块，用于引用别人的文章内容。例如：

> 这里是引用内容
>
> 这里是引用内容
>
> 这里是引用内容

### 1.6 超链接

用`[链接文字](链接地址)`或`<超链接地址>`两种语法表示超链接，也可使用快捷键`ctrl+K`。例如：

```
[百度](https://www.baidu.com/)
<https://www.baidu.com/>
```

效果如下：

[百度](https://www.baidu.com/)

<https://www.baidu.com/>

### 1.7 符号的输入

使用转义字符`\`输入符号，基本语法如下：

```
\\         反斜线
\`         反引号
\*         星号
\_         下划线
\{ \}      花括号
\[ \]      方括号
\( \)      括弧
\#         井号
\+         加号
\-         减号
\.         英文句点
\!         惊叹号
```

### 1.8 特殊符号

```
&copy;      版权      
&reg;       注册商标
&trade;     商标
&nbsp;      空格
&amp;       和号
&quot;      引号
&apos;      撇号
&lt;        小于号
&gt;        大于号
&ne;        不等号
&le;        小于等于
&ge;        大于等于
&cent;      分
&pound;     磅
&euro;      欧元
&yen;       元
&sect;      节
&times;     乘号
&divide;    除号
&plusmn;    正负号
```

## 2 代码

### 2.1 单行代码

+ 语法：代码之间使用一对反引号即可表示代码。例如：

```
`print("Hello World!")`
```

+ 效果：

`pirnt("Hello World!")`

### 2.2 多行代码

+ 语法：使用三个~或三个反引号将代码块包起来。例如：

```
~~~代码区域~~~ 或 ```代码区域```
```

+ 效果：

```python
import numpy as np
import matplotlib.pyplot as plt
np.random.seed(100)  #生成一组随机数据
data = np.random.normal(size = (1000,4),loc = 0,scale = 1)
labels = ['A','B','C','D']
# 创建一个4×1000的数组，即有4组数据，每一组数据有1000个数据，各组名称依次为A,B,C,D。
plt.boxplot(data,labels = labels)
plt.show()
```

## 3 表格

Markdown使用`|`分割不同的单元格，使用`-`分割表头和其他行，分别用`:-`、`-:`和`:-:`表示左对齐、右对齐和居中。 也可使用快捷键`ctrl+T`直接生成表格。

+ 语法：

```
|英雄|属性|能量|阵营|身份|
|:-:|:--:|:-:|:--|:--|
|周瑜|法师|魔道|吴|吴地都督|
|妲己|法师|魔道|倒悬天|姜子牙所造人偶|
|牛魔|辅助|武道|日之塔|魔种起义军叛徒|
|钟无艳|战士|武道|稷下学院|稷下学生|
|兰陵王|刺客|武道|金庭国|金庭城王子|
```

+ 效果：

|  英雄  | 属性 | 能量 | 阵营     | 身份           |
| :----: | :--: | :--: | :------- | :------------- |
|  周瑜  | 法师 | 魔道 | 吴       | 吴地都督       |
|  妲己  | 法师 | 魔道 | 倒悬天   | 姜子牙所造人偶 |
|  牛魔  | 辅助 | 武道 | 日之塔   | 魔种起义军叛徒 |
| 钟无艳 | 战士 | 武道 | 稷下学院 | 稷下学生       |
| 兰陵王 | 刺客 | 武道 | 金庭国   | 金庭城王子     |

## 4 图片

Markdown插入图片的基本语法为：`![图片alt 属性文本](图片地址 "可选标题")`，使用`style="zoom:25%`缩放图片。实际中可直接用`ctrl+C`与`ctrl+V`进行复制粘贴。图片alt为显示在图片下面的文字，用于解释图片内容。图片title为图片的标题，当鼠标移到图片上时显示的内容。

## 5 常见数学公式

插入数学公式的语法包括两种：

+ 行内公式（内联公式）：`$数学公式$`
+ 行间公式（外联公式），单独占据一行或数行并居中显示，行间换行使用`\\`：

```
$$
数学公式
$$
```

### 5.1 上标下标

同1.3 字体中的上下标，这里不再赘述。

### 5.2 根号

用`\sqrt[]{}`表示根号。例如，`$\sqrt{2},\sqrt[3]{5}$`表示$\sqrt{2}$，$\sqrt[3]{5}$。

### 5.3 向量符号

用`\vec{}`表示单个字母向量，用`$\overrightarrow{}$`和`$\overleftarrow{}$`表示从A到B的向量。例如，`$\vec{a}$`表示$\vec{a}$，`$\overrightarrow{AB}$`表示$\overrightarrow{AB}$，`$\overleftarrow{AB}$`表示$\overleftarrow{AB}$。

### 5.4 分数

用`\frac{}{}`表示分数。例如，`$\frac{\sqrt{3}}{4}$`表示$\frac{\sqrt{3}}{4}$。

### 5.5 括号

`$\{ \}$`：$\{ \}$

`${a \choose b}$`：${a \choose b}$

### 5.6 微积分

`$\int_0^2 x^2 {\rm d}x$`：$\int_0^2 x^2 {\rm d}x$

`$\lim\limits_{n \rightarrow +\infty} \frac{1}{n(n+1)}$`：$\lim\limits_{n \rightarrow +\infty} \frac{1}{n(n+1)}$

### 5.7 求和与连乘

`$\sum_{i=0}^n \frac{1}{i^2}$`：$\sum_{i=0}^n \frac{1}{i^2}$

`$\sum_{i=1}^{10}x_i$`：$\sum_{i=1}^{10}x_i$

`$\prod_{i=1}^{n-1}x_i$`：$\prod_{i=1}^{n-1}x_i$

### 5.8 希腊字母

```
$$
\alpha \beta \gamma \Gamma \delta \Delta \epsilon \varepsilon \zeta \eta \theta \Theta \vartheta \iota \kappa \lambda \Lambda \mu \nu \xi \Xi \pi \Pi \varpi \rho \varrho \sigma \Sigma \varsigma \tau \upsilon \Upsilon \phi \Phi \varphi \chi \psi \Psi \Omega \omega
$$
```

$$
\alpha \beta \gamma \Gamma \delta \Delta \epsilon \varepsilon \zeta \eta \theta \Theta \vartheta \iota \kappa \lambda \Lambda \mu \nu \xi \Xi \pi \Pi \varpi \rho \varrho \sigma \Sigma \varsigma \tau \upsilon \Upsilon \phi \Phi \varphi \chi \psi \Psi \Omega \omega
$$

注：其余数学公式参考[LaTeX official Core Documentation](https://www.latex-project.org/help/documentation/#general-documentation)。

