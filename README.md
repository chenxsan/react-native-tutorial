# React Native 教程

事先声明，作者是一名前端开发，对 iOS/Android 原生开发并不了解，某些看法难免失于偏颇，欢迎指正。

## 准备工作

1. 如果只针对 iOS 平台，请准备一台 Mac 系统的电脑；如果只想开发 Android 应用，则 Linux/Windows/Mac 均可，不过我还是推荐使用 Mac 电脑，因为能节省不少时间
2. 翻墙工具要给力，否则跑完 `npm install`，人生也到尽头
3. 学好英文，不要看中文教程

    这一点，当然会有争议。
    
    不过，请先看下表，这是我从 Github API 抓取的 React Native 发布时间表，可以看到，React Native 目前的更新非常快，基本上两个星期推一个小版本，其中 API 可能会调整、变动。许多中文信息当时有效，过两天可能就失效了 - 所以最好的办法，是阅读英文原文。

    <table><thead><tr><th>版本</th><th>日期</th></tr></thead><tbody><tr><td>v0.13.0</td><td>10/24/2015</td></tr><tr><td>v0.14.0-rc</td><td>10/29/2015</td></tr><tr><td>v0.15.0-rc</td><td>11/10/2015</td></tr><tr><td>0.14.0</td><td>11/6/2015</td></tr><tr><td>v0.14.1</td><td>11/7/2015</td></tr><tr><td>v0.14.2</td><td>11/10/2015</td></tr><tr><td>v0.15.0</td><td>11/24/2015</td></tr><tr><td>v0.16.0</td><td>11/26/2015</td></tr><tr><td>v0.17.0</td><td>12/12/2015</td></tr><tr><td>v0.18.0</td><td>1/6/2016</td></tr><tr><td>v0.19.0</td><td>2/4/2016</td></tr><tr><td>v0.20.0</td><td>2/17/2016</td></tr><tr><td>v0.21.0</td><td>3/1/2016</td></tr><tr><td>v0.22.0</td><td>3/9/2016</td></tr><tr><td>v0.24.0</td><td>4/5/2016</td></tr><tr><td>v0.23.0</td><td>4/7/2016</td></tr><tr><td>v0.23.1</td><td>4/8/2016</td></tr><tr><td>v0.25.1</td><td>5/5/2016</td></tr><tr><td>v0.25.0</td><td>5/6/2016</td></tr><tr><td>v0.26.0</td><td>5/19/2016</td></tr><tr><td>v0.27.0-rc</td><td>5/21/2016</td></tr><tr><td>v0.26.1</td><td>5/22/2016</td></tr><tr><td>v0.26.2</td><td>5/25/2016</td></tr><tr><td>v0.27.0</td><td>6/6/2016</td></tr><tr><td>v0.28.0</td><td>6/22/2016</td></tr><tr><td>v0.29.0</td><td>7/6/2016</td></tr><tr><td>v0.29.1</td><td>7/14/2016</td></tr><tr><td>v0.29.2</td><td>7/18/2016</td></tr><tr><td>v0.30.0</td><td>7/21/2016</td></tr><tr><td>v0.31.0</td><td>8/5/2016</td></tr></tbody></table>

## 搭建环境

在 Mac 下开发 React Native，需要准备以下环境：

1. [Xcode](https://developer.apple.com/xcode/cn/) - 用于编译、构建项目，运行模拟器等
2. [node.js](https://nodejs.org/en/) - 项目的依赖等都需要通过 node.js 的 npm 包管理器安装、管理
3. [react-native-cli](https://www.npmjs.com/package/react-native-cli) - React Native 的命令行工具
4. [Watchman](https://facebook.github.io/watchman/) - 文件监控工具，可以监听文件变化，然后执行各种任务

在安装完以上各项后，我们就可以在命令行下初始化项目并运行起来：

```bash
$ react-native init myFirstApp
$ cd myFirstApp
$ react-native run-ios
```
稍等片刻，我们就能在 iOS 模拟器下看到 app 的样子。

## 目录

1. [语法入门](syntax.md)