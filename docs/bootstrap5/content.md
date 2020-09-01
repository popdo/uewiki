# 内容

## 全局设置说明

为了在媒体响应上具有更好的体验bootstrap使用rem作为尺寸单位。为了更容易地跨设备大小缩放，块元素应该使用rem作为边距。尽可能使用inherit，尽量减少字体相关属性不必要的声明。

更新`<html>`和`<body>`元素以提供更好的页面范围默认值。更具体地说：

- `box-sizing:border-box`是在每个元素上全局设置的，包括`*::before`和`*::after`，以确保不会超过此元素的边框宽度。
- `<html>`上没有声明基本字体大小，但假定为16px（浏览器默认值）。字体大小：1rem应用于`<body>`上，以便通过媒体查询轻松响应类型缩放，同时尊重用户偏好并确保更易访问的方法。可以通过修改`$font-size`根变量来覆盖此浏览器默认值。
- `<body>`还设置了全局`font-family`, `font-weight`, `line-height`和`color`。某些表单元素会继承这一特性，以防止字体不一致。
- 为了安全起见，`<body>`有一个声明的背景色，默认为#fff。

## 版式设计

### 标题和段落

如果想在`h1~h6`以外的元素上使用同样的标题效果可以添加`.h1`~`.h6`类名 即可。

|Heading|Example|更大的标题(类名:display-*)|
|-------|-------|--------|
|h1|<span class="h1">h1. Bootstrap heading</span>|<span class="display-1">Display1 Bootstrap heading</span>|
|h2|<span class="h2">h2. Bootstrap heading</span>|<span class="display-2">Display2 Bootstrap heading</span>|
|h3|<span class="h3">h3. Bootstrap heading</span>|<span class="display-3">Display3 Bootstrap heading</span>|
|h4|<span class="h4">h4. Bootstrap heading</span>|<span class="display-4">Display4 Bootstrap heading</span>|
|h5|<span class="h5">h5. Bootstrap heading</span>|<span class="display-5">Display5 Bootstrap heading</span>|
|h6|<span class="h6">h6. Bootstrap heading</span>|<span class="display-6">Display6 Bootstrap heading</span>|

### 列表

所有列表-`<ul>`、`<ol>`和`<dl>`都删除了它们的页边距顶部和底部边距：1rem。嵌套列表没有边距底端。我们还重置了左边的元素。

<!-- tabs:start -->

#### **ul列表**

```demo
<ul>
  <li>一级li</li>
  <li>Consectetur adipiscing elit</li>
  <li>Facilisis in pretium nisl aliquet</li>
  <li>Nulla volutpat aliquam velit
    <ul>
      <li>二级li</li>
      <li>Purus sodales ultricies</li>
      <li>Vestibulum laoreet porttitor sem</li>
    </ul>
  </li>
</ul>
<hr>
<ul class="list-unstyled">
  <li>无样式列表</li>
  <li>Aenean sit amet erat nunc</li>
  <li>Eget porttitor lorem</li>
</ul>
<hr>
<ul class="list-inline">
  <li class="list-inline-item">行内列表li1</li>
  <li class="list-inline-item">行内列表li2</li>
  <li class="list-inline-item">行内列表li3</li>
</ul>
```

```html
<ul>
  <li>一级li</li>
  <li>Nulla volutpat aliquam velit
    <ul>
      <li>二级li</li>
    </ul>
  </li>
</ul>
<hr>

<!-- 无样式列表 -->
<ul class="list-unstyled">
  <li>无样式列表</li>
</ul>

<!-- 行内列表 -->
<ul class="list-inline">
  <li class="list-inline-item">行内列表li1</li>
  <li class="list-inline-item">行内列表li2</li>
  <li class="list-inline-item">行内列表li3</li>
</ul>
```

#### **ol列表**

```demo
<ol>
  <li>一级li</li>
  <li>Consectetur adipiscing elit</li>
  <li>Facilisis in pretium nisl aliquet</li>
  <li>Nulla volutpat aliquam velit
    <ol>
      <li>二级li</li>
      <li>Purus sodales ultricies</li>
      <li>Vestibulum laoreet porttitor sem</li>
    </ol>
  </li>
</ol>
<hr>
<!-- 无样式列表 -->
<ol class="list-unstyled">
  <li>无样式列表</li>
  <li>Aenean sit amet erat nunc</li>
  <li>Eget porttitor lorem</li>
</ol>
```

```html
<ol>
  <li>一级li</li>
  <li>Nulla volutpat aliquam velit
    <ol>
      <li>二级li</li>
    </ol>
  </li>
</ol>
<hr>

<!-- 无样式列表 -->
<ol class="list-unstyled">
  <li>无样式列表</li>
</ol>
```

#### **dl列表**

```demo
<dl>
    <dt>Description lists</dt>
    <dd>A description list is perfect for defining terms.</dd>
    <dt>Euismod</dt>
    <dd>Vestibulum id ligula porta felis euismod semper eget lacinia odio sem.</dd>
    <dd>Donec id elit non mi porta gravida at eget metus.</dd>
    <dt>Malesuada porta</dt>
    <dd>Etiam porta sem malesuada magna mollis euismod.</dd>
</dl>
```

```html
<dl>
    <dt>Description lists</dt>
    <dd>A description list is perfect for defining terms.</dd>
    <dt>Euismod</dt>
    <dd>Vestibulum id ligula porta felis euismod semper eget lacinia odio sem.</dd>
    <dd>Donec id elit non mi porta gravida at eget metus.</dd>
    <dt>Malesuada porta</dt>
    <dd>Etiam porta sem malesuada magna mollis euismod.</dd>
</dl>
```

<!-- tabs:end -->

### 突出段落

通过加上"`.lead`"使段落突出。

```demo
<p>
  Vivamus sagittis lacus vel augue laoreet rutrum faucibus dolor auctor. Duis mollis, est non commodo luctus.
</p>
<p class="lead">
  Vivamus sagittis lacus vel augue laoreet rutrum faucibus dolor auctor. Duis mollis, est non commodo luctus.
</p>
```

```html
<p>
  Vivamus sagittis lacus vel augue laoreet rutrum faucibus dolor auctor. Duis mollis, est non commodo luctus.
</p>
<p class="lead">
  Vivamus sagittis lacus vel augue laoreet rutrum faucibus dolor auctor. Duis mollis, est non commodo luctus.
</p>
```

### 内联文本标签

|标签|类名支持|说明|示例|
|---|-------|---|----|
|`<code>`||内联代码|`.cc{color:#ccc}`|
|`<pre>`<br>`<code>...</code>`<br>`</pre>`||代码块|<pre><code>$text="hello";<br>echo $text</code></pre>|
|`<var>`||变量|<var>var</var>|
|`<kbd>`||键盘符|<kbd>Shift</kbd>|
|`<samp>`||是一个短语标签，用来定义计算机程序的样本文本|<samp>样本文本</samp>|
|`<address>`||地址|<address><a href="mailto:first.last@example.com">first.last@example.com</a></address>|
|`<abbr>`||标记一个简称、缩写|Nulla <abbr title="attribute">attr</abbr> vitae elit libero, a pharetra augue.|
|`<blockquote>`|.blockquote|引用文档中其他来源的内容块，更详细查看[官方文档](https://v5.getbootstrap.com/docs/5.0/content/typography/#blockquotes)|<blockquote>小鸟飞的很高，很远...</blockquote>|
|`<mark>`||表示标记或突出显示以供参考或表示的文本。|<mark>highlight</mark>|
|`<small>`||代表旁注和小字体，如版权和法律文本。||
|`<del>`||删除线：表示不再相关或不再准确的元素。|<del>开发一个blog系统</del>|
|`<u>`||下划线：在非链接元素上少用，容易与链接混淆。|<u>Hello!</u>|
|`<strong>`||加粗：表示强调。强调性高于em||
|`<b>`||加粗：单纯的加粗||
|`<em>`||斜体：含语意-一般的强调文本||
|`<i>`||斜体：无语意||
|`<br>`||是HTML写法||
|`<br/>`||是XHTML1.1的写法，也是XML写法。||
|`<br />`||是XHTML为兼容HTML的写法，也是XML写法||

## 图片

将图像设置为响应式（这样它们永远不会变得比其父元素大），并为它们添加轻量级样式 -- 所有这些都通过类来实现的。

### 响应式图片

在Bootstrap中的图片是用`.img-fluid`来做响应的，它应用`max-width: 100%;`和`height: auto;`到图片上，使它与父元素一起伸缩。

```demo
<svg class="img-fluid"width="100%" style="text-anchor: middle;" height="250" xmlns="http://www.w3.org/2000/svg" aria-label="Placeholder: Responsive image" preserveAspectRatio="xMidYMid slice" role="img" focusable="false"><title>Placeholder</title><rect width="100%" height="100%" fill="#868e96"></rect><text x="50%" y="50%" fill="#dee2e6" dy=".3em">Responsive image</text></svg>
```

```html
<img src="..." class="img-fluid" alt="...">
```

### 图片缩略图

除了我们的`.border-radius`实用工具之外，您还可以使用`.img-thumbnail`使图像具有`1px`的圆角边框外观。

```demo
<svg class="img-thumbnail" style="text-anchor: middle;" width="200" height="200" xmlns="http://www.w3.org/2000/svg" aria-label="A generic square placeholder image with a white border around it, making it resemble a photograph taken with an old instant camera: 200x200" preserveAspectRatio="xMidYMid slice" role="img" focusable="false"><title>A generic square placeholder image with a white border around it, making it resemble a photograph taken with an old instant camera</title><rect width="100%" height="100%" fill="#868e96"></rect><text x="50%" y="50%" fill="#dee2e6" dy=".3em">200x200</text></svg>
```

```html
<img src="..." class="img-thumbnail" alt="...">
```

### 图片对齐

左右浮动对齐。

```demo
<svg class="rounded float-left" style="text-anchor: middle;" width="200" height="200" xmlns="http://www.w3.org/2000/svg" aria-label="Placeholder: 200x200" preserveAspectRatio="xMidYMid slice" role="img" focusable="false"><title>Placeholder</title><rect width="100%" height="100%" fill="#868e96"></rect><text x="50%" y="50%" fill="#dee2e6" dy=".3em">200x200</text></svg>
<svg class="rounded float-right" style="text-anchor: middle;" width="200" height="200" xmlns="http://www.w3.org/2000/svg" aria-label="Placeholder: 200x200" preserveAspectRatio="xMidYMid slice" role="img" focusable="false"><title>Placeholder</title><rect width="100%" height="100%" fill="#868e96"></rect><text x="50%" y="50%" fill="#dee2e6" dy=".3em">200x200</text></svg>
<div class="clearfix"></div>
```

```html
<img src="..." class="rounded float-left" alt="...">
<img src="..." class="rounded float-right" alt="...">
```

图片水平对齐有两种常用方法。第一种方法是使用我们的[间距辅助工具](/bootstrap5/utilities?id=spacing)中的`.mx-auto`。

```demo
<svg class="rounded mx-auto d-block" style="text-anchor: middle;"  width="200" height="200" xmlns="http://www.w3.org/2000/svg" aria-label="Placeholder: 200x200" preserveAspectRatio="xMidYMid slice" role="img" focusable="false"><title>Placeholder</title><rect width="100%" height="100%" fill="#868e96"></rect><text x="50%" y="50%" fill="#dee2e6" dy=".3em">200x200</text></svg>
```

```html
<img src="..." class="rounded mx-auto d-block" alt="...">
```

方法二：

```demo
<div class="text-center">
  <svg class="rounded" width="200" style="text-anchor: middle;"  height="200" xmlns="http://www.w3.org/2000/svg" aria-label="Placeholder: 200x200" preserveAspectRatio="xMidYMid slice" role="img" focusable="false"><title>Placeholder</title><rect width="100%" height="100%" fill="#868e96"></rect><text x="50%" y="50%" fill="#dee2e6" dy=".3em">200x200</text></svg>
</div>
```

```html
<div class="text-center">
  <img src="..." class="rounded" alt="...">
</div>
```

### 文档图片

`<figure>`标签用作文档中插图的图片。当你需要显示内容（例如带有可选标题的图片）时，可以考虑使用。它是HTML 5 中的新标签。

- 请使用包含`.fig`、`.fig-img`和`.fig-caption`的元素为HTML5`<figure>`和`<figcaption>`元素提供一些基本样式。
- 如果`<figure>`中的图片没有明确的大小，请确保在你的`<img>`中添加`.img-fluid`类，使其变为响应式的。

```demo
<figure class="figure">
  <svg class="figure-img img-fluid rounded" style="text-anchor: middle;" width="400" height="300" xmlns="http://www.w3.org/2000/svg" aria-label="Placeholder: 400x300" preserveAspectRatio="xMidYMid slice" role="img" focusable="false"><title>Placeholder</title><rect width="100%" height="100%" fill="#868e96"></rect><text x="50%" y="50%" fill="#dee2e6" dy=".3em">400x300</text></svg>
  <figcaption class="figure-caption text-center">A caption for the above image.</figcaption>
</figure>
```

```html
<figure class="figure">
  <img src="..." class="figure-img img-fluid rounded" alt="...">
  <figcaption class="figure-caption text-center">A caption for the above image.</figcaption>
</figure>
```
