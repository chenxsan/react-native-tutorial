# Text 组件

如果说人是由手、脚及大脑等组成，那么不妨说一个页面是由文本、图片等组成。

`Text` 组件是 React Native 中最常见的一个组件，它标识文本：

```js
<Text>嗨，我是普通的文本</Text>
```
我们从来不会止步于普通文本，我们可能想把文字大小调大一点。

`Text` 组件有一个 `style` 属性可以定义字体大小，实际上，其它组件多数也拥有 `style` 属性，只不过不同组件 `style` 属性中允许的特性不太一样，后面会说到。

```js
<Text style={{
  fontSize: 18
}}>嗨，我是字体大点的普通文本</Text>
```
等等，`{{}}` 是什么？如果你用过 [jsx，则已经知道](https://facebook.github.io/react/docs/jsx-in-depth.html#attribute-expressions)，如果没用过：

1. `{{}}` 是两对花括号
2. 外面一对表示它的里面是 JavaScript 表达式
3. 上面的示例中，里面的一对是对象 `{fontSize: 18}`

可以想象，我们还可以修改文本的其它样式：

1. `color` - 文本颜色
2. `textAlign` - 文本对齐方式，左，或右，或居中
3. 更多样式请查看[文档](https://facebook.github.io/react-native/docs/text.html#style)

> “小光问云门，如果文本很长，但我只想显示一行，超出的部分用 `...` 显示，该如何？”

应该说，绝大部分我们能想到的需求，React Native 都已经提供了，比如上面提及的只显示一行的需求：

```js
<Text numberOfLines={1}
  ellipsizeMode={'tail'}>a long long text here...</Text>

至于 React Native 没有提供的一些特性，还可以自己写组件来扩展。

```
另外，`Text` 是可以互相嵌套的，比如：

```js
<Text>hello <Text style={{color: 'red'}}>React Native</Text></Text>
```

