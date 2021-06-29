# 代码段自定义

编辑代码时经常会一直重复类似的代码段，比如：

```
function PushMeTop() {
    // 各种各样的代码
}
```

可以通过把公共的部分抽取出来为 `snippets`，当打出关键词的时候即可快速选择需要的代码段。甚至可以对代码段进行变量化 更加灵活和复用代码块。

使用 `command + shift + p` 打开命令面板输入 `>Preferences: Configure User Snippets` 回车后即可看到一系列的语言选项。选择一个代码段所属的语言或者是创建一个新的分类后就可以开始编辑代码段了。

通过 JSON 的格式来定义代码段，例子如下：

```
{
    // 片段名
    "Print to console": {

        // 智能提示前缀
        "prefix": "log",

        // 代码段内容
        "body": [
            "console.log('$1');",
            "$2"
        ],

        // 代码段描述
        "description": "Log output to console"
    }
}
```

上面代码片段中使用了 `$1` 和 `$2` 表示当使用代码段时按下 `tab` 时会按照序号顺序跳转到对应的位置。如果需要使用默认变量名可以使用 `${id:variable}` 的形式来实现例如 ${1:hello}，对于同一个变量名在重新编辑的时候会同步操作。

## 一起成长

如果您感觉有收获可以点赞关注`激励我`，也欢迎到 [Github](https://github.com/zhangxiangliang/vscode-tutorial) 加个 star。

> 本文原稿来自 [ZhangXiangLiang](https://github.com/zhangxiangliang)