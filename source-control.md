# 源码管理

需要先使用`control + shift + g`打开 源码管理器。

## 介绍

源码管理器中的`CHANGES`用于显示当前项目中的变化。文件名后会根据变化的类型分别显示：

* M 即 Modified 表示文件被修改。
* U 即 Untracked 表示文件未被跟踪或新建文件。
* D 即 Deleted 表示文件已被删除，

鼠标悬停在文件名上面，会显示可对文件进行的操作。

* 点击第一个图标可以打开当前文件。
* 点击第二个图标可以撤销当前文件的变化。
* 点击第三个图标可以把文件提交到`STAGED CHANGES`中。
* 点击文件名可以直接打开文件修改变化窗口。

## 文件状态

打开修改的文件可以看到被修改的地方的行头被标上了蓝色，点击改区域可以快速查看当前修改和未修改的对比 和 进行快速撤回的操作。

## 项目初始化

在编辑器输入`Git: Initialize Repository`也可以快速初始化当前项目。

## 修改提交

当文件被提交到`STAGED CHANGES`后，可以在面板中的`Message`输入框中输入提交信息，使用`command + enter`既可执行 git commit 操作将操作写入日志中。

## 恢复修改

当文件被提交到`STAGED CHANGES`中时，将鼠标放到该文件名上点击减号即可把文件回退到`CHANGES`中。

当文件在`CHANGES`中时，将鼠标放到该文件名上点击第二个图标即可取消文件修改。

当文件刚被提交时，可以点击 源码管理器 顶部第三个图标`More Action`选 `Undo Last Commit`撤回最后一次代码提交。

如果想撤销当前所有文件的修改，可以点击 源码管理器 顶部第三个图标`More Action`选择`Discard All changes`撤回所有修改。

## 分支管理

使用`command + shift + p`打开命令面板，输入`Git: Branch`可以看到一些列的分支相关操作：

* Git: Create Branch - 创建分支
* Git: Delete Branch - 删除分支
* Git: Merge Branch  - 合并分支
* Git: Publish Branch - 推送分支
* Git: Rename Branch - 重命名分支

## 储藏修改

使用`command + shift + p`打开命令面板，输入`Git: Stash`可以看到一些列的分支相关操作：

* Git: Stash - 将当前编辑内容进行存储到记录中
* Git: Apply Stash - 打开已经存储编辑内容
* Git: Apply Stash - 打开最后一个存储编辑内容
* Git: Pop Stash - 打开已经存储编辑内容 并 删除对应记录
* Git: Pop Stash - 打开最后一个存储编辑内容 并 删除对应记录

## 解决冲突

当代码合并出现冲突时，冲突文件的顶部会出现一些可选项：

* Accept Current Change - 当前的修改
* Accept Incoming Change - 即将合并的修改
* Accept Both Changes - 同时应用两个修改
* Compare Changes - 对比两个修改

## 远程管理

使用`command + shift + p`打开命令面板，输入下列指令可以和远程仓库进行交互：

* Git: Pull - 拉取远程仓库的修改
* Git: Push - 推送当前修改到远程仓库
* Git: Sync - 拉取远程仓库并提交修改
* Git: Publish Branch - 推送分支