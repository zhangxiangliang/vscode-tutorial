# DotENV - dotenv语法高亮

## 简介

在开发过程中会有一些 `环境配置`，需要进行 `生产环境`、`开发环境` 等其他环境的单独配置。例如生产环境数据库账号使用pushmetop，开发环境数据库账号使用test。而 `dotenv` 则是对这些环境变量参数进行记录的一种规范。

## 安装

使用`command + shift + x`打开扩展，搜索`DotENV`插件并安装后重启编辑器，扩展将会给 .env 文件进行代码着色。

## 资源

* go [.env 库](https://github.com/theskumar/joho/godotenv)
* php [.env 库](https://github.com/theskumar/symfony/dotenv)
* ruby [.env 库](https://github.com/bkeepers/dotenv)
* nodejs [.env 库](https://github.com/motdotla/dotenv)
* python [.env 库](https://github.com/theskumar/python-dotenv)

## 使用

#### 单行值

```
PUSH_ME_TOP=PUSHMETOP
```

#### 多行值

```
PUSH_ME_TOP="pushe\nme\ntop"
```

```
PUSH_ME_TOP="push
me
top"
```

#### 命令替换

在环境变量中使用命令 `$(your_command)`。

```
PUSH_ME_TOP="$(whoami) push me top"
```

#### 变量替换

在定义的新环境变量中使用其他环境变量 `${VAR}`。

```
WHO=ME
PUSH_ME_TOP="${WHO} push me top"
```

#### 变量注释
```
# 这是一个注释
PUSH_ME_TOP=PUSHMETOP
```
## 一起成长

如果您感觉有收获可以点赞关注`激励我`，也欢迎到 [Github](https://github.com/zhangxiangliang/vscode-tutorial) 加个 star。

> 本文原稿来自 [ZhangXiangLiang](https://github.com/zhangxiangliang)