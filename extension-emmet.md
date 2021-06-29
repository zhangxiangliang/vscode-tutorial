# Emmet - HTML与CSS快速生成工具

## 简介

在编辑 html 和 css 代码的时候，我们经常要无数次的敲入 `<tag></tag>`、 `<tag class="pushmetop"></tag>` 、`<tag id="pushmetop"></tag>` 效率特别低下。就算使用了 `snippets` 在写类似：

```
<ul>
    <li>push</li>
    <li>me</li>
    <li>top</li>
</ul>
```

依旧需要多次的使用各种 `snippets`，而 `emmet` 提供了一种非常简练的语法规则，然后立刻生成对应的 HTML 结构或者 CSS 代码。例如完成上面的代码只需要输入 `ul>li*3` 则可以快速生成 HTML 结构。

## 安装

Emmet 是 VSCode 内建的扩展，只需要在 `.html` 和 `.css` 类型的文件下即可使用。如果需要进行别的语言也可以使用 `command + ,` 搜索 `emmet`，在搜索结果中点击 Emmet: Include Languages 标题内的 Edit in settings.json 进行设置，例如php的配置：

```
{
    "emmet.syntaxProfiles": {
        "php": "html"
    }
}
```

小提示：在 VSCode 中的 emmet 插件在一些嵌套中可能会失效，官方正在修复这个问题。可以先利用分组 `()` 来解决失效问题。

## 资源

* [官方网站](https://emmet.io/)
* [Emmet 速查表](https://docs.emmet.io/cheat-sheet/)

## 使用

#### 基础用法

使用标签的名称即可快速生成 html 代码，当然也可以输入自定义的标签。

输入

```
h1
```

输出

```
<h1></h1>
```

#### 类名

使用 `标签名.类名` 的形式可以在快速生成 html 代码时生成类名，如果直接使用 `.类名` 的形式会输出div的html和类名。

输入

```
h1.pushmetop
```

输出

```
<h1 class="pushmetop"></h1>
```

输入

```
.pushmetop
```

输出

```
<div class="pushmetop"></div>
```

#### ID名

使用 `标签名#类名` 的形式可以在快速生成 html 代码时生成类名，如果直接使用 `#类名` 的形式会输出div的html和类名。

输入

```
h1#pushmetop
```

输出

```
<h1 id="pushmetop"></h1>
```

输入

```
#pushmetop
```

输出

```
<div id="pushmetop"></div>
```

#### 属性

Emmet 除了使用 `.` 表示 类名 和 `#` 表示 ID名，还可以使用 `[xxx=xxx]` 来表示属性。

输入

```
input[type=email][placeholder=pushmetop]
```

输出

```
<input type="email" placeholder="pushmetop">
```

#### 子元素

使用 `标签名 > 标签名` 的形式可以快速生成带有层级结构的 html 代码。

输入

```
div>h1
```

输出

```
<div>
    <h1></h1>
</div>
```

#### 文本操作

使用 `标签名{文本}` 的形式可以快速生成 html 代码和文本内容。

输入

```
h1{pushmetop}
```

输出

```
<h1>pushmetop</h1>
```

#### 重复元素

使用 `标签名*个数` 的形式可以快速生成多个标签名一样的 html 代码。

输入

```
ul>li*5
```

输出

```
<ul>
    <li></li>
    <li></li>
    <li></li>
    <li></li>
    <li></li>
</ul>
```

#### 分组和兄弟元素

使用 `()` 可以对操作代码进行分组，配合使用兄弟元素的操作符号 `+`。

输入

```
.columns>(.hello{pushmetop})+(.world{pushmetop})
```

输出

```
<div class="columns">
    <div class="hello">pushmetop</div>
    <div class="world">pushmetop</div>
</div>
```

#### 上级元素来减少分组嵌套

如果只使用分组和兄弟元素，太多的 `()` 有时候不利于阅读。使用 `^` 可以表示当前元素向上一级元素。

使用分组和兄弟元素

```
.columns>(.hello>.box>h2{pushmetop})+(.world>.box>h2{pushmetop})
```

使用上级元素

```
.columns>.hello>.box>h2{pushmetop}^^.world>.box>h2{pushmetop}
```

输出

```
<div class="columns">
    <div class="hello">
        <div class="box">
            <h2>pushmetop</h2>
        </div>
    </div>
    <div class="world">
        <div class="box">
            <h2>pushmetop</h2>
        </div>
    </div>
</div>
```

#### 占位符

emmet 提供了 `$` 符号，可以用于快速生成一系列的数字占位符。

输入

```
ul>li.li-${I love pushmetop $ strong!!!!}*10
```

输出

```
<ul>
    <li class="li-1">I love pushmetop 1 strong!!!!</li>
    <li class="li-2">I love pushmetop 2 strong!!!!</li>
    <li class="li-3">I love pushmetop 3 strong!!!!</li>
    <li class="li-4">I love pushmetop 4 strong!!!!</li>
    <li class="li-5">I love pushmetop 5 strong!!!!</li>
    <li class="li-6">I love pushmetop 6 strong!!!!</li>
    <li class="li-7">I love pushmetop 7 strong!!!!</li>
    <li class="li-8">I love pushmetop 8 strong!!!!</li>
    <li class="li-9">I love pushmetop 9 strong!!!!</li>
    <li class="li-10">I love pushmetop 10 strong!!!!</li>
</ul>
```

#### 常用的 HTML 元素

Emmet 除了简单的输出标签、类名、ID名等，还带了一些列快捷缩写详情点击 [Emmet 速查表](https://docs.emmet.io/cheat-sheet/)。

* `!`： 快速输出 HTML 基础结构
* `a`：`<a href=""></a>`
* `link:css`：`<link rel="stylesheet" href="style.css">`
* `script:src`：`<script src=""></script>`
* `input:text`：`<input type="text" name="" id="">`

#### 常用的 CSS 元素

Emmet 除了提供了 html 代码快速生成 还提供了 css 样式的一些 `snippets` 快捷缩写详情点击 [Emmet 速查表](https://docs.emmet.io/cheat-sheet/)。

* `pos`：`position: relative;`
* `d`：`display: block;`
* `m`：`margin: ;`
* `mt`：`margin-top: ;`
* `mb`：`margin-bottom: ;`
* `pw`：`padding-top: ;`
* `pb`：`padding-bottom: ;`
* `bg`：`background: #000;`
* `!`：`!important`
* `@m`：`@media screen {}`
* `c`：`color: #000;`
* `op`：`opacity: ;`
## 一起成长

如果您感觉有收获可以点赞关注`激励我`，也欢迎到 [Github](https://github.com/zhangxiangliang/vscode-tutorial) 加个 star。

> 本文原稿来自 [ZhangXiangLiang](https://github.com/zhangxiangliang)