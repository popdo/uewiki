# 布局

Bootstrap 提供了一套响应式、移动设备优先的流式栅格系统，随着屏幕或视口（viewport）尺寸的增加，系统会自动分为最多12列。它包含了易于使用的预定义类，还有强大的`mixin` 用于生成更具语义的布局。

## 容器断点表

容器是Bootstrap中最基本的布局元素，在我们的默认网格系统时需要。容器用于包含、填充和（有时）居中的内容。虽然容器可以嵌套，但大多数布局并不需要嵌套的容器。

Bootstrap有三个不同的容器。

- `.container`, 在每个响应断点处设置最大宽度
- `.container-fluid`, 在所有断点处width:100%。
- `.container-{breakpoint}`, width:100%直到指定断点

下表说明了每个容器的`max-width`在每种容器断点下的比较。

| Class name         | Extra small  *<576px*     | Small   *≥576px*     | Medium  *≥768px*     | Large  *≥992px*     | X\-Large  *≥1200px*     | XX\-Large  *≥1400px*     |
|--------------------|---------------------------|----------------------|----------------------|---------------------|-------------------------|--------------------------|
| `.container`       | 100%                      | 540px                | 720px                | 960px               | 1140px                  | 1320px                   |
| `.container-sm`    | 100%                      | 540px                | 720px                | 960px               | 1140px                  | 1320px                   |
| `.container-md`    | 100%                      | 100%                 | 720px                | 960px               | 1140px                  | 1320px                   |
| `.container-lg`    | 100%                      | 100%                 | 100%                 | 960px               | 1140px                  | 1320px                   |
| `.container-xl`    | 100%                      | 100%                 | 100%                 | 100%                | 1140px                  | 1320px                   |
| `.container-xxl`   | 100%                      | 100%                 | 100%                 | 100%                | 100%                    | 1320px                   |
| `.container-fluid` | 100%                      | 100%                 | 100%                 | 100%                | 100%                    | 100%                     |

## Grid-栅格参数表

栅格系统用于通过一系列的行（row）与列（column）的组合来创建页面布局，你的内容就可以放入这些创建好的布局中。

通过下表可以详细查看 Bootstrap 的栅格系统是如何在多种屏幕设备上工作的。

| name            | xs <576px                | sm  ≥576px  | md  ≥768px  | lg  ≥992px  | xl  ≥1200px | xxl  ≥1400px |
|-----------------|--------------------------|-------------|-------------|-------------|-------------|--------------|
| 容器的max-width  | None(auto)               | 540px       | 720px       | 960px       | 1140px      | 1320px       |
| 类前缀           | `.col`                   | `.col-sm-`  | `.col-md-`  | `.col-lg-`  | `.col-xl-`  | `.col-xxl-`  |
| \# of columns   | 12                       |             |             |             |             |              |
| 槽(Gutter)宽     | 1\.5rem \(每列左和右\.75rem\) |             |             |             |             |              |
| 自定义槽          | Yes                      |             |             |             |             |              |
| 可嵌套           | Yes                      |             |             |             |             |              |
| 列排序           | Yes                      |             |             |             |             |              |

## row类对照表

| 类名                                   |响应类| 说明                       |
|-----------------------------|-------|---------------|
|`.row`                                 |           |                  |
|`.row-cols-{1~12}`             |`.row-cols-{breakpoint}-{1~12}` |通过row批量设置col布局|
|`.g-{1~5}`                       | `.g-{breakpoint}-{1~5}` |col之间水平+垂直间距(槽宽)(若溢出 外层加.overfollow-hidden)||
|`.gx-{1~5}`                       | `.gx-{breakpoint}-{1~5}` |col之间水平间距(槽宽)||
|`.gy-{1~5}`                        |`.gy-{breakpoint}-{1~5}` |col之间垂直间距(槽宽)||
|`.row.align-items-start`    | |整个row居于容器垂直顶部|
|`.row.align-items-center`    | |整个row居于容器垂直居中|
|`.row.align-items-end`   | |整个row居于容器垂直底部|
|`.row.justify-content-start`   | |row内元素水平左对齐|
|`.row.justify-content-center`   | |row内元素水平居中对齐|
|`.row.justify-content-end`   | |row内元素水平右对齐|
|`.row.justify-content-around`   | |row内元素水平等分对齐|
|`.row.justify-content-between`   | |row内元素水平左---右对齐|
|`.row.justify-content-evenly`   | |row内元素水平evenly对齐|

> - **Gutters** (槽宽)默认是1.5rem（20px）。这使我们能够根据padding和margin spacers的比例来匹配我们的网格。

## col类对照表

| 类名                                   |响应类|  说明              |
|-----------------------------|-------|---------------|
| `.col`                                  |          |自动宽度布局                 |
| `.col-{1~12}`                      |`.col-{breakpoint}-{1~12}` |按比例布局 |
| `.col-auto`    |`.col-{breakpoint}-auto`| 按内容宽度自动布局 |
|`.offset-{1~12}`|`.offset-{breakpoint}-{1~12}`|当前col水平偏移量设置|
|`.order-first`              |  |当前col放置到第一个位置|
|`.order-last`              |  |当前col放置到最后一个位置|
|`.order-{1~5}`              |  |当前col位置排序|
| `.col.align-self-start`  |  | 当前col居容器垂直顶部 |
| `.col.align-self-center`  |  | 当前col居容器垂直居中 |
| `.col.align-self-end`  |  | 当前col居容器垂直底部 |

> - **col分段：** 在多个col之间插入`width:100%`的元素（例如`<div class="w-100 d-none"></div>`），可以让col分段换行。
> - **m-auto：** 利用flexbox的特性，你可以使用像`.mr-auto`这样的margin实用工具来强制分开兄弟列之间的距离。
> - **col单独使用：** col可以脱离row进行单独使用。例如：`<p><div class="col-3">我的宽度是25%</div></p>`。
> - **col换行：** 如果一行中有超过12列，则每一组额外超出的列将作为一个单元换行。

## Sass定制

### 媒体断点sass

这些断点可以通过Sass源码进行定制，您可以在我们的sass源码`_variables.scss`中找到他们。

| Breakpoint        | Class infix | Dimensions |
|-------------------|-------------|------------|
| X\-Small          | None        | 0–576px    |
| Small             | `sm`          | ≥576px     |
| Medium            | `md`          | ≥768px     |
| Large             | `lg`          | ≥992px     |
| Extra large       | `xl`          | ≥1200px    |
| Extra extra large | `xxl`         | ≥1400px    |

```scss
$grid-breakpoints: (
  xs: 0,
  sm: 576px,
  md: 768px,
  lg: 992px,
  xl: 1200px,
  xxl: 1400px
);
```

<!-- tabs:start -->

#### **Min-width**

Bootstrap在Sass源代码中为布局、网格系统和组件使用以下媒体查询范围的断点。

```scss
// Source mixins

// No media query necessary for xs breakpoint as it's effectively `@media (min-width: 0) { ... }`
@include media-breakpoint-up(sm) { ... }
@include media-breakpoint-up(md) { ... }
@include media-breakpoint-up(lg) { ... }
@include media-breakpoint-up(xl) { ... }
@include media-breakpoint-up(xxl) { ... }

// Usage

// Example: Hide starting at `min-width: 0`, and then show at the `sm` breakpoint
.custom-class {
  display: none;
}
@include media-breakpoint-up(sm) {
  .custom-class {
    display: block;
  }
}
```

这些Sass mixin编译之后的css示例：

```scss
// X-Small devices (portrait phones, less than 576px)
// No media query for `xs` since this is the default in Bootstrap

// Small devices (landscape phones, 576px and up)
@media (min-width: 576px) { ... }

// Medium devices (tablets, 768px and up)
@media (min-width: 768px) { ... }

// Large devices (desktops, 992px and up)
@media (min-width: 992px) { ... }

// X-Large devices (large desktops, 1200px and up)
@media (min-width: 1200px) { ... }

// XX-Large devices (larger desktops, 1400px and up)
@media (min-width: 1400px) { ... }
```

#### **Max-width**

我们偶尔会使用相反方向的媒体查询（给定屏幕大小或更小）：

```scss
// No media query necessary for xs breakpoint as it's effectively `@media (max-width: 0) { ... }`
@include media-breakpoint-down(sm) { ... }
@include media-breakpoint-down(md) { ... }
@include media-breakpoint-down(lg) { ... }
@include media-breakpoint-down(xl) { ... }
@include media-breakpoint-down(xxl) { ... }

// Example: Style from medium breakpoint and down
@include media-breakpoint-down(md) {
  .custom-class {
    display: block;
  }
}
```

这些mixin获取那些声明的断点，从中减去.02px，并将它们用作我们的最大宽度值。例如：

```scss
// X-Small devices (portrait phones, less than 576px)
@media (max-width: 575.98px) { ... }

// Small devices (landscape phones, less than 768px)
@media (max-width: 767.98px) { ... }

// Medium devices (tablets, less than 992px)
@media (max-width: 991.98px) { ... }

// Large devices (desktops, less than 1200px)
@media (max-width: 1199.98px) { ... }

// X-Large devices (large desktops, less than 1400px)
@media (max-width: 1399.98px) { ... }

// XX-Large devices (larger desktops)
// No media query since the xxl breakpoint has no upper bound on its width
```

#### **单个断点**

还有媒体查询和mixin，可以使用最小和最大断点宽度来定位屏幕大小的单个片段。

```scss
@include media-breakpoint-only(xs) { ... }
@include media-breakpoint-only(sm) { ... }
@include media-breakpoint-only(md) { ... }
@include media-breakpoint-only(lg) { ... }
@include media-breakpoint-only(xl) { ... }
@include media-breakpoint-only(xxl) { ... }
```

例如`@include media-breakpoint-only(md) { ... }`输出的结果是：

```css
@media (min-width: 768px) and (max-width: 991.98px) { ... }
```

#### **断点跨度**

同样，媒体查询可能跨越多个断点宽度：

```scss
@include media-breakpoint-between(md, xl) { ... }
```

输出结果是：

```css
@media (min-width: 768px) and (max-width: 1199.98px) { ... }
```

<!-- tabs:end -->

### 容器sass定制

Bootstrap生成了一系列预定义的容器类，以帮助你构建你想要的布局。您可以通过修改为它们提供的 Sass 映射（在`_variables.scss`中找到）来定制这些预定义的容器类。

```scss
$container-max-widths: (
  sm: 540px,
  md: 720px,
  lg: 960px,
  xl: 1140px,
  xxl: 1320px
);
```

除了定制Sass，你还可以用我们的Sass mixin创建自己的容器。

```scss
// Source mixin
@mixin make-container($padding-x: $container-padding-x) {
  width: 100%;
  padding-right: $padding-x;
  padding-left: $padding-x;
  margin-right: auto;
  margin-left: auto;
}

// Usage
.custom-container {
  @include make-container();
}
```

### 栅格sass定制

当使用Bootstrap的源代码Sass文件时，您可以选择使用Sass变量和mixins来创建自定义的、语义的和响应式的页面布局。我们预定义的网格类使用这些相同的变量和混搭，为快速响应式布局提供了一整套现成的类。

#### 变量

变量和map决定了列的数量、沟槽宽度和开始浮动列的media查询点。我们使用这些变量和map来生成上面记录的预定义网格类，以及下面列出的自定义混搭。

```scss
$grid-columns:      12;
$grid-gutter-width: 1.5rem;
```

```scss
$grid-breakpoints: (
  xs: 0,
  sm: 576px,
  md: 768px,
  lg: 992px,
  xl: 1200px,
  xxl: 1400px
);
```

```scss
$container-max-widths: (
  sm: 540px,
  md: 720px,
  lg: 960px,
  xl: 1140px,
  xxl: 1320px
);
```

#### Mixins

Mixins与网格变量一起使用，为各个网格列生成语义CSS。

```scss
// Creates a wrapper for a series of columns
@include make-row();

// Make the element grid-ready (applying everything but the width)
@include make-col-ready();
@include make-col($size, $columns: $grid-columns);

// Get fancy by offsetting, or changing the sort order
@include make-col-offset($size, $columns: $grid-columns);
```

#### 使用实例

你可以将变量修改为你自己的自定义值，或者直接使用mixins的默认值。下面是一个使用默认设置来创建两栏布局的例子，中间有空隙。

```scss
.example-container {
  @include make-container();
  // Make sure to define this width after the mixin to override
  // `width: 100%` generated by `make-container()`
  width: 800px;
}

.example-row {
  @include make-row();
}

.example-content-main {
  @include make-col-ready();

  @include media-breakpoint-up(sm) {
    @include make-col(6);
  }
  @include media-breakpoint-up(lg) {
    @include make-col(8);
  }
}

.example-content-secondary {
  @include make-col-ready();

  @include media-breakpoint-up(sm) {
    @include make-col(6);
  }
  @include media-breakpoint-up(lg) {
    @include make-col(4);
  }
}
```

```html
<div class="example-container">
  <div class="example-row">
    <div class="example-content-main">Main content</div>
    <div class="example-content-secondary">Secondary content</div>
  </div>
</div>
```

### 自定义栅格

使用我们内置的网格Sass变量和地图，可以完全定制预定义的网格类。改变层数、媒体查询尺寸和容器宽度，然后重新编译。

#### Columns 和 gutters

网格列的数量可以通过Sass变量来修改，`$grid-columns`用于生成每个单独列的宽度（百分比），而`$grid-gutter-width`则设置了列槽的宽度。`$grid-columns`用于生成每个单独列的宽度（百分比），而`$grid-gutter-width`则设置列槽的宽度。

```scss
$grid-columns: 12 !default;
$grid-gutter-width: 1.5rem !default;
```

#### 栅格层

除了列本身，你还可以自定义网格层数。如果你只想要四层网格，你可以更新`$grid-breakpoints`和`$container-max-widths`，就像这样。

```scss
$grid-breakpoints: (
  xs: 0,
  sm: 480px,
  md: 768px,
  lg: 1024px
);

$container-max-widths: (
  sm: 420px,
  md: 720px,
  lg: 960px
);
```

当对Sass变量或map进行任何更改时，你需要保存你的更改并重新编译。然后输出一组全新的预定义网格类，用于列宽、偏移量和排序。响应式visibility实用工具也将被更新以使用自定义断点。确保以`px`为单位设置网格值（不是 `rem`、`em`或`%`）。

### 槽宽sass间距定制

是从`$gutters`Sass映射构建的，该映射继承自`$spacers`Sass映射。

```scss
$grid-gutter-width: 1.5rem;
$gutters: (
  0: 0,
  1: $spacer * .25,
  2: $spacer * .5,
  3: $spacer,
  4: $spacer * 1.5,
  5: $spacer * 3,
);
```

## z-index

```scss
$zindex-dropdown:                   1000;
$zindex-sticky:                     1020;
$zindex-fixed:                      1030;
$zindex-modal-backdrop:             1040;
$zindex-modal:                      1050;
$zindex-popover:                    1060;
$zindex-tooltip:                    1070;
```

## 查看详细文档

- [查看详细文档](/bootstrap5/layout-old.md)
- [查看官方文档](https://v5.getbootstrap.com/docs/5.0/layout/breakpoints/)
