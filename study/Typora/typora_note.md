

#源代码模式

```markdown
ctrl + /
```



# Typora的各种链接跳转

[点击这里](https://blog.csdn.net/qq_41907769/article/details/121722716)

# 标题

```markdown
# 一级标题
## 二级标题
### 三级标题
```



# 引用

```markdown
> 一级引用
>> 二级引用
```



# 列表

```markdown
无序列表
* content 1
* content 2
* content 3
有序列表
1. content 1
2. content 2
3. content 3
```



# 任务列表

```markdown
- [ ] a task list item
- [ ] list syntax required
- [ ] normal **formatting**, @mentions, #1234 refs
- [ ] incomplete
- [x] completed
```



# 代码块

```markdown
Here's an example:

​```
function test() {
  console.log("notice the blank line before this function?");
}
​```

syntax highlighting:
​```ruby
require 'redcarpet'
markdown = Redcarpet.new("Hello World!")
puts markdown.to_html
​```
```



# 数学公式

```markdown
$$
\mathbf{V}_1 \times \mathbf{V}_2 =  \begin{vmatrix}
\mathbf{i} & \mathbf{j} & \mathbf{k} \\
\frac{\partial X}{\partial u} &  \frac{\partial Y}{\partial u} & 0 \\
\frac{\partial X}{\partial v} &  \frac{\partial Y}{\partial v} & 0 \\
\end{vmatrix}
$$
```



# 表格

## 建表格式

```markdown
| First Header  | Second Header |
| ------------- | ------------- |
| Content Cell  | Content Cell  |
| Content Cell  | Content Cell  |
```

| First Header | Second Header |
| :----------- | ------------- |
|              |               |

## 左右对齐

```markdown
| Left-Aligned  | Center Aligned  | Right Aligned |
| :------------ |:---------------:| -----:|
| col 3 is      | some wordy text | $1600 |
| col 2 is      | centered        |   $12 |
| zebra stripes | are neat        |    $1 |
```

| First Header | Second Header |
| :----------: | :-----------: |
|              |               |



# 下标

```markdown
You can create footnotes like this[^footnote].

[^footnote]: Here is the *text* of the **footnote**.
```

You can create footnotes like this [^footnote].

[^footnote]: Here is the *text* of the **footnote**.



# 水平线

```markdown
--- + enter
```

---



# 添加目录

```markdown
[toc] + enter
```

[toc]

# 扩展元素

##超链接

```markdown
This is [an example](http://example.com/ "Title") inline link.

[This link](http://example.net/) has no title attribute.
```

This is [an example](https://baidu.com) inline link.

[This link](http://baidu.com) has no title attribute.

## 跳转到文件

[跳转到typora_note](typora_note)

## 跳转到网站

```markdown
This is [an example][id] reference-style link.

Then, anywhere in the document, you define your link label on a line by itself like this:

[id]: http://example.com/  "Optional Title Here"
```

This is  [an example][id]

[id]:  https://www.baidu.com/

```markdown
[Google][]
And then define the link:

[Google]: http://google.com/
```

[Google][]

[Google]: http://google.com/

## 图片

```markdown
![Alt text](/path/to/img.jpg)

![Alt text](/path/to/img.jpg "Optional title")
```

<img src="typora_note.assets/QQ图片20220314224809.jpg" alt="alt" style="zoom:50%;" />

## 强调

```markdown
*single asterisks*

_single underscores_
```

*single asterisks*

_single asterisks_

```markdown
\*this text is surrounded by literal asterisks\*
```

\*this text is surrounded by literal asterisks\*



## 代码

``` markdown
Use the `printf()` function.
```

C++ use `sort()` function to sort element



## 划线

`This is a mistake`~~This is a mistake~~



## 表情

:smile:

:cry:



## 内联公式和其他

H~2~O

X^2^

==highlight==

<video src="xxx.mp4" />

















