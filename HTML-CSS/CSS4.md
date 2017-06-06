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

#### 测试 ####
在网站 [css-selectors.com]("http://css4-selectors.com/") 上可以测试你的浏览器是否支持这些选择器和其他高级选择器。另外你也可以找到要添加的选择器。

## CSS混合模式 ##
该规范将混合模式适用于背景以及浏览器HTML页面里的任何元素。
```css
.box {
  background-color: red;
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
![使用background-blend-mode（图片来源于网络）](http://img.ptcms.csdn.net/article/201503/06/54f944c3249a3.jpg)
> 使用background-blend-mode（图片来源于网络）





