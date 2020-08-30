# 辅助工具

## Clearfix

通过向父元素添加`.clearfix`可以很简单的清除浮动。 也可以配合`mixin`使用

```html
<div class="clearfix">...</div>
```

mixin源代码：
```scss
@mixin clearfix() {
  &::after {
    display: block;
    clear: both;
    content: "";
  }
}
```
在SCSS中使用mixin：

```scss
.element {
  @include clearfix;
}
```

示例：

```demo
<div class="bg-light clearfix">
  <button type="button" class="btn btn-success float-left">Example Button floated left</button>
  <button type="button" class="btn btn-success float-right">Example Button floated right</button>
</div>
```

```html
<div class="bg-info clearfix">
  <button type="button" class="btn btn-success float-left">Example Button floated left</button>
  <button type="button" class="btn btn-success float-right">Example Button floated right</button>
</div>
```

## 多色链接 :id=colored_links

**悬停状态的彩色链接:** 你可以使用`.link-*`类为链接上色。与`.text-*`不同，这些具有 `:hover`和`:focus`状态。

```demo
<a href="#" class="link-primary mr-2">Primary link</a>
<a href="#" class="link-secondary mr-2">Secondary link</a>
<a href="#" class="link-success mr-2">Success link</a>
<a href="#" class="link-danger mr-2">Danger link</a>
<a href="#" class="link-warning mr-2">Warning link</a>
<a href="#" class="link-info mr-2">Info link</a>
<a href="#" class="link-light mr-2">Light link</a>
<a href="#" class="link-dark">Dark link</a>
```

```html
<a href="#" class="link-primary">Primary link</a>
<a href="#" class="link-secondary">Secondary link</a>
<a href="#" class="link-success">Success link</a>
<a href="#" class="link-danger">Danger link</a>
<a href="#" class="link-warning">Warning link</a>
<a href="#" class="link-info">Info link</a>
<a href="#" class="link-light">Light link</a>
<a href="#" class="link-dark">Dark link</a>
```

## 延伸链接

- 在拥有`position: relative`属性的元素（容器）中，只要给包含其中的`<a>`添加`.stretched-link`，使整个容器可点击。
- 它是通过给`<a>`添加`::after`伪元素来覆盖整个`position: relative;`容器来实现的。

```demo
<div class="card" style="width: 18rem;">
  <svg class="bd-placeholder-img card-img-top" width="100%" height="180" xmlns="http://www.w3.org/2000/svg" aria-label="Card image cap" preserveAspectRatio="xMidYMid slice" role="img" focusable="false"><title>Card image cap</title><rect width="100%" height="100%" fill="#868e96"></rect></svg>
  <div class="card-body">
    <h5 class="card-title">鼠标放进来试试</h5>
    <p class="card-text">以下链接添加了.stretched-link，使整个容器都可以被点击</p>
    <a href="#" class="btn btn-primary stretched-link">Go somewhere</a>
  </div>
</div>
```

```html
<div class="card" style="width: 18rem;">
  <img src="..." class="card-img-top" alt="...">
  <div class="card-body">
    <h5 class="card-title">鼠标放进来试试</h5>
    <p class="card-text">以下链接添加了.stretched-link，使整个容器都可以被点击</p>
    <a href="#" class="btn btn-primary stretched-link">Go somewhere</a>
  </div>
</div>
```

## Position

**固定顶部**

将一个元素固定到窗口的顶部

```html
<div class="fixed-top">...</div>
```

**固定底部**

```html
<div class="fixed-bottom">...</div>
```

**粘性顶部**

将元素始终悬浮定位在窗口的顶部`.sticky-top`是使用了CSS的`position.sticky-top`。
```html
<div class="sticky-top">...</div>

<!-- 响应式 -->
<div class="sticky-sm-top">...</div>
<div class="sticky-md-top">...</div>
<div class="sticky-lg-top">.../div>
<div class="sticky-xl-top">...</div>
```


## 文本截断

对于很长的内容，可以添加`.text-truncate`用省略号来截断文本。需要`display:inline-block`或`display:block`。

```demo
<!-- Block level -->
<span class="d-block text-truncate" style="max-width:10%;">
    Praeterea iter est quasdam res quas ex communi.
</span>

<!-- Inline level -->
<span class="d-inline-block text-truncate" style="max-width: 150px;">
  Praeterea iter est quasdam res quas ex communi.
</span>
```

```html
<!-- Block level -->
<span class="d-block text-truncate" style="max-width:10%;">
    Praeterea iter est quasdam res quas ex communi.
</span>

<!-- Inline level -->
<span class="d-inline-block text-truncate" style="max-width: 150px;">
  Praeterea iter est quasdam res quas ex communi.
</span>
```

## Embeds嵌入

通过创建可在任何设备上缩放的内在比率，根据父对象的宽度创建响应的视频或幻灯片嵌入

**关于：**

可以直接应用于`<iframe>`，`<embed>`，`<video>`和`<object>`元素；当你想为其他属性匹配样式时，可选择使用显式子类`.embed-responsive-item`。
> 特别提示! 你不需要在你的`<iframe>`中设置`frameborder="0"`，因为我们会在重启时覆盖它。

**示例：**

```demo
<div class="embed-responsive embed-responsive-16by9">
  <iframe class="embed-responsive-item" src="https://img.orchome.com/record/kafka_01.mp4" title="YouTube video" allowfullscreen></iframe>
</div>
```

```html
<div class="embed-responsive embed-responsive-16by9">
  <iframe class="embed-responsive-item" src="https://img.orchome.com/record/kafka_01.mp4" title="YouTube video" allowfullscreen></iframe>
</div>
```


**长宽比：**

可以使用modifier自定义长宽比`.embed-responsive-*`。默认情况下，提供以下比率类：

```html
<!-- 21:9 aspect ratio -->
<div class="embed-responsive embed-responsive-21by9">
  <iframe class="embed-responsive-item" src="..."></iframe>
</div>

<!-- 16:9 aspect ratio -->
<div class="embed-responsive embed-responsive-16by9">
  <iframe class="embed-responsive-item" src="..."></iframe>
</div>

<!-- 4:3 aspect ratio -->
<div class="embed-responsive embed-responsive-4by3">
  <iframe class="embed-responsive-item" src="..."></iframe>
</div>

<!-- 1:1 aspect ratio -->
<div class="embed-responsive embed-responsive-1by1">
  <iframe class="embed-responsive-item" src="..."></iframe>
</div>
```

在`_variables.scss`的源码中，您可以更改要使用的宽高比。 这是`$embed-responsive-aspect-ratios`映射的示例：

```scss
$embed-responsive-aspect-ratios: (
  "21by9": (
    x: 21,
    y: 9
  ),
  "16by9": (
    x: 16,
    y: 9
  ),
  "4by3": (
    x: 4,
    y: 3
  ),
  "1by1": (
    x: 1,
    y: 1
  )
);
```
