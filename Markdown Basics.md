关于 Markdown 的基础
====

[Markdown](http://daringfireball.net/projects/markdown/) 允许您编写使用易于阅读,易于编写的纯文本格式,然后转化成有效的 HTML 用于在 GitHub 上查看。

## 基本写法

### 段落

段落在 Markdown 只是连续的一行或多行文本后面跟着一个或多个空行。

```
On July 2, an alien mothership entered Earth's orbit and deployed several dozen saucer-shaped "destroyer" spacecraft, each 15 miles (24 km) wide.

On July 3, the Black Knights, a squadron of Marine Corps F/A-18 Hornets, participated in an assault on a destroyer near the city of Los Angeles.
```

### 标题

您可以创建一个标题通过添加一个或多个 `#` 符号在你的标题文本中。你使用的 `#` 数量将决定标题的大小。

```
# The largest heading (an <h1> tag)
## The second largest heading (an <h2> tag)
…
###### The 6th largest heading (an <h6> tag)
```

### 引用

你可以用 `>` 表示[引用](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/blockquote)

```
In the words of Abraham Lincoln:

> Pardon my french
```

### 样式文本

你可以使文本[粗体](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/strong)或[斜体](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/em)

```
*This text will be italic*
**This text will be bold**
```

粗体和斜体都可以使用`*`或`_`在文本样式。这允许您如果需要结合粗体和斜体。

```
**Everyone _must_ attend the meeting at 5 o'clock today.**
```

## 列表

### 无序列表

你可以做一个无序列表通过前面的列表项`*`或`-`

```
* Item
* Item
* Item

- Item
- Item
- Item
```

### 有序列表

你可以有序列表通过前面的列表项一个数字

```
1. Item 1
2. Item 2
3. Item 3
```

### 嵌套列表

您可以创建嵌套列表由两个空格缩进列表项

```
1. Item 1
  1. A corollary to the above item.
  2. Yet another point to consider.
2. Item 2
  * A corollary that does not need to be ordered.
    * This is indented four spaces, because it's two spaces further than the item above.
    * You might want to consider making a new list.
3. Item 3
```

## 代码格式化

### 内联格式

使用单引号(`)格式文本在一个特殊的等宽字体格式

```
Here's an idea: why don't we take `SuperiorProject` and turn it into `**Reasonable**Project`.
```

### 多行

使用 (```) 格式来表示多行

	Check out this neat program I wrote:
	
	```
	x = 0
	x = 2 + 2
	what is x
	```
###　链接

链接的文本放在方括号([]),然后把链接在括号(())。

例如,创建一个链接到<http://www.waylau.com>的链接文本,你会写成:

	[访问 Waylau's Peronal Blog](http://www.waylau.com)
### 也可以看

* [GitHub Flavored Markdown](GitHub Flavored Markdown.md)
* [Writing on GitHub](Writing on GitHub.md)
* [Mastering Markdown](https://guides.github.com/features/mastering-markdown/)



*参考*：<https://help.github.com/articles/markdown-basics/>