# EditorConfig - 编辑规范配置工具

## 简介

经常在项目合作开发中，由于没有统一规范、开发者各自的编辑器配置不一样、不同项目、不同语言在代码格式上经常有所不同要求，会导致代码没有一个统一的格式，可能会造成代码在阅读的时候样式出现没有进行对齐和格式。

使用`EditorConfig`可以对全局的文件、单独的语言、单独的文件进行对应的设置。除了自己设置以外`EditorConfig`还提供了一系列的知名开源项目的配置，可以到 github [传送门](https://github.com/editorconfig/editorconfig/wiki/Projects-Using-EditorConfig) 进行参考。

## 安装

使用`command + shift + x`打开扩展，搜索`EditorConfig for Visual Studio Code`插件并安装后重启编辑器。

## 资源

* [官方网站](https://github.com/editorconfig/editorconfig/)

## 使用

当编辑某一个文件时EditorConfig通过读取`.editorconfig`中的配置的规则来对代码进行格式化，读取的过程会一直往上层目录搜索直到找到`.editorconfig`中配置了`root = true` 为止。越接近的`.editorconfig`配置优先级别越高。`.editorconfig` 使用 ini 格式。

#### 通配符
* `*` 匹配任意多个字符 '/' 除外。
* `**` 匹配任意多个字符。
* `?` 匹配任意单个字符。
* `[pushmetop]` 匹配 pushmetop 中所包含的任一字符。
* `[!pushmetop]` 匹配 pushmetop 中所不包含的任一字符。
* `{s1,s2,s3}` 匹配其中任一字符串的字符（`,`为分隔符号）。

#### 配置属性

* `root` 用于设置项目根目录，可选值`true|false`。
* `indent_style` 用于配置缩进使用`tab` 或者`space`，可选值`tab|space`。
* `indent_size` 缩进的长度，可选值`integer|tab`。
* `tab_width` tab的长度，可选值`integer`。
* `end_of_line` 换行符配置，不同的操作系统有不同的配置`win用crlf`、`linux/unix用lf`、`mac用cr`，如果需要经常在不同的操作系统切换最好不要配置这个值，可选值`lf|crlf|cr`（[相关解释](https://github.com/cssmagic/blog/issues/22)）。
* `charset` 字符集设置，可选值`latin1|utf-8|utf-16be|utf-16le|utf-8-bom`。
* `trim_trailing_whitespace` 是否需要去除行尾的无用空格，可选值`true|false`。
* `insert_final_newline` 是否需要在文件尾部插入空行，可选值`true|false`。
* `max_line_length` 设置每行的最大字符长度，可选值`integer|off`。

#### 例子

```
# 设置当前配置文件所在目录为项目根目录
root = true
 
# 所有文件
# 设置换行符为 lf
# 设置需要在文件底部插入行
[*]
end_of_line = lf
insert_final_newline = true
 
# 当文件名为 .js 或 .py 结尾
# 设置字符集为utf-8
[*.{js,py}]
charset = utf-8
 
# 当文件名为 .py 结尾
# 设置缩进使用空格
# 设置缩进长度为4个空格
[*.py]
indent_style = space
indent_size = 4
 
# 当文件名为 .js 结尾
[*.js]
indent_style = tab
 
# 文件位于 `lib` 目录下 文件名为 .js 结尾
# 设置缩进使用空格
# 设置缩进长度为2个空格
[lib/**.js]
indent_style = space
indent_size = 2
 
# 当文件名为 .travis.yml 或者 package.json
# 设置缩进使用空格
# 设置缩进长度为2个空格
[{package.json,.travis.yml}]
indent_style = space
indent_size = 2
```

## 一起成长

如果您感觉有收获可以点赞关注`激励我`，也欢迎到 [Github](https://github.com/zhangxiangliang/vscode-tutorial) 加个 star。

> 本文原稿来自 [ZhangXiangLiang](https://github.com/zhangxiangliang)