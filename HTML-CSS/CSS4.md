## 第四代CSS选择器 ##
> 第四代选择器为我们提供了诸多方法来定位CSS的内容。

#### 否定类 `:not` ####
* 在 `CSS3` 中，可以通过一个否定伪类选择器来选取不需要运用CSS的元素。
```css
p:not(.intro) { font-weight: normal;}
```
> 给除了 `.intro` 类以外的文本加粗。

* 在 `CSS4` 选择器中，可以传入一个用逗号（,）分割的选择器列表。
```css
p:not(.intro, blockquote) { font-weight: normal;}
```

#### 关联伪类 `:has` ####
通过一个参数（选择器列表），去匹配与某一元素对应的任意选择器。
```css
a:has(>img) { border: 1px solid #000;}
```
> 任何带有 `<img>` 的 `<a>` 元素都会加个黑色的边框。

```css
li:not(:has(p)) { padding-bottom: 1em;}
```
> 选择不带有 `<p>` 的 `<li>` 元素。

#### 匹配任何伪类 `:matches` ####
把规则运用在所有的选择器组中。
```css
p:matches(.alert, .error, .warn) { color: red;}
```

#### 兼容测试 ####
在网站 [css-selectors.com](http://css4-selectors.com/) 上可以测试你的浏览器是否支持这些选择器和其他高级选择器。另外你也可以找到要添加的选择器。
<br><br>

## CSS混合模式 ##
该规范将混合模式适用于背景以及浏览器HTML页面里的任何元素。

#### background-blend-mode ####
使用带有背景图片的选择器 `.box`，通过设置 `background-color` 为 `red`，`background-blend-mode` 为 `hue` 和 `multiply`，给图片添加了有趣的效果：
```css
.box {
  background-image: url(balloons.jpg);
}
.box2 {
  background-color: red;
  background-blend-mode: hue;
}
.box3 {
  background-color: red;
  background-blend-mode: multiply;
}
```
![使用 background-blend-mode](http://img.ptcms.csdn.net/article/201503/06/54f944c3249a3.jpg)
> 使用 background-blend-mode（图片来源于网络）

#### mix-blend-mode ####
使用 `mix-blend-mode` 属性可以设置混合文字置于图片顶部：
```css
.box {
  background-image: url(balloons.jpg);
}
.box h1 {
  font-size: 140px;
  color: green;
}
.box2 h1 {
  mix-blend-mode: screen;
}
```
![使用 mix-blend-mode](http://img.ptcms.csdn.net/article/201503/06/54f9454781d6f.jpg)
> 使用 mix-blend-mode（图片来源于网络）

#### 兼容测试 ####
* IE浏览器支持CSS混合模式
* Safari和Firefox紧追其后
* Opera和Chrome尚在实验阶段
> 只要在那些暂时不支持这项规范的浏览器中有向后兼容方案 —— ** 在Photoshop中完成图片的制作，然后将其替代CSS的效果 **，不至于留下一堆乱七八糟的东西，就可以小心地使用这一规范，提升设计层次。

#### 知识补给 ####
* [CSS的混合模式和规范](https://drafts.fxtf.org/compositing-1/)
* [如何使用CSS的混合模式](https://css-tricks.com/basics-css-blend-modes/)
* [Adobe网站资源](http://webplatform.adobe.com/blend-modes/)
* [Dev Opera网站](https://dev.opera.com/articles/getting-to-know-css-blend-modes/)
<br><br>

## calc() 函数 ##
