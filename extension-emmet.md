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

## 资源

* [官方网站](https://emmet.io/)
* [Emmet 语法](https://docs.emmet.io/cheat-sheet/)

## 安装

Emmet 是 VSCode 内建的扩展，只需要在 `.html` 和 `.css` 类型的文件下即可使用。如果需要进行别的语言也可以使用 `command + ,` 搜索 `emmet`，在搜索结果中点击 Emmet: Include Languages 标题内的 Edit in settings.json 进行设置，例如php的配置：

```
{
    "emmet.syntaxProfiles": {
        "php": "html"
    }
}
```

## 使用

### 基础用法

### 小技巧

#### 利用分组和兄弟元素进行复制操作

使用 `()` 可以对操作代码进行分组，配合使用兄弟元素的操作符号 `+`。