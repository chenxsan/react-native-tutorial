# React Native 语法入门

我猜，写 React Native 的开发者可以简单分三类：

1. 本是前端开发，熟悉 react.js
2. 本是 iOS/Android 原生开发
3. 不属于前面两类

对第一类开发者来说，React Native 的语法并不难，因为它本身就只是 JavaScript + [JSX](https://facebook.github.io/react/docs/jsx-in-depth.html)，熟悉了 react.js，React Native 的上手也很快，毕竟，react.js 推出时，打的口号就是 Learn Once, Write anywhere。

对第二类开发者来说，突然要写 JavaScript 了，可能有些莫名其妙。

对第三类开发者来说 - 抱歉，我不了解这群人，我不知道你们为什么要学原生 app 的开发。

人类看到图片，会知道它是图片，但计算机需要辅助。比如有一个 url，它是一张图片，我们要让计算机识别，就要标识出来：

```
这是一张图片 -> https://example.com/image.png
```
如果能这样写代码，说明某些人追求的中文编码已经成功了，但可惜并不能这样写，我们要用英文这样写：

```
<Image>https://example.com/image.png</Image>
```
上面的写法，只不过标识了图片在网络上的地址，如果我们要标识出图片的大小呢？估计得这么写：

```
<Image>
  <Source>https://example.com/image.png</Source>
  <Size>100</Size>
</Image>
```
当然，这种写法太繁琐了，写代码的人，通常都是懒的，能省一个字符是一个字符，

```
<Image source='https://example.com/image.png' size='100' />
```
这样，我们的 JSX 语法就入门了。

React Native 提供的各种组件，大抵都是上面这类，举些例子说：

1. `<Text></Text>` - 标识文本
2. `<TouchableHighlight></TouchableHighlight>` - 标识可点击的区域

当然，我们不必都记在脑海里，通常在要用的时候，检索一下就是。