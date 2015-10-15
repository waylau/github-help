在 GitHub 上书写
====

问题，评论和 pull 请求描述使用 GitHub 的 [GitHub Flavored Markdown](GitHub Flavored Markdown.md) 再加上一些额外的功能，使在 GitHub 上书写内容更加轻松。

## 标记

### 换行

与在 GitHub 上书写最大的区别就是我们处理换行符的方式。通过 Markdown，可以硬包装的文字段落，让他们结合成一个段落。我们认为这将导致巨大的意外格式错误。在评论，GitHub 对待段状内容换行就像是真正的换行符，这通常是你所希望的。

接下来的段落包含由一个换行符分隔两句话：

```
Roses are red
Violets are blue
```

变成 

Roses are red

Violets are blue

### 任务列表

列表可以通过加上前缀用[]或[X]（不完全或完全）列表中的项目变成任务列表。

```
- [x] @mentions, #refs, [links](), **formatting**, and <del>tags</del> are supported
- [x] list syntax is required (any unordered or ordered list supported)
- [x] this is a complete item
- [ ] this is an incomplete item
```


任务列表渲染所有评论和 Markdown 文件的复选框。选择或取消选择这些复选框在 GitHub 中标记为完全或不完全的。

任务列表可以嵌套到更好的结构中，任务列表：

```
- [ ] a bigger project
  - [ ] first subtask #1234
  - [ ] follow up subtask #4321
  - [ ] final subtask cc @mention
- [ ] a separate task
```

任务列表可以嵌套到任意深度的，尽管我们建议嵌套最多一次或两次;更复杂的任务应分解成单独的列表。

### 引用

某些引用是自动链接的：

```
* SHA: a5c3785ed8d6a35868bc169f07e40e889087fd2e
* User@SHA: jlord@a5c3785ed8d6a35868bc169f07e40e889087fd2e
* User/Repository@SHA: jlord/sheetsee.js@a5c3785ed8d6a35868bc169f07e40e889087fd2e
* #Num: #26
* GH-Num: GH-26
* User#Num: jlord#26
* User/Repository#Num: jlord/sheetsee.js#26
```

变成

* SHA: a5c3785ed8d6a35868bc169f07e40e889087fd2e
* User@SHA: jlord@a5c3785ed8d6a35868bc169f07e40e889087fd2e
* User/Repository@SHA: jlord/sheetsee.js@a5c3785ed8d6a35868bc169f07e40e889087fd2e
* #Num: #26
* GH-Num: GH-26
* User#Num: jlord#26
* User/Repository#Num: jlord/sheetsee.js#26

## 特性

### 快速引用

在键盘上输入 `r` 可以让你用评论来回复到当前的问题，或者请求。你选择的任何文本在讨论线程之前按下R将自动添加到您的评论并格式化为一个引用。

### 名称和团队用 @ 自动补齐

输入一个`@`符号将出现的人或团队名单上的项目。这份名单是根据您的输入来过滤的，所以一旦你找到你要找的，你可以使用箭头键选择它，同时按下任一选项卡或输入来完成这个名字的人或团队的名字。对于团队，只要输入`@`组织/团队名和团队的所有成员将获得订阅的问题。

自动完成结果仅限于存储库的合作者和线程上任何其他参与者，所以它不是一个完整的全局搜索。它使用相同的模糊过滤器作为文件查找器，并同时适用于用户名和全名。

博客文章有关`@` 自动补齐，请参阅[用户](https://github.com/blog/1004-mention-autocompletion)和[团队](https://github.com/blog/1121-introducing-team-mentions)的更多信息。

### 表情符号自动完成

键入`：`将弹出提示表情符号列表。该列表将根据你的输入来过滤，所以一旦你找到你要找的，按`Tab`键或`Enter`键完成突出显示表情符号的结果。有关可用表情符号的完整列表，请参阅[emoji-cheat-sheet.com](http://emoji-cheat-sheet.com/)。

### 问题自动完成

键入`＃`将弹出提示问题的列表，并 Pull请求。键入数字或一些文字过滤列表，然后点击任一选项卡或输入完成高亮显示的结果。

## 更多可见

* [Markdown Basics 关于 Markdown 的基础](Markdown Basics.md)
* [GitHub Flavored Markdown](GitHub Flavored Markdown.md)

*参考*：<https://help.github.com/articles/writing-on-github>