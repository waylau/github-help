GitHub Flavored Markdown
====

GitHub 使用 “GitHub Flavored Markdown” 或 GFM 在整个网站包括问题，评论，和请求。在一些重要的方面 它不同于标准的 Markdown (SM)，而且也增加了一些额外的功能。

如果你不熟悉 Markdown，查看[Markdown 基础](Markdown Basics.md)。如果你想了解更多功能关于提交问题，提供意见，提交请求描述，如任务列表等，请查阅[在 GitHub 上书写](Writing on GitHub.md)。

## 与传统  Markdown 不同之处

### 词中的多重下划线

在 Markdown 将下划线（_）为斜体，GFM 会忽略如下情况的下划线：

```
> wow_great_stuff
> do_this_and_do_that_and_another_thing.
```

这允许代码和名称强使用多个调下划线来了正确显示。要强调的一个字的一部分，使用星号（*）。

### URL 自动链接

GFM 将自动链接标准的URL，因此，如果你要链接到 URL （而不是设置链接文本），你可以简单地输入网址，它会变成一个链接到该网址:

```
http://example.com
```

将变成

http://example.com

### 删除线

GFM 增加了语法来创建删除线的文本，这是从标准的 Markdown 所没有的

```
~~Mistaken text.~~
```

变成

~~Mistaken text.~~


### 围栏代码块

标准 Markdown 转换开头是四个空格的文本每行成一个代码块; GFM 还支持围栏块。只是包装在你的代码```（如下图所示），您将不再需要通过四个空格缩进它。需要注意的是，虽然围代码块不必在前面加一个空行，不像缩进代码块，但建议您还是加上一个空行来更容易阅读。

	Here's an example:
	
	```
	function test() {
	  console.log("notice the blank line before this function?");
	}
	```

请记住，在列表中，您必须缩进非围栏代码块八个空格才能正确显示他们。

### 语法高亮

代码块可以再往前走一步，加入语法高亮。在您的围栏块，添加一个可选的语言标识，我们将通过语法高亮运行它。例如，语法高亮显示 Ruby 代码：

	```ruby
	require 'redcarpet'
	markdown = Redcarpet.new("Hello World!")
	puts markdown.to_html
	```
我们使用 [Linguist](https://github.com/github/linguist)来实现语法高亮，关键字的解析参见[语言 YAML 文件](https://github.com/github/linguist/blob/master/lib/linguist/languages.yml)

### 表格

可以通过组装一个单词列表，并将它们用 `-` （对第一行）进行分割，然后用每个`|`分离，实现创建表：

	First Header  | Second Header
	------------- | -------------
	Content Cell  | Content Cell
	Content Cell  | Content Cell

为了美观起见，您还可以在两端添加额外的 `|`：

	| First Header  | Second Header |
	| ------------- | ------------- |
	| Content Cell  | Content Cell  |
	| Content Cell  | Content Cell  |

注意，虚线上方不需要匹配标题文本的长度：

	| Name | Description          |
	| ------------- | ----------- |
	| Help      | Display the help window.|
	| Close     | Closes a window     |

你也可以包含 Markdown 的其他语法如链接，粗体，斜体，或删除线：

	| Name | Description          |
	| ------------- | ----------- |
	| Help      | ~~Display the~~ help window.|
	| Close     | _Closes_ a window     |

最后，通过包括冒号`：`在标题行中，您可以定义文本是左对齐，右对齐或居中对齐：

	| Left-Aligned  | Center Aligned  | Right Aligned |
	| :------------ |:---------------:| -----:|
	| col 3 is      | some wordy text | $1600 |
	| col 2 is      | centered        |   $12 |
	| zebra stripes | are neat        |    $1 |

`：`在最左边显示左对齐；`：`在最右边显示右对齐；`：`在两侧则显示中心对齐。

## HTML

您可以在 README 文件，问题和拉请求中使用 HTML 的一个子集。

我们支持的标记和属性的完整列表可以在 <https://github.com/github/markup> 标记库中找到。

## 扩展阅读

* [在 GitHub 上书写](Writing on GitHub.md)
*参考*：<https://help.github.com/articles/github-flavored-markdown/>

