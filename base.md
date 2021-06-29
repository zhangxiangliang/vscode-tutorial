# 初识编辑器

## Command - 命令面板

使用 `command + shift + p` 可以打开命令面板，命令面板可以查看编辑器中所有的命令，可以通过模糊搜索来快速的找到并执行自己需要的命令。

使用 `command + p` 可以打开快速切换文件面板，输入需要访问的文件名后便可以迅速打开文件。


## Activity Bar - 活动栏

编辑器最左边的栏叫做 `活动栏`，从上到下提供了5个默认编辑器快捷方式 分别是 Explorer、Search、Source Control、Debug、Extensions。点击这几个快捷方式能分别打开对应的功能并显示在 \`边栏\` 上。有时候安装一些插件也会在这边生成新的快捷方式。

隐藏`活动栏`可以打开`命令面板`输入`View: Toggle Activity Bar Visibility`来隐藏活动栏。

查看`快捷方式`快捷键可以把鼠标悬停在图标上即可看到对应的快捷键。

#### Explorer - 资源管理器

用于显示当前项目目录结构，在这里你可以进行编辑、创建、删除目录或文件等一系列操作。

如果想要快速将边栏切换到 资源管理器 可以使用`command + shift + e`。

#### Search - 搜索

输入要搜索的关键字后可以检索出当前项目文件中包含关键字的文件，并显示出他们的路径。

如果想要快速将边栏切换到 搜索 可以使用`command + shift + f`。

#### Source Control - 源码管理器

编辑器自带的一款非常好用的`git`源码管理器，可以在这进行代码的`版本控制`，包括推送、提交、拉取、分支创建等一系列方便好用的操作。在后面的章节中将详细介绍该功能。

如果想要快速将边栏切换到 源码管理器 可以使用`control+ shift + g`。

#### Debug - 调试器

需要进行一定的配置后可以调试代码。（相关配置请根据对应的编程语言安装扩展）

如果想要快速将边栏切换到 调试器 可以使用`control+ shift + d`。

#### Extensions - 扩展

用于搜索、安装和管理扩展，通过一系列的可以让 VSCode 变得更加得心应手。

如果想要快速将边栏切换到 扩展 可以使用`control+ shift + x`。

## Side Bar - 边栏
活动栏右边的栏目叫做边栏，它会随着选择的快捷方式而变化。

隐藏 `边栏` 可以打开 `命令面板` 输入 `View: Toggle Side Bar Visibility` 来隐藏边栏，也可以使用快捷键 `command + b` 来实现隐藏。

## Status Bar - 状态栏
编辑器最底部的栏目叫做状态栏目，用于展示所在分支、Debug 情况、行号、编码、空格缩进等信息。

隐藏 `状态栏` 可以打开 `命令面板` 输入 `View: Toggle Status Bar Visibility` 来隐藏状态栏。

## Pannel - 面板
面板中包括了调试控制台、终端等功能。

默认面板是隐藏起来的，可以把鼠标放在状态栏后按住往上拖拉来显示。

快速打开 面板 可以使用快捷键 `command + j`。

快速打开 终端 可以使用快捷键 <code>command + `</code>。

快速打开 调试控制台 可以使用快捷键 `command+ shift + y`。

## 一起成长

如果您感觉有收获可以点赞关注`激励我`，也欢迎到 [Github](https://github.com/zhangxiangliang/vscode-tutorial) 加个 star。

> 本文原稿来自 [ZhangXiangLiang](https://github.com/zhangxiangliang)