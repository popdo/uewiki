# 实用工具

## 工具api

> Utilities API是一个基于Sass的工具，用于生成实用工具类。

### api属性

`$utilities`映射包含所有实用工具，实用工具映射包含一个带有关键字的实用程序组列表，这些工具组接受以下选项：

> 点击属性名称可以跳转到相应的章节。

|属性|说明|
|--|--|
|[property](#property-新增)|添加实用工具：String或Array（可以自定义更多实用工具）|
|[responsible](#responsible-响应式)（可选）|响应式工具：默认:false,表示是否需要生成媒体响应类。|
|[class](#class-前缀)（可选）|自定义类前缀：变量，如果不喜欢原始类名则可以进行更改。如果数组中的第一个属性是key元素，那么就不要提供该类的第一个数组名。|
|[values](#values-更改)（可选）|更改实用工具：如果不希望类名与值相同，则可以是值列表或映射。如果使用null作为映射键，则不会呈现它。|
|[print](#print-打印)（可选）|打印实用工具：默认:false,指示是否需要生成打印类。|
|rfs（可选）|默认:false,启用流体重新缩放的变量。可以看看[RFS](https://v5.getbootstrap.com/docs/5.0/getting-started/rfs/)页面了解它是如何工作的。|

### property-新增

所有实用工具变量都将添加到`$utilities`变量中。我们可以这样添加自定义实用程序组：

```scss
$utilities: (
  "opacity": (
    property: opacity,
    values: (
      0: 0,
      25: .25,
      50: .5,
      100: 1,
    )
  )
 );
```

生成的css是这样的：

```css
.opacity-0 {opacity: 0;}
.opacity-25 {opacity: .25;}
.opacity-50 {opacity: .5;}
.opacity-100 {opacity: 1;}
```

### class-前缀

使用`class`选项，可以更改类前缀以达到更个性化的项目需求：示例中使用`class: o`

```scss
$utilities: (
  "opacity": (
    property: opacity,
    class: o,
    values: (
      0: 0,
      25: .25,
      50: .5,
      100: 1,
    )
  )
 );
```

最后生成的css是：

```css
.o-0 {opacity: 0;}
.o-25 {opacity: .25;}
.o-50 {opacity: .5;}
.o-100 {opacity: 1;}
```

### responsible-响应式

使用`responsive:true`选项，可以生成响应实用工具类：

```scss
$utilities: (
  "opacity": (
    property: opacity,
    responsive: true,
    values: (
      0: 0,
      25: .25,
      50: .5,
      100: 1,
    )
  )
 );
```

这样就生成每个媒体尺寸的响应式工具类：

```css
.opacity-0 {opacity: 0;}
.opacity-25 {opacity: .25;}
.opacity-75 {opacity: .75;}
.opacity-100 {opacity: 1;}

@media (min-width: 576px) {
  .opacity-sm-0 {opacity: 0;}
  .opacity-sm-25 {opacity: .25;}
  .opacity-sm-75 {opacity: .75;}
  .opacity-sm-100 {opacity: 1;}
}
@media (min-width: 768px) {
  .opacity-md-0 {opacity: 0;}
  .opacity-md-25 {opacity: .25;}
  .opacity-md-75 {opacity: .75;}
  .opacity-md-100 {opacity: 1;}
}
@media (min-width: 992px) {
  .opacity-lg-0 {opacity: 0;}
  .opacity-lg-25 {opacity: .25;}
  .opacity-lg-75 {opacity: .75;}
  .opacity-lg-100 {opacity: 1;}
}
@media (min-width: 1200px) {
  .opacity-xl-0 {opacity: 0;}
  .opacity-xl-25 {opacity: .25;}
  .opacity-xl-75 {opacity: .75;}
  .opacity-xl-100 {opacity: 1;}
}
```

### values-更改

通过使用相同的key可以重写exicing实用工具。例如，如果您想要更具响应性的溢出实用工具类可以执行以下操作：

```scss
$utilities: (
  "overflow": (
    responsive: true,
    property: overflow,
    values: visible hidden scroll auto,
  ),
);
```

### print-打印

启用`print:true`选项还将生成用于打印的实用程序类。

```scss
$utilities: (
  "opacity": (
    property: opacity,
    class: o,
    print: true,
    values: (
      0: 0,
      25: .25,
      50: .5,
      100: 1,
    )
  )
 );
```

输出结果类：

```css
.o-0 {opacity: 0;}
.o-25 {opacity: .25;}
.o-75 {opacity: .75;}
.o-100 {opacity: 1;}

@media print {
  .o-print-0 {opacity: 0;}
  .o-print-25 {opacity: .25;}
  .o-print-75 {opacity: .75;}
  .o-print-100 {opacity: 1;}
}
```

### 移除实用工具

也可以通过将组键更改为`null`来删除实用工具：

```scss
$utilities: (
  "float": null,
);
```

## Borders

设置边框：

```demo
<span class="border p-5 bg-light d-inline-block mr-2"></span>
<span class="border-top p-5 bg-light d-inline-block mr-2"></span>
<span class="border-right p-5 bg-light d-inline-block mr-2"></span>
<span class="border-bottom p-5 bg-light d-inline-block mr-2"></span>
<span class="border-left p-5 bg-light d-inline-block"></span>
```

```html
<span class="border"></span>
<span class="border-top"></span>
<span class="border-right"></span>
<span class="border-bottom"></span>
<span class="border-left"></span>
```

排除边框：

```demo
<span class="border border-0 p-5 bg-light d-inline-block mr-2"></span>
<span class="border border-top-0 p-5 bg-light d-inline-block mr-2"></span>
<span class="border border-right-0 p-5 bg-light d-inline-block mr-2"></span>
<span class="border border-bottom-0 p-5 bg-light d-inline-block mr-2"></span>
<span class="border border-left-0 p-5 bg-light d-inline-block"></span>
```

```html
<span class="border-0"></span>
<span class="border-top-0"></span>
<span class="border-right-0"></span>
<span class="border-bottom-0"></span>
<span class="border-left-0"></span>
```

边框颜色：

```demo
<span class="border border-primary p-4 bg-light d-inline-block mr-2"></span>
<span class="border border-secondary p-4 bg-light d-inline-block mr-2"></span>
<span class="border border-success p-4 bg-light d-inline-block mr-2"></span>
<span class="border border-danger p-4 bg-light d-inline-block mr-2"></span>
<span class="border border-warning p-4 bg-light d-inline-block mr-2"></span>
<span class="border border-info p-4 bg-light d-inline-block mr-2"></span>
<span class="border border-light p-4 bg-light d-inline-block mr-2"></span>
<span class="border border-dark p-4 bg-light d-inline-block mr-2"></span>
<span class="border border-white"></span>
```

```html
<span class="border border-primary"></span>
<span class="border border-secondary"></span>
<span class="border border-success"></span>
<span class="border border-danger"></span>
<span class="border border-warning"></span>
<span class="border border-info"></span>
<span class="border border-light"></span>
<span class="border border-dark"></span>
<span class="border border-white"></span>
```

## Radius

设置圆角：  

```demo
<span class="rounded p-4 bg-secondary d-inline-block mr-2 text-white">全圆角</span>
<span class="rounded-top p-4 bg-secondary d-inline-block mr-2 text-white">上圆角</span>
<span class="rounded-right p-4 bg-secondary d-inline-block mr-2 text-white">右圆角</span>
<span class="rounded-bottom p-4 bg-secondary d-inline-block mr-2 text-white">下圆角</span>
<span class="rounded-left p-4 bg-secondary d-inline-block mr-2 text-white">左圆角</span>
<span class="rounded-circle p-4 bg-secondary d-inline-block mr-2 text-white text-center" style="width:70px;height:70px">圆</span>
<span class="rounded-pill p-4 bg-secondary d-inline-block mr-2 text-white">半径圆</span>
<span class="rounded rounded-0 p-4 bg-secondary d-inline-block text-white">无圆角</span>
```

```html
<span class="rounded">全圆角</span>
<span class="rounded-top">上圆角</span>
<span class="rounded-right">右圆角</span>
<span class="rounded-bottom">下圆角</span>
<span class="rounded-left">左圆角</span>
<span class="rounded-circle">圆</span>
<span class="rounded-pill">半径圆</span>
<span class="rounded-0">无圆角</span>
```

圆角尺寸：

```demo
<span class="rounded-sm p-4 bg-secondary d-inline-block mr-2 text-white">小圆角</span>
<span class="rounded p-4 bg-secondary d-inline-block mr-2 text-white">中圆角</span>
<span class="rounded-lg p-4 bg-secondary d-inline-block text-white">大圆角</span>
```

```html
<span class="rounded-sm">小圆角</span>
<span class="rounded">中圆角</span>
<span class="rounded-lg">大圆角</span>
```

## Colors

### 情境文本颜色

使用颜色工具为文本着色。如果您想给链接`<a>`着色，可以使用[.link-*helper](/bootstrap5/helpers?id=colored_links)类，这些类具有`:hover`和`:focus`状态。

```demo
<span class="text-primary mr-2">.text-primary</span>
<span class="text-secondary mr-2">.text-secondary</span>
<span class="text-success mr-2">.text-success</span>
<span class="text-danger mr-2">.text-danger</span>
<span class="text-warning bg-dark mr-2">.text-warning</span>
<span class="text-info bg-dark mr-2">.text-info</span>
<span class="text-light bg-dark mr-2">.text-light</span>
<span class="text-dark mr-2">.text-dark</span>
<span class="text-body mr-2">.text-body</span>
<span class="text-muted mr-2">.text-muted</span>
<span class="text-white bg-dark mr-2">.text-white</span>
<span class="text-black-50 mr-2">.text-black-50</span>
<span class="text-white-50 bg-dark">.text-white-50</span>
```

```html
<span class="text-primary">.text-primary</span>
<span class="text-secondary">.text-secondary</span>
<span class="text-success">.text-success</span>
<span class="text-danger">.text-danger</span>
<span class="text-warning bg-dark">.text-warning</span>
<span class="text-info bg-dark">.text-info</span>
<span class="text-light bg-dark">.text-light</span>
<span class="text-dark">.text-dark</span>
<span class="text-body">.text-body</span>
<span class="text-muted">.text-muted</span>
<span class="text-white bg-dark">.text-white</span>
<span class="text-black-50">.text-black-50</span>
<span class="text-white-50 bg-dark">.text-white-50</span>
```

### 背景颜色

```demo
<span class="p-3 mr-2 bg-primary text-white d-inline-block">.bg-primary</span>
<span class="p-3 mr-2 bg-secondary text-white">.bg-secondary</span>
<span class="p-3 mr-2 bg-success text-white">.bg-success</span>
<span class="p-3 mr-2 bg-danger text-white">.bg-danger</span>
<span class="p-3 mr-2 bg-warning text-white">.bg-warning</span>
<span class="p-3 mr-2 bg-info text-white">.bg-info</span>
<span class="p-3 mr-2 bg-light text-dark">.bg-light</span>
<span class="p-3 mr-2 bg-dark text-white">.bg-dark</span>
<span class="p-3 mr-2 bg-white text-dark">.bg-white</span>
<span class="p-3 bg-transparent text-dark">.bg-transparent</span>
```

```html
<div class="bg-primary">.bg-primary</div>
<div class="bg-secondary">.bg-secondary</div>
<div class="bg-success">.bg-success</div>
<div class="bg-danger">.bg-danger</div>
<div class="bg-warning">.bg-warning</div>
<div class="bg-info">.bg-info</div>
<div class="bg-light">.bg-light</div>
<div class="bg-dark">.bg-dark</div>
<div class="bg-white">.bg-white</div>
<div class="bg-transparent">.bg-transparent</div>
```

### 渐变背景颜

通过添加`.bg-gradient`类，可以将线性渐变作为背景图像添加到背景中。 此渐变从半透明的白色开始，逐渐淡出到底部。你的自定义CSS是否需要渐变？ 只需添加`background-image: var(--bs-gradient)`;

```demo
<span class="bg-gradient p-3 mr-2 bg-primary text-white d-inline-block">.bg-primary</span>
<span class="bg-gradient p-3 mr-2 bg-secondary text-white">.bg-secondary</span>
<span class="bg-gradient p-3 mr-2 bg-success text-white">.bg-success</span>
<span class="bg-gradient p-3 mr-2 bg-danger text-white">.bg-danger</span>
<span class="bg-gradient p-3 mr-2 bg-warning text-white">.bg-warning</span>
<span class="bg-gradient p-3 mr-2 bg-info text-white">.bg-info</span>
<span class="bg-gradient p-3 mr-2 bg-light text-dark">.bg-light</span>
<span class="bg-gradient p-3 bg-dark text-white">.bg-dark</span>
```

```html
<div class="bg-gradient bg-primary">.bg-primary</div>
<div class="bg-gradient bg-secondary">.bg-secondary</div>
<div class="bg-gradient bg-success">.bg-success</div>
<div class="bg-gradient bg-danger">.bg-danger</div>
<div class="bg-gradient bg-warning">.bg-warning</div>
<div class="bg-gradient bg-info">.bg-info</div>
<div class="bg-gradient bg-light">.bg-light</div>
<div class="bg-gradient bg-dark">.bg-dark</div>
```

## Display

bootstrap支持所有display属性的类写法，具体如下：

|css属性|类写法|
|--|--|
|display:none|.d-none|
|display:nline|.d-inline|
|display:inline-block|.d-inline-block|
|display:block|.d-block|
|display:table|.d-table|
|display:table-cell|.d-table-cell|
|display:table-row|.d-table-row|
|display:flex|.d-flex|
|display:inline-flex|.d-inline-flex|

可以通过修改源码`$displays`变量和重新编译SCSS来改变属性值。

### 响应式display

> `.d-*`的类名支持所有屏幕尺寸的媒体,我们只需要书写`.d-{sm,md,lg,xl,xxl}-*`,例如：`.d-sm-block`、`.d-lg-inline-block`

### 响应式隐藏

为了更快更友好的进行移动开发，使用响应式显示类，按设备来显示和隐藏元素。

- 要隐藏元素，只需使用`.d-none`类或`.d-{sm,md,lg,xl,xxl}-none`类中的一个，即可实现任何响应式屏幕变化。  
- 要在给定的屏幕尺寸区间上显示一个元素，就可以用如下表格的方式进行区间设置。

|屏幕大小|类名称|
|--|--|
|隐藏所有|`.d-none`|
|仅在xs上隐藏|`.d-none` `.d-sm-block`|
|仅在sm上隐藏|`.d-sm-none` `.d-md-block`|
|仅在md上隐藏|`.d-md-none` `.d-lg-block`|
|仅在lg隐藏|`.d-lg-none` `.d-xl-block`|
|仅在xl隐藏|`.d-xl-none`|
|仅在xxl隐藏|`.d-xxl-none`|
|显示所有|`.d-block`|
|仅在xs上可见|`.d-block` `.d-sm-none`|
|仅在sm上可见|`.d-none` `.d-sm-block` `.d-md-none`|
|仅在md上可见|`.d-none` `.d-md-block` `.d-lg-none`|
|仅在lg上可见|`.d-none` `.d-lg-block` `.d-xl-none`|
|仅在xl上可见|`.d-none` `.d-xl-block` `.d-xxl-none`|
|仅在xxl上可见|`.d-none` `.d-xxl-block`|

```demo
<div class="d-lg-none">隐藏在lg和更宽的屏幕上</div>
<div class="d-none d-lg-block">隐藏在比lg更小的屏幕上</div>
```

```html
<div class="d-lg-none">隐藏在lg和更宽的屏幕上</div>
<div class="d-none d-lg-block">隐藏在比lg更小的屏幕上</div>
```

### 打印型显示

当使用打印`display`类来打印时，改变元素的`display`值。包括支持与响应式`.d-*`相同的显示值。

- .d-print-none
- .d-print-inline
- .d-print-inline-block
- .d-print-block
- .d-print-table
- .d-print-table-row
- .d-print-table-cell
- .d-print-flex
- .d-print-inline-flex

打印类和显示类可以合并。

```demo
<div class="d-print-none">Screen Only (Hide on print only)</div>
<div class="d-none d-print-block">Print Only (Hide on screen only)</div>
<div class="d-none d-lg-block d-print-block">Hide up to large on screen, but always show on print</div>
```

```html
<div class="d-print-none">Screen Only (Hide on print only)</div>
<div class="d-none d-print-block">Print Only (Hide on screen only)</div>
<div class="d-none d-lg-block d-print-block">Hide up to large on screen, but always show on print</div>
```

## Float

使用我们的响应式浮动实用工具，可以在任何断点的任何元素上切换浮动。也支持全响应式设备浮动`.float-{sm,md,lg,xl,xxl}-*`

```demo
<div class="float-left">float-left</div><br>
<div class="float-right">float-right</div><br>
<div class="float-none">float-none</div>
<hr>
<div class="float-sm-right">Float right on viewports sized SM (small) or wider</div><br>
<div class="float-md-right">Float right on viewports sized MD (medium) or wider</div><br>
<div class="float-lg-right">Float right on viewports sized LG (large) or wider</div><br>
<div class="float-xl-right">Float right on viewports sized XL (extra-large) or wider</div><br>
```

```html
<div class="float-left">float-left</div><br>
<div class="float-right">float-right</div><br>
<div class="float-none">float-none</div>

<!-- 也支持全尺寸的响应式 -->
<div class="float-sm-right">Float right on viewports sized SM (small) or wider</div><br>
<div class="float-md-right">Float right on viewports sized MD (medium) or wider</div><br>
<div class="float-lg-right">Float right on viewports sized LG (large) or wider</div><br>
<div class="float-xl-right">Float right on viewports sized XL (extra-large) or wider</div><br>
```

## Interactions

> 用于改变用户与网站内容的交互方式的实用类。

### 文本选择

改变用户与内容交互时的选择方式。

```demo
<p class="user-select-all">当用户点击时，这一段将完全被选中。</p>
<p class="user-select-auto">本段有默认选择行为。</p>
<p class="user-select-none">当用户点击时，该段将无法选择。</p>
```

```html
<p class="user-select-all">当用户点击时，这一段将完全被选中。</p>
<p class="user-select-auto">本段有默认选择行为。</p>
<p class="user-select-none">当用户点击时，该段将无法选择。</p>
```

### 指针事件

Bootstrap提供了 `pe-none` 和 `pe-auto`类来防止或添加元素交互。

```demo
<p><a href="#" class="pe-none">此连接</a> 不能点击</p>
<p><a href="#" class="pe-auto">此链接</a> 能被点击 (默认).</p>
<p class="pe-none"><a href="#">此链接</a> 不能点击，是由于<code>pointer-events</code>属性是从其父级继承的，但是, <a href="#" class="pe-auto">此链接</a> 设置了 <code>pe-auto</code> 所以可以被点击</p>
```

```html
<p><a href="#" class="pe-none">此连接</a> 不能点击</p>
<p><a href="#" class="pe-auto">此链接</a> 能被点击 (默认).</p>
<p class="pe-none">
    <a href="#">此链接</a> 不能点击，是由于<code>pointer-events</code>属性是从其父级继承的，但是, <a href="#" class="pe-auto">此链接</a> 设置了 <code>pe-auto</code> 所以可以被点击
</p>

```

## Overflow

默认情况下，`overflow`功能两个值提供，而且它们不是响应的.
通过`_variables.scss`的源码可以对`$overflows`进行自定义

```demo
<div class="bd-example d-md-flex">
  <div class="overflow-auto p-3 mb-3 mb-md-0 mr-md-3 bg-light" style="max-width: 260px; max-height: 100px;">
    This is an example of using <code>.overflow-auto</code> on an element with set width and height dimensions. By design, this content will vertically scroll.
  </div>
  <div class="overflow-hidden p-3 bg-light" style="max-width: 260px; max-height: 100px;">
    This is an example of using <code>.overflow-hidden</code> on an element with set width and height dimensions.
  </div>
</div>
```

```html
<div class="overflow-auto">...</div>
<div class="overflow-hidden">...</div>
```

## Position

使用这些速记实用工具可以快速配置元素的位置。他们不支持设备的响应式

```html
<div class="position-static">...</div>
<div class="position-relative">...</div>
<div class="position-absolute">...</div>
<div class="position-fixed">...</div>
<div class="position-sticky">...</div>
```

## Shadows

阴影效果目前支持三种尺寸。

```demo
<div class="shadow-none p-3 mb-5 bg-light rounded">No shadow</div>
<div class="shadow-sm p-3 mb-5 bg-white rounded">Small shadow</div>
<div class="shadow p-3 mb-5 bg-white rounded">Regular shadow</div>
<div class="shadow-lg p-3 mb-5 bg-white rounded">Larger shadow</div>
```

```html
<div class="shadow-none">No shadow</div>
<div class="shadow-sm">Small shadow</div>
<div class="shadow">Regular shadow</div>
<div class="shadow-lg">Larger shadow</div>
```

## Sizing

- `宽度`和`高度`实用工具默认情况下包括对`25%`、`50%`、`75%`、`100%`和`自动`的支持。
- 需要自定义他们可以通过[API](#工具api)对`_utilities.scss`进行定制

### 宽度

```demo
<div class="w-25 p-2" style="background-color: #efefef;">Width 25%</div>
<div class="w-50 p-2" style="background-color: #eaeaea;">Width 50%</div>
<div class="w-75 p-2" style="background-color: #efefef;">Width 75%</div>
<div class="w-100 p-2" style="background-color: #eaeaea;">Width 100%</div>
<div class="w-auto p-2" style="background-color: #efefef;">Width auto</div>
```

```html
<div class="w-25">Width 25%</div>
<div class="w-50">Width 50%</div>
<div class="w-75">Width 75%</div>
<div class="w-100">Width 100%</div>
<div class="w-auto">Width auto</div>
```

### 高度

```demo
<div style="height: 100px; background-color: rgba(255,0,0,0.1);">
  <div class="h-25 d-inline-block" style="width: 120px; background-color: rgba(0,0,255,.1)">Height 25%</div>
  <div class="h-50 d-inline-block" style="width: 120px; background-color: rgba(0,0,255,.1)">Height 50%</div>
  <div class="h-75 d-inline-block" style="width: 120px; background-color: rgba(0,0,255,.1)">Height 75%</div>
  <div class="h-100 d-inline-block" style="width: 120px; background-color: rgba(0,0,255,.1)">Height 100%</div>
  <div class="h-auto d-inline-block" style="width: 120px; background-color: rgba(0,0,255,.1)">Height auto</div>
</div>
```

```html
<div class="h-25">height 25%</div>
<div class="h-50">height 50%</div>
<div class="h-75">height 75%</div>
<div class="h-100">height 100%</div>
<div class="h-auto">height auto</div>
```

### 最大宽高

很多时候我们总是需要设置`max-width: 100%;` 和 `max-height: 100%;`,我们当然也是支持

```html
<div class="mw-100">max-width: 100%</div>
<div class="mh-100">max-height: 100%</div>
```

### 浏览器视窗

也可以使用工具设置相对视窗的宽度和高度。

```html
<div class="min-vw-100">Min-width 100vw</div>
<div class="min-vh-100">Min-height 100vh</div>
<div class="vw-100">Width 100vw</div>
<div class="vh-100">Height 100vh</div>
```

## Spacing

通过`间距工具`可以在任意元素上轻松设置彼此之间的`x`、`y`轴的间距

|类前缀|说明|
|--|--|
|m|margin-|
|p|padding-|

|拼接项|说明|
|--|--|
|t| top|
|b| bottom |
|l| left |
|r| right |
|x| left + right |
|y| top + bottom |

|类后缀|说明|
|--|--|
|-0|0|
|-1|.25rem|
|-2|.5rem|
|-3|1rem|
|-4|1.5rem|
|-5|3rem|
|-auto|auto|

那么 `.mt-1` = `margin-top:.25rem;`或者 `.pb-3` = `padding-bottom:1rem;`

> 由于`margin`有负值，因此我们可以使用`n`代表负值，例如：`.ml-n3` = `margin-left:-1rem;`

?> **水平居中：** 此外，Bootstrap还包括一个`.mx-auto`类，用于通过将水平边距设置为auto来使居中固定宽度的块级内容(display:block) 水平居中。

```demo
<span class="d-block mx-auto" style="width: 200px;">
  Centered element
</span>
```

```html
<span class="d-block mx-auto" style="width: 200px;">
  Centered element
</span>
```

## Text

`text-align:{left,center,right}`文本对齐方式我们提供了相应的实用工具，并且支持媒体响应。

```demo
<p class="text-left">Left aligned text on all viewport sizes.</p>
<p class="text-center">Center aligned text on all viewport sizes.</p>
<p class="text-right">Right aligned text on all viewport sizes.</p>

<p class="text-sm-left">Left aligned text on viewports sized SM (small) or wider.</p>
<p class="text-md-left">Left aligned text on viewports sized MD (medium) or wider.</p>
<p class="text-lg-left">Left aligned text on viewports sized LG (large) or wider.</p>
<p class="text-xl-left">Left aligned text on viewports sized XL (extra-large) or wider.</p>
```

```html
<p class="text-left">Left aligned text on all viewport sizes.</p>
<p class="text-center">Center aligned text on all viewport sizes.</p>
<p class="text-right">Right aligned text on all viewport sizes.</p>

<p class="text-sm-left">Left aligned text on viewports sized SM (small) or wider.</p>
<p class="text-md-left">Left aligned text on viewports sized MD (medium) or wider.</p>
<p class="text-lg-left">Left aligned text on viewports sized LG (large) or wider.</p>
<p class="text-xl-left">Left aligned text on viewports sized XL (extra-large) or wider.</p>
```

### 文本换行和溢出

|类名|说明|
|--|--|
|.text-wrap|文本换行|
|.text-nowrap|文本不换行|
|.text-break|强制换行，防止长英文字符破坏布局|

### 文字变形

使用文本大小写类转换组件中的文本。

```demo
<p class="text-lowercase">Lowercased text.</p>
<p class="text-uppercase">Uppercased text.</p>
<p class="text-capitalize">CapiTaliZed text.</p>
```

```html
<p class="text-lowercase">Lowercased text.</p>
<p class="text-uppercase">Uppercased text.</p>
<p class="text-capitalize">CapiTaliZed text.</p>
```

### 字体粗细和斜体

```demo
<p class="font-weight-bold">超粗体：Bold text.</p>
<p class="font-weight-bolder">粗体：Bolder weight text (relative to the parent element).</p>
<p class="font-weight-normal">常规：Normal weight text.</p>
<p class="font-weight-light">细体：Light weight text.</p>
<p class="font-weight-lighter">超细体：Lighter weight text (relative to the parent element).</p>
<p class="font-italic">斜体：Italic text.</p>
<p class="font-normal">常规风格：（font-style）Text without font style</p>
```

```html
<p class="font-weight-bold">超粗体：Bold text.</p>
<p class="font-weight-bolder">粗体：Bolder weight text (relative to the parent element).</p>
<p class="font-weight-normal">常规：Normal weight text.</p>
<p class="font-weight-light">细体：Light weight text.</p>
<p class="font-weight-lighter">超细体：Lighter weight text (relative to the parent element).</p>
<p class="font-italic">斜体：Italic text.</p>
<p class="font-normal">常规风格：（font-style）Text without font style</p>
```

### 行高

```demo
<p class="lh-1">Vivamus sagittis lacus vel augue laoreet rutrum faucibus dolor auctor. Donec sed odio dui. Cras mattis pannenkoek purus sit amet fermentum. Praesent commodo cursus magna, vel scelerisque nisl consectetur et. Nullam id dolor id nibh ultricies vehicula ut id elit. Cras mattis consectetur purus sit amet fermentum.</p>
<p class="lh-sm">Vivamus sagittis lacus vel augue laoreet rutrum faucibus dolor auctor. Donec sed odio dui. Cras mattis pannenkoek purus sit amet fermentum. Praesent commodo cursus magna, vel scelerisque nisl consectetur et. Nullam id dolor id nibh ultricies vehicula ut id elit. Cras mattis consectetur purus sit amet fermentum.</p>
<p class="lh-base">Vivamus sagittis lacus vel augue laoreet rutrum faucibus dolor auctor. Donec sed odio dui. Cras mattis pannenkoek purus sit amet fermentum. Praesent commodo cursus magna, vel scelerisque nisl consectetur et. Nullam id dolor id nibh ultricies vehicula ut id elit. Cras mattis consectetur purus sit amet fermentum.</p>
<p class="lh-lg">Vivamus sagittis lacus vel augue laoreet rutrum faucibus dolor auctor. Donec sed odio dui. Cras mattis pannenkoek purus sit amet fermentum. Praesent commodo cursus magna, vel scelerisque nisl consectetur et. Nullam id dolor id nibh ultricies vehicula ut id elit. Cras mattis consectetur purus sit amet fermentum.</p>
```

```html
<p class="lh-1">...</p>
<p class="lh-sm">...</p>
<p class="lh-base">...</p>
<p class="lh-lg">...</p>
```

### 等宽字体

使用`.font-monospace`将所选内容更改为等宽字体排版

```demo
<p class="font-monospace">This is in monospace</p>
```

```html
<p class="font-monospace">This is in monospace</p>
```

### 重置文本颜色

使用.text Reset重置文本或链接的颜色，使其继承其父项的颜色。`.text-reset`所代表的css是`color: inherit !important`

```demo
<p class="text-muted">
  muted text with a <a href="#" class="text-reset">reset link</a>.
</p>
```

```html
<p class="text-muted">
  muted text with a <a href="#" class="text-reset">reset link</a>.
</p>
```

### 文本修饰

```demo
<p class="text-decoration-underline">This text has a line underneath it.</p>
<p class="text-decoration-line-through">This text has a line going through it.</p>
<a href="#" class="text-decoration-none">This link has its text decoration removed</a>
```

```html
<p class="text-decoration-underline">This text has a line underneath it.</p>
<p class="text-decoration-line-through">This text has a line going through it.</p>
<a href="#" class="text-decoration-none">This link has its text decoration removed</a>
```

## 垂直对齐

使用`垂直对齐`工具`.align-*`改变元素的`vertical-alignment`对齐方式。请注意，垂直对齐只影响`inline`、`inline-block`、`inline-table`和`table`单元格元素。

对于内联元素：

```demo
<span class="align-baseline">baseline</span>
<span class="align-top">top</span>
<span class="align-middle">middle</span>
<span class="align-bottom">bottom</span>
<span class="align-text-top">text-top</span>
<span class="align-text-bottom">text-bottom</span>
```

```html
<span class="align-baseline">baseline</span>
<span class="align-top">top</span>
<span class="align-middle">middle</span>
<span class="align-bottom">bottom</span>
<span class="align-text-top">text-top</span>
<span class="align-text-bottom">text-bottom</span>
```

对于表格单元格：

```demo
<table style="height:100px;display:table">
  <tbody>
    <tr>
      <td class="align-baseline">baseline</td>
      <td class="align-top">top</td>
      <td class="align-middle">middle</td>
      <td class="align-bottom">bottom</td>
      <td class="align-text-top">text-top</td>
      <td class="align-text-bottom">text-bottom</td>
    </tr>
  </tbody>
</table>
```

```html
<table style="height:100px;display:table">
  <tbody>
    <tr>
      <td class="align-baseline">baseline</td>
      <td class="align-top">top</td>
      <td class="align-middle">middle</td>
      <td class="align-bottom">bottom</td>
      <td class="align-text-top">text-top</td>
      <td class="align-text-bottom">text-bottom</td>
    </tr>
  </tbody>
</table>
```

## Visibility

Visibility可见性的显示与隐藏的类名：

```html
<div class="visible">...</div>
<div class="invisible">...</div>
```

类名所代表的css样式：

```css
.visible {
  visibility: visible !important;
}
.invisible {
  visibility: hidden !important;
}
```
