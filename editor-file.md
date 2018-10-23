# 编辑技巧

## 光标大范围移动

* 使用 `command + 方向键上` 移动到文件顶部。
* 使用 `command + 方向键下` 移动到文件顶部。
* 使用 `command + 方向键左` 移动到当前行头。
* 使用 `command + 方向键右` 移动到当前行尾。

## 光标单词移动

* 使用 `alt + 方向键左` 可以移动到词首。
* 使用 `alt + 方向键右` 可以移动到词尾。

## 光标变量名中单词移动

在单词移动中 helloWorld、hello_world、HelloWorld 这类单词会被当做一个整体。当需要做到移动到 hello尾部 或者 移动到 world 的头部，使用 `control + alt + 方向键左或右` 可以完成。

## 多行编辑

* 使用 `alt + 鼠标点击` 可以同时选择多个编辑点进行编辑。
* 选中需要编辑的单词，使用 `command + d` 可以选择文件中出现相同单词的文本同时进行编辑。
* 使用 `command + alt + 方向键上或下` 可以选择多行进行编辑。

## 多行编辑到行尾

使用多行编辑的时候可以搭配 `大范围移动`、`单词移动`、`变量名中单词移动` 来快速进行代码光标的移动，如果是需要同时移动到行尾除了使用 `command + 方向键右` 也可以使用 `shift + alt + i`。

## 行操作

* 使用 `shift + alt + 方向键上或下` 可以快速的复制当前行。
* 使用 `command + shift + enter` 在光标当前行上创建空行。
* 使用 `command + enter` 在光标当前行下创建空行。
* 使用 `command + i` 选中当前行。
* 使用 `command + x` 剪切当前行。
* 使用 `command + shift + k` 删除当前行。
* 使用 `control + j` 合并当前行。
* 使用 `command + [ 或 ]` 代码向前或向后缩进。

## 选择操作

* 按住 `shift` 搭配 `大范围移动`、`单词移动`、`变量名中单词移动` 中的快捷键可以快速的进行内容的选择。
* 使用 `shift + 方向键上` 选中光标后面到上一行所有内容。
* 使用 `shift + 方向键下` 选中光标后面到下一行所有内容。
* 使用 `shift + 方向键左` 选中光标左边一个字符。
* 使用 `shift + 方向键右` 选中光标右边一个字符。
* 使用 `command + ctrl + shift + 方向键右` 扩大选中范围内的代码块。
* 使用 `command + ctrl + shift + 方向键右` 缩小选中范围内的代码块。

## 代码块操作

* 按住 `command + alt + [ 或者 ]` 可以对代码进行折叠、展开操作。
* 按住 `command + k + [ 或者 ]` 可以对代码进行递归折叠、递归展开操作。
* 按住 `command + k + 0` 可以折叠当前所有代码块。
* 按住 `command + k + j` 可以展开当前所有代码块。

## 错误修复

编辑器会对一些代码语法错误以 `红色波浪线` 进行提示，可以使用 `commnad + .` 来进行 文件导入、代码纠错等修复，装上一些语言相关扩展可以使得功能变得更加强大。

## 代码查看与引用

在编辑代码或者阅读源码的时候经常需要查看 源码 或者 引用。使用 `alt + F12` 可以方便的查看当前类或者方法的定义。如果想更详细的阅读代码可以使用 `alt + 右键点击` 类或者方法名可以快速进入对应的源码中。

如果需要查看整个项目中 引用或者使用 这个类的地方，我们除了使用 `command + shift + f` 进行关键词搜索，也可以使用 `shift + F12` 会出现一个更加友好的对话框查看相关引用。

## 格式化代码

使用 `shift + alt + f` 可以对代码进行格式化。