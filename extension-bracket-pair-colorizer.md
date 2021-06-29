# Bracket Pair Colorizer - 括号美化

## 简介

在编辑代码的过程中会出现嵌套非常多的 `()` 和 `{}`、`[]`，使得我们阅读代码需要小心谨慎的进行代码匹配：

```
(() => setInterval(() => {
    console.log('pushmetop');
}, 1000))();
```

使用 `Bracket Pair Colorizer` 可以对匹配的 `()` 和 `{}`、`[]` 进行对应的染色方便更好的阅读代码，也支持匹配着色方式的自定。

## 安装

使用`command + shift + x`打开扩展，搜索`DotENV`插件并安装后重启编辑器，扩展将会给 .env 文件进行代码着色。

## 使用

* `"bracketPairColorizer.timeOut"` 着色时间间隔，默认为0，可选值`integer`。
* `"bracketPairColorizer.forceUniqueOpeningColor"` 是否强制相邻的匹配颜色不相同，默认为false，可选值`true|false`。
* `bracketPairColorizer.forceIterationColorCycle` 是否循环匹配颜色，默认为 true，可选值`true|false`。
* `bracketPairColorizer.colorMode` 是否对 `()` 和 `{}`、`[]` 分别设置颜色，默认为Consecutive，可选值`Consecutive|Independant`。
* `bracketPairColorizer.activeScopeCSS` 配置在代码块中的高亮状态。
* `bracketPairColorizer.showBracketsInGutter` 是否在行号栏显示当前区间范围，默认为 false，`true|false`。
* `bracketPairColorizer.showBracketsInRuler` 是否在代码地图中显示当前区间范围，默认为 false，`true|false`。
* `bracketPairColorizer.rulerPosition` 代码地图中显示当前区间范围的坐标，默认为 Center，`Center|Full|Left|Right`。
* `bracketPairColorizer.showVerticalScopeLine` 是否显示垂直匹配线，默认为 true，`true|false`。
* `bracketPairColorizer.showHorizontalScopeLine` 是否显示水平匹配线，默认为 true，`true|false`。
* `bracketPairColorizer.scopeLineCSS` 配置匹配线的样式。
* `bracketPairColorizer.consecutivePairColors` 配置连续颜色对。
* `bracketPairColorizer.independentPairColors` 配置独立颜色对。
* `bracketPairColorizer.excludedLanguages` 配置不需要使用括号美化的文件扩展。

## 一起成长

如果您感觉有收获可以点赞关注`激励我`，也欢迎到 [Github](https://github.com/zhangxiangliang/vscode-tutorial) 加个 star。

> 本文原稿来自 [ZhangXiangLiang](https://github.com/zhangxiangliang)