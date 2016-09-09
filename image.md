# Image 组件

都说一图抵千字，放到 React Native 下，就是一个 `Image` 抵千个 `Text`。

既然是图片，它就需要一个图片地址，在 React Native 下，它由 `source` 指定：

```jsx
<Image source={require('../images/logo.png')} />
```
通过 `require`，我们指定了一张本地图片。这是 CommonJS 引用资源的方式。

我们还可以使用网络图片，如下：

```jsx
<Image source={{uri: 'https://example.org/placeholder.png'}} />
```
不过你会发现，在使用网络图片时，App 上显示空白，并没有图片。这是因为 React Native 能够知道本地图片的尺寸，却没法知道网络图片的尺寸，需要我们在代码中指明：

```jsx
<Image source={{uri: 'https://example.org/placeholder.png'}} style={{width: 44, height: 44}}/>
```
当然我们还会有不少使用场景需要解决，下面逐一介绍。

1. 如果 Android 上的图片跟 iOS 上不是一张怎么办？

    没有问题，只要把图片命名为 `logo.android.png` 和 `logo.ios.png` 即可，React Native 会根据平台自动选择。

2. 以 iOS 平台说，它有各种分辨率的屏，我们如何使用 2x、3x 的高清图片？

    很简单，将多种图片分别命名为 `logo@2x.png`，`logo@3x.png`，React Native 会根据屏幕分辨率自动选择。

3. 背景图片？

   当然，CSS 下有 `background-image` 的属性，`Image` 组件并没有，但它同样可以作为背景图片使用，只要我们把背景前的内容置于其中：

   ```jsx
   <Image source={require('../images/background.png')} >
     <Text>我是个有背景的文字</Text>
   </Image>
   ```