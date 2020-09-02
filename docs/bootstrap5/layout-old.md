# 布局

Bootstrap 提供了一套响应式、移动设备优先的流式栅格系统，随着屏幕或视口（viewport）尺寸的增加，系统会自动分为最多12列。它包含了易于使用的预定义类，还有强大的`mixin` 用于生成更具语义的布局。

## 媒体断点

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

### **Min-width**

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

### **Max-width**

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

### **单个断点**

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

### **断点跨度**

同样，媒体查询可能跨越多个断点宽度：

```scss
@include media-breakpoint-between(md, xl) { ... }
```

输出结果是：

```css
@media (min-width: 768px) and (max-width: 1199.98px) { ... }
```

<!-- tabs:end -->

## container-容器

### 如何工作的

容器是Bootstrap中最基本的布局元素，在我们的默认网格系统时需要。容器用于包含、填充和（有时）居中的内容。虽然容器可以嵌套，但大多数布局并不需要嵌套的容器。

Bootstrap有三个不同的容器。

- `.container`, 在每个响应断点处设置最大宽度
- `.container-fluid`, 在所有断点处width:100%。
- `.container-{breakpoint}`, width:100%直到指定断点

下表说明了每个容器的`max-width`与原始`.container`和`.container-fluid`在每个断点上的比较。

在我们的网格示例中，可以看到它们的运行情况并进行比较。

| Class name         | Extra small  *<576px*     | Small   *≥576px*     | Medium  *≥768px*     | Large  *≥992px*     | X\-Large  *≥1200px*     | XX\-Large  *≥1400px*     |
|--------------------|---------------------------|----------------------|----------------------|---------------------|-------------------------|--------------------------|
| `.container`       | 100%                      | 540px                | 720px                | 960px               | 1140px                  | 1320px                   |
| `.container-sm`    | 100%                      | 540px                | 720px                | 960px               | 1140px                  | 1320px                   |
| `.container-md`    | 100%                      | 100%                 | 720px                | 960px               | 1140px                  | 1320px                   |
| `.container-lg`    | 100%                      | 100%                 | 100%                 | 960px               | 1140px                  | 1320px                   |
| `.container-xl`    | 100%                      | 100%                 | 100%                 | 100%                | 1140px                  | 1320px                   |
| `.container-xxl`   | 100%                      | 100%                 | 100%                 | 100%                | 100%                    | 1320px                   |
| `.container-fluid` | 100%                      | 100%                 | 100%                 | 100%                | 100%                    | 100%                     |

### Sass源码定制

如上所示，Bootstrap生成了一系列预定义的容器类，以帮助你构建你想要的布局。您可以通过修改为它们提供的 Sass 映射（在`_variables.scss`中找到）来定制这些预定义的容器类。

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

## Grid-栅格系统

栅格系统用于通过一系列的行（row）与列（column）的组合来创建页面布局，你的内容就可以放入这些创建好的布局中。

### 栅格参数

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

### 自动列布局

根据屏幕窗口的大小，自动布局（无需使用类似`.col-sm-6`指定宽度）。

<!-- tabs:start -->

#### **等宽布局**

例如，下面的例子中两种网格布局方式，适用于任何设备和屏幕（从`xs`到`xxl`）。根据需要的断点添加任意数量的无单元类（col），每一列的宽度都是一样的。

```demo
<div class="container">
  <div class="row mb-2">
    <div class="col border bg-light p-2">
      1 of 2
    </div>
    <div class="col border bg-light p-2">
      2 of 2
    </div>
  </div>
  <div class="row">
    <div class="col border bg-light p-2">
      1 of 3
    </div>
    <div class="col border bg-light p-2">
      2 of 3
    </div>
    <div class="col border bg-light p-2">
      3 of 3
    </div>
  </div>
</div>

```

```html
<div class="container">
  <div class="row">
    <div class="col">
      1 of 2
    </div>
    <div class="col">
      2 of 2
    </div>
  </div>
  <div class="row">
    <div class="col">
      1 of 3
    </div>
    <div class="col">
      2 of 3
    </div>
    <div class="col">
      3 of 3
    </div>
  </div>
</div>

```

#### **单独设置列宽度**

flexbox网格列的自动布局也意味着你可以设置一列的宽度，并使其周围的兄弟列自动调整大小。你可以使用预定义的网格类（如下所示），网格混搭，或者内联宽度。请注意，无论指定列的宽度如何，其他列都会自动调整大小。

```demo
<div class="container">
  <div class="row mb-2">
    <div class="col border bg-light p-2">
      1 of 3
    </div>
    <div class="col-6 border bg-light p-2">
      2 of 3 (wider)
    </div>
    <div class="col border bg-light p-2">
      3 of 3
    </div>
  </div>
  <div class="row">
    <div class="col-5 border bg-light p-2">
      1 of 3
    </div>
    <div class="col border bg-light p-2">
      2 of 3 (wider)
    </div>
    <div class="col border bg-light p-2">
      3 of 3
    </div>
  </div>
</div>
```

```html
<div class="container">
  <div class="row">
    <div class="col">
      1 of 3
    </div>
    <div class="col-6">
      2 of 3 (wider)
    </div>
    <div class="col">
      3 of 3
    </div>
  </div>
  <div class="row">
    <div class="col">
      1 of 3
    </div>
    <div class="col-5">
      2 of 3 (wider)
    </div>
    <div class="col">
      3 of 3
    </div>
  </div>
</div>
```

#### **可变内容宽度**

使用`col-{breakpoint}-auto`类可以根据其内容的自然宽度来调整列的大小。

```demo
<div class="container">
  <div class="row justify-content-md-center mb-2">
    <div class="col col-lg-2 border bg-light p-2">
      1 of 3
    </div>
    <div class="col-md-auto border bg-light p-2">
      Variable width content
    </div>
    <div class="col col-lg-2 border bg-light p-2">
      3 of 3
    </div>
  </div>
  <div class="row">
    <div class="col border bg-light p-2">
      1 of 3
    </div>
    <div class="col-md-auto border bg-light p-2">
      Variable width content.aaaaaaaabbbbbbbbbbbbbbb
    </div>
    <div class="col col-lg-2 border bg-light p-2">
      3 of 3
    </div>
  </div>
</div>
```

```html
<div class="container">
  <div class="row justify-content-md-center">
    <div class="col col-lg-2">
      1 of 3
    </div>
    <div class="col-md-auto">
      Variable width content
    </div>
    <div class="col col-lg-2">
      3 of 3
    </div>
  </div>
  <div class="row">
    <div class="col">
      1 of 3
    </div>
    <div class="col-md-auto">
      Variable width content.aaaaaaaabbbbbbbbbbbbbbb
    </div>
    <div class="col col-lg-2">
      3 of 3
    </div>
  </div>
</div>
```

<!-- tabs:end -->

### 响应式class

Bootstrap的网格包括六层预定义类，用于构建复杂的响应式布局。在超小型、小型、中型、大型或超大型设备上自定义你的列的大小，无论你怎么看都合适。

<!-- tabs:start -->

#### **所有断点**

对于从最小设备到最大设备的相同网格，请使用`.col`和`.col-*`类。当您需要一个特定大小的列时，请指定一个带编号的类；否则，请随意使用`.col`。

```demo
<div class="container">
  <div class="row mb-2">
    <div class="col border bg-light p-2">col</div>
    <div class="col border bg-light p-2">col</div>
    <div class="col border bg-light p-2">col</div>
    <div class="col border bg-light p-2">col</div>
  </div>
  <div class="row">
    <div class="col-8 border bg-light p-2">col-8</div>
    <div class="col-4 border bg-light p-2">col-4</div>
  </div>
</div>

```

```html
<div class="container">
  <div class="row">
    <div class="col">col</div>
    <div class="col">col</div>
    <div class="col">col</div>
    <div class="col">col</div>
  </div>
  <div class="row">
    <div class="col-8">col-8</div>
    <div class="col-4">col-4</div>
  </div>
</div>

```

#### **水平铺满**

使用一组响应类，例如`.col-sm-*`类，创建一个基本的网格系统，当在小的屏幕断点（`sm`）处就变成水平铺满的。(请在小屏设备上测试一下)

```demo
<div class="container">
  <div class="row mb-2">
    <div class="col-sm-8 border bg-light p-2">col-sm-8</div>
    <div class="col-sm-4 border bg-light p-2">col-sm-4</div>
  </div>
  <div class="row">
    <div class="col-sm border bg-light p-2">col-sm</div>
    <div class="col-sm border bg-light p-2">col-sm</div>
    <div class="col-sm border bg-light p-2">col-sm</div>
  </div>
</div>
```

```html
<div class="container">
  <div class="row">
    <div class="col-sm-8">col-sm-8</div>
    <div class="col-sm-4">col-sm-4</div>
  </div>
  <div class="row">
    <div class="col-sm">col-sm</div>
    <div class="col-sm">col-sm</div>
    <div class="col-sm">col-sm</div>
  </div>
</div>
```

#### **混合搭配**

不想让你的列简单地堆叠在一些网格层中？根据需要为每个层级使用不同的类组合。请看下面的例子，以便更好地了解这一切是如何工作的。

```demo
<div class="container">
  <!-- Stack the columns on mobile by making one full-width and the other half-width -->
  <div class="row mb-2">
    <div class="col-md-8 border bg-light p-2">.col-md-8</div>
    <div class="col-6 col-md-4 border bg-light p-2">.col-6 .col-md-4</div>
  </div>

  <!-- Columns start at 50% wide on mobile and bump up to 33.3% wide on desktop -->
  <div class="row mb-2">
    <div class="col-6 col-md-4 border bg-light p-2">.col-6 .col-md-4</div>
    <div class="col-6 col-md-4 border bg-light p-2">.col-6 .col-md-4</div>
    <div class="col-6 col-md-4 border bg-light p-2">.col-6 .col-md-4</div>
  </div>

  <!-- Columns are always 50% wide, on mobile and desktop -->
  <div class="row">
    <div class="col-6 border bg-light p-2">.col-6</div>
    <div class="col-6 border bg-light p-2">.col-6</div>
  </div>
</div>
```

```html
<div class="container">
  <!-- Stack the columns on mobile by making one full-width and the other half-width -->
  <div class="row">
    <div class="col-md-8">.col-md-8</div>
    <div class="col-6 col-md-4">.col-6 .col-md-4</div>
  </div>

  <!-- Columns start at 50% wide on mobile and bump up to 33.3% wide on desktop -->
  <div class="row">
    <div class="col-6 col-md-4">.col-6 .col-md-4</div>
    <div class="col-6 col-md-4">.col-6 .col-md-4</div>
    <div class="col-6 col-md-4">.col-6 .col-md-4</div>
  </div>

  <!-- Columns are always 50% wide, on mobile and desktop -->
  <div class="row">
    <div class="col-6">.col-6</div>
    <div class="col-6">.col-6</div>
  </div>
</div>
```

<!-- tabs:end -->

### 在row上设置col宽

使用响应的`.row-cols-*`类来快速设置列数，以最好地呈现你的内容和布局。普通的`.col-*`类适用于单独的列（例如`.col-md-4`），而行列类是作为快捷方式在父`.row`上设置的。使用`.row-cols-auto`，你可以给列以自然宽度。  
使用这些行列类来快速创建基本的网格布局或控制你的布局。

```demo
<div class="container">
  <div class="row row-cols-2">
    <div class="col border p-2 bg-light">Column</div>
    <div class="col border p-2 bg-light">Column</div>
    <div class="col border p-2 bg-light">Column</div>
    <div class="col border p-2 bg-light">Column</div>
  </div>
</div>
```

```html
<div class="container">
  <div class="row row-cols-2">
    <div class="col">Column</div>
    <div class="col">Column</div>
    <div class="col">Column</div>
    <div class="col">Column</div>
  </div>
</div>
```

```demo
<div class="container">
  <div class="row row-cols-3">
    <div class="col border p-2 bg-light">Column</div>
    <div class="col border p-2 bg-light">Column</div>
    <div class="col border p-2 bg-light">Column</div>
    <div class="col border p-2 bg-light">Column</div>
  </div>
</div>
```

```html
<div class="container">
  <div class="row row-cols-3">
    <div class="col">Column</div>
    <div class="col">Column</div>
    <div class="col">Column</div>
    <div class="col">Column</div>
  </div>
</div>
```

```demo
<div class="container">
  <div class="row row-cols-auto">
    <div class="col border p-2 bg-light">Column</div>
    <div class="col border p-2 bg-light">Column</div>
    <div class="col border p-2 bg-light">Column</div>
    <div class="col border p-2 bg-light">Column</div>
  </div>
</div>
```

```html
<div class="container">
  <div class="row row-cols-auto">
    <div class="col">Column</div>
    <div class="col">Column</div>
    <div class="col">Column</div>
    <div class="col">Column</div>
  </div>
</div>
```

```demo
<div class="container">
  <div class="row row-cols-4">
    <div class="col border p-2 bg-light">Column</div>
    <div class="col border p-2 bg-light">Column</div>
    <div class="col border p-2 bg-light">Column</div>
    <div class="col border p-2 bg-light">Column</div>
  </div>
</div>
```

```html
<div class="container">
  <div class="row row-cols-4">
    <div class="col">Column</div>
    <div class="col">Column</div>
    <div class="col">Column</div>
    <div class="col">Column</div>
  </div>
</div>
```

```demo
<div class="container">
  <div class="row row-cols-4">
    <div class="col border p-2 bg-light">Column</div>
    <div class="col border p-2 bg-light">Column</div>
    <div class="col-6 border p-2 bg-light">Column</div>
    <div class="col border p-2 bg-light">Column</div>
  </div>
</div>
```

```html
<div class="container">
  <div class="row row-cols-4">
    <div class="col">Column</div>
    <div class="col">Column</div>
    <div class="col-6">Column</div>
    <div class="col">Column</div>
  </div>
</div>
```

```demo
<div class="container">
  <div class="row row-cols-1 row-cols-sm-2 row-cols-md-4">
    <div class="col border p-2 bg-light">Column</div>
    <div class="col border p-2 bg-light">Column</div>
    <div class="col border p-2 bg-light">Column</div>
    <div class="col border p-2 bg-light">Column</div>
  </div>
</div>
```

```html
<div class="container">
  <div class="row row-cols-1 row-cols-sm-2 row-cols-md-4">
    <div class="col">Column</div>
    <div class="col">Column</div>
    <div class="col">Column</div>
    <div class="col">Column</div>
  </div>
</div>
```

您还可以使用附带的Sass mixin，`row-cols():`

```scss
.element {
  // Three columns to start
  @include row-cols(3);

  // Five columns from medium breakpoint up
  @include media-breakpoint-up(md) {
    @include row-cols(5);
  }
}
```

### 嵌套

要用默认网格来嵌套你的内容，可以在现有的`.col-sm-*`列中添加一个新的`.row`和一组`.col-sm-*`列。一组嵌套的行应该加起来为12列或更少的列（不要求你使用所有12列）。

```demo
<div class="container">
  <div class="row">
    <div class="col-sm-3 border bg-light py-2">
      Level 1: .col-sm-3
    </div>
    <div class="col-sm-9 border bg-light py-2">
      <div class="row">
        <div class="col-8 col-sm-6 border bg-light py-2">
          Level 2: .col-8 .col-sm-6
        </div>
        <div class="col-4 col-sm-6 border bg-light py-2">
          Level 2: .col-4 .col-sm-6
        </div>
      </div>
    </div>
  </div>
</div>
```

```html
<div class="container">
  <div class="row">
    <div class="col-sm-3">
      Level 1: .col-sm-3
    </div>
    <div class="col-sm-9">
      <div class="row">
        <div class="col-8 col-sm-6">
          Level 2: .col-8 .col-sm-6
        </div>
        <div class="col-4 col-sm-6">
          Level 2: .col-4 .col-sm-6
        </div>
      </div>
    </div>
  </div>
</div>
```

### Sass源码

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

## Columns-列

使用flexbox对齐实用工具可以垂直和水平对齐列。

### 垂直对齐

```demo
<div class="container">
  <div class="row align-items-start bg-light mb-3" style="min-height:10rem">
    <div class="col border p-2">
      One of three columns
    </div>
    <div class="col border p-2">
      One of three columns
    </div>
    <div class="col border p-2">
      One of three columns
    </div>
  </div>
  <div class="row align-items-center bg-light mb-3" style="min-height:10rem">
    <div class="col border p-2">
      One of three columns
    </div>
    <div class="col border p-2">
      One of three columns
    </div>
    <div class="col border p-2">
      One of three columns
    </div>
  </div>
  <div class="row align-items-end bg-light" style="min-height:10rem">
    <div class="col border p-2">
      One of three columns
    </div>
    <div class="col border p-2">
      One of three columns
    </div>
    <div class="col border p-2">
      One of three columns
    </div>
  </div>
</div>
```

```html
<div class="container">
  <div class="row align-items-start">
    <div class="col">
      One of three columns
    </div>
    <div class="col">
      One of three columns
    </div>
    <div class="col">
      One of three columns
    </div>
  </div>
  <div class="row align-items-center">
    <div class="col">
      One of three columns
    </div>
    <div class="col">
      One of three columns
    </div>
    <div class="col">
      One of three columns
    </div>
  </div>
  <div class="row align-items-end">
    <div class="col">
      One of three columns
    </div>
    <div class="col">
      One of three columns
    </div>
    <div class="col">
      One of three columns
    </div>
  </div>
</div>
```

```demo
<div class="container">
  <div class="row bg-light" style="min-height:10rem">
    <div class="col align-self-start border p-2">
      One of three columns
    </div>
    <div class="col align-self-center border p-2">
      One of three columns
    </div>
    <div class="col align-self-end border p-2">
      One of three columns
    </div>
  </div>
</div>
```

```html
<div class="container">
  <div class="row">
    <div class="col align-self-start">
      One of three columns
    </div>
    <div class="col align-self-center">
      One of three columns
    </div>
    <div class="col align-self-end">
      One of three columns
    </div>
  </div>
</div>
```

### 水平对齐

```demo
<div class="container">
  <div class="row justify-content-start">
    <div class="col-4 border bg-light p-2">
      One of two columns
    </div>
    <div class="col-4 border bg-light p-2">
      One of two columns
    </div>
  </div>
  <div class="row justify-content-center">
    <div class="col-4 border bg-light p-2">
      One of two columns
    </div>
    <div class="col-4 border bg-light p-2">
      One of two columns
    </div>
  </div>
  <div class="row justify-content-end">
    <div class="col-4 border bg-light p-2">
      One of two columns
    </div>
    <div class="col-4 border bg-light p-2">
      One of two columns
    </div>
  </div>
  <div class="row justify-content-around">
    <div class="col-4 border bg-light p-2">
      One of two columns
    </div>
    <div class="col-4 border bg-light p-2">
      One of two columns
    </div>
  </div>
  <div class="row justify-content-between">
    <div class="col-4 border bg-light p-2">
      One of two columns
    </div>
    <div class="col-4 border bg-light p-2">
      One of two columns
    </div>
  </div>
  <div class="row justify-content-evenly">
    <div class="col-4 border bg-light p-2">
      One of two columns
    </div>
    <div class="col-4 border bg-light p-2">
      One of two columns
    </div>
  </div>
</div>
```

```html
<div class="container">
  <div class="row justify-content-start">
    <div class="col-4">
      One of two columns
    </div>
    <div class="col-4">
      One of two columns
    </div>
  </div>
  <div class="row justify-content-center">
    <div class="col-4">
      One of two columns
    </div>
    <div class="col-4">
      One of two columns
    </div>
  </div>
  <div class="row justify-content-end">
    <div class="col-4">
      One of two columns
    </div>
    <div class="col-4">
      One of two columns
    </div>
  </div>
  <div class="row justify-content-around">
    <div class="col-4">
      One of two columns
    </div>
    <div class="col-4">
      One of two columns
    </div>
  </div>
  <div class="row justify-content-between">
    <div class="col-4">
      One of two columns
    </div>
    <div class="col-4">
      One of two columns
    </div>
  </div>
  <div class="row justify-content-evenly">
    <div class="col-4">
      One of two columns
    </div>
    <div class="col-4">
      One of two columns
    </div>
  </div>
</div>
```

### 列换行

如果一行中有超过12列，则每一组额外超出的列将作为一个单元换行。

```demo
<div class="container">
  <div class="row">
    <div class="col-9 border bg-light py-2">.col-9</div>
    <div class="col-4 border bg-light py-2">.col-4<br>由于 9 + 4 = 13 &gt; 12, 所以这个4列宽的div会作为一个连续的单元被包到新的行上。</div>
    <div class="col-6 border bg-light py-2">.col-6<br>随后的列将追加上去</div>
  </div>
</div>
```

```html
<div class="container">
  <div class="row">
    <div class="col-9">.col-9</div>
    <div class="col-4">.col-4<br>Since 9 + 4 = 13 &gt; 12, this 4-column-wide div gets wrapped onto a new line as one contiguous unit.</div>
    <div class="col-6">.col-6<br>Subsequent columns continue along the new line.</div>
  </div>
</div>
```

### 列分隔行

在flexbox中，将列分割到新的行上需要一个小技巧：在你想将列打散到新的行上的地方添加一个 `width: 100%`的元素。通常情况下，这是通过多个`.rows`来实现的，但并不是每个实现方法都能做到这一点。

```demo
<div class="container">
  <div class="row">
    <div class="col-6 col-sm-3 border bg-light py-2">.col-6 .col-sm-3</div>
    <div class="col-6 col-sm-3 border bg-light py-2">.col-6 .col-sm-3</div>

    <!-- Force next columns to break to new line -->
    <div class="w-100"></div>

    <div class="col-6 col-sm-3 border bg-light py-2">.col-6 .col-sm-3</div>
    <div class="col-6 col-sm-3 border bg-light py-2">.col-6 .col-sm-3</div>
  </div>
</div>
```

```html
<div class="container">
  <div class="row">
    <div class="col-6 col-sm-3">.col-6 .col-sm-3</div>
    <div class="col-6 col-sm-3">.col-6 .col-sm-3</div>

    <!-- Force next columns to break to new line -->
    <div class="w-100"></div>

    <div class="col-6 col-sm-3">.col-6 .col-sm-3</div>
    <div class="col-6 col-sm-3">.col-6 .col-sm-3</div>
  </div>
</div>
```

您也可以使用我们的响应式`display`工具在特定的断点处应用此间隔。

```demo
<div class="container">
  <div class="row">
    <div class="col-6 col-sm-4 border bg-light py-2">.col-6 .col-sm-4</div>
    <div class="col-6 col-sm-4 border bg-light py-2">.col-6 .col-sm-4</div>

    <!-- Force next columns to break to new line at md breakpoint and up -->
    <div class="w-100 d-none d-md-block"></div>

    <div class="col-6 col-sm-4 border bg-light py-2">.col-6 .col-sm-4</div>
    <div class="col-6 col-sm-4 border bg-light py-2">.col-6 .col-sm-4</div>
  </div>
</div>
```

```html
<div class="container">
  <div class="row">
    <div class="col-6 col-sm-4">.col-6 .col-sm-4</div>
    <div class="col-6 col-sm-4">.col-6 .col-sm-4</div>

    <!-- Force next columns to break to new line at md breakpoint and up -->
    <div class="w-100 d-none d-md-block"></div>

    <div class="col-6 col-sm-4">.col-6 .col-sm-4</div>
    <div class="col-6 col-sm-4">.col-6 .col-sm-4</div>
  </div>
</div>
```

### 重组排序

#### 排列类

使用`.order-{1~5}`类控制内容的可视顺序。这些类是响应的，因此您可以按断点设置顺序（例如，`order-1.order-md-2`）。

```demo
<div class="container">
  <div class="row">
    <div class="col border bg-light py-2">
      默认排序1：
    </div>
    <div class="col order-5 border bg-light py-2">
      默认排序：2，使用order-5
    </div>
    <div class="col order-1 border bg-light py-2">
      默认排序：3，使用order-1
    </div>
  </div>
</div>
```

```html
<div class="container">
  <div class="row">
    <div class="col">
      默认排序1：
    </div>
    <div class="col order-5">
      默认排序：2，使用order-5
    </div>
    <div class="col order-1">
      默认排序3，使用order-1
    </div>
  </div>
</div>
```

还有响应式`.order-first`和`.order-last`类，分别通过应用`order:-1`和`order:6`来更改元素的顺序。 这些类也可以根据需要与编号的`.order-*`类混合使用。

```demo
<div class="container">
  <div class="row">
    <div class="col order-last border bg-light py-2">
      默认排序1：使用 order-last
    </div>
    <div class="col border bg-light py-2">
      默认排序2
    </div>
    <div class="col order-first border bg-light py-2">
      默认排序3：使用 order-first
    </div>
  </div>
</div>
```

```html
<div class="container">
  <div class="row">
    <div class="col order-last">
      默认排序1：使用 order-last
    </div>
    <div class="col">
      默认排序2
    </div>
    <div class="col order-first">
      默认排序3：使用 order-first
    </div>
  </div>
</div>
```

#### 偏移网格列

你可以用两种方式来偏移网格列：我们的响应式`.offset-`网格类和我们的`margin utilities`。网格类的大小与列的大小相匹配，而`margins`对于快速布局来说更有用，因为偏移的宽度是可变的。

##### 方法1:偏移量class

使用`.offset-md-*`类将列向右移动。这些类将一列的左边距增加`*`列。例如，`.offset-md-4`将`.col-md-4`移动到四列上。

```demo
<div class="container">
  <div class="row mb-2">
    <div class="col-md-4 border bg-light py-2">.col-md-4</div>
    <div class="col-md-4 offset-md-4 border bg-light py-2">.col-md-4 .offset-md-4</div>
  </div>
  <div class="row mb-2">
    <div class="col-md-3 offset-md-3 border bg-light py-2">.col-md-3 .offset-md-3</div>
    <div class="col-md-3 offset-md-3 border bg-light py-2">.col-md-3 .offset-md-3</div>
  </div>
  <div class="row">
    <div class="col-md-6 offset-md-3 border bg-light py-2">.col-md-6 .offset-md-3</div>
  </div>
</div>

```

```html
<div class="container">
  <div class="row">
    <div class="col-md-4">.col-md-4</div>
    <div class="col-md-4 offset-md-4">.col-md-4 .offset-md-4</div>
  </div>
  <div class="row">
    <div class="col-md-3 offset-md-3">.col-md-3 .offset-md-3</div>
    <div class="col-md-3 offset-md-3">.col-md-3 .offset-md-3</div>
  </div>
  <div class="row">
    <div class="col-md-6 offset-md-3">.col-md-6 .offset-md-3</div>
  </div>
</div>

```

响应式偏移量：

```demo
<div class="container">
  <div class="row mb-2">
    <div class="col-sm-5 col-md-6 border bg-light py-2">.col-sm-5 .col-md-6</div>
    <div class="col-sm-5 offset-sm-2 col-md-6 offset-md-0 border bg-light py-2">.col-sm-5 .offset-sm-2 .col-md-6 .offset-md-0</div>
  </div>
  <div class="row">
    <div class="col-sm-6 col-md-5 col-lg-6 border bg-light py-2">.col-sm-6 .col-md-5 .col-lg-6</div>
    <div class="col-sm-6 col-md-5 offset-md-2 col-lg-6 offset-lg-0 border bg-light py-2">.col-sm-6 .col-md-5 .offset-md-2 .col-lg-6 .offset-lg-0</div>
  </div>
</div>

```

```html
<div class="container">
  <div class="row">
    <div class="col-sm-5 col-md-6">.col-sm-5 .col-md-6</div>
    <div class="col-sm-5 offset-sm-2 col-md-6 offset-md-0">.col-sm-5 .offset-sm-2 .col-md-6 .offset-md-0</div>
  </div>
  <div class="row">
    <div class="col-sm-6 col-md-5 col-lg-6">.col-sm-6 .col-md-5 .col-lg-6</div>
    <div class="col-sm-6 col-md-5 offset-md-2 col-lg-6 offset-lg-0">.col-sm-6 .col-md-5 .offset-md-2 .col-lg-6 .offset-lg-0</div>
  </div>
</div>

```

##### 方法2:Margin实用工具

利用flexbox的特性，你可以使用像`.mr-auto`这样的`margin`实用工具来强制兄弟列之间的距离。

```demo
<div class="container">
  <div class="row mb-2">
    <div class="col-md-4 border bg-light py-2">.col-md-4</div>
    <div class="col-md-4 ml-auto border bg-light py-2">.col-md-4 .ml-auto</div>
  </div>
  <div class="row mb-2">
    <div class="col-md-3 ml-md-auto border bg-light py-2">.col-md-3 .ml-md-auto</div>
    <div class="col-md-3 ml-md-auto border bg-light py-2">.col-md-3 .ml-md-auto</div>
  </div>
  <div class="row">
    <div class="col-auto mr-auto border bg-light py-2">.col-auto .mr-auto</div>
    <div class="col-auto border bg-light py-2">.col-auto</div>
  </div>
</div>
```

```html
<div class="container">
  <div class="row">
    <div class="col-md-4">.col-md-4</div>
    <div class="col-md-4 ml-auto">.col-md-4 .ml-auto</div>
  </div>
  <div class="row">
    <div class="col-md-3 ml-md-auto">.col-md-3 .ml-md-auto</div>
    <div class="col-md-3 ml-md-auto">.col-md-3 .ml-md-auto</div>
  </div>
  <div class="row">
    <div class="col-auto mr-auto">.col-auto .mr-auto</div>
    <div class="col-auto">.col-auto</div>
  </div>
</div>
```

### 独立使用col

.col-*类也可以在.row之外使用，给元素一个特定的宽度。当列类被用作行的非直接子类时，就会省略paddings。

```demo
<div class="col-3 bg-light p-2 border">
  .col-3: 宽度25%
</div>
<div class="col-sm-9 bg-light p-2 border">
  .col-sm-9: sm断点上方宽度75%
</div>
```

```html
<div class="col-3 bg-light p-2 border">
  .col-3: 宽度25%
</div>
<div class="col-sm-9 bg-light p-2 border">
  .col-sm-9: sm断点上方宽度75%
</div>
```

这些类可以与实用工具一起使用，来创建响应的浮动图片。如果文本较短，可以使用`.clearfix`包装器包装内容以清除浮动。

```demo
<div class="clearfix" style="max-width:800px">
  <svg class="col-md-6 float-md-right mb-3 ml-md-3" style="text-anchor: middle;" width="100%" height="210" xmlns="http://www.w3.org/2000/svg" aria-label="Placeholder: Responsive floated image" preserveAspectRatio="xMidYMid slice" role="img" focusable="false"><title>Placeholder</title><rect width="100%" height="100%" fill="#868e96"></rect><text x="50%" y="50%" fill="#dee2e6" dy=".3em">Responsive floated image</text></svg>
  <p>
    Donec ullamcorper nulla non metus auctor fringilla. Nulla vitae elit libero, a pharetra augue. Fusce dapibus, tellus ac cursus commodo, tortor mauris paddenstoel nibh, ut fermentum massa justo sit amet risus. Lorem ipsum dolor sit amet, consectetur adipiscing elit.
  </p>
  <p>
    Sed posuere consectetur est at lobortis. Etiam porta sem malesuada magna mollis euismod. Duis mollis, est non commodo luctus, nisi erat porttitor ligula, eget lacinia odio sem nec elit. Id nullam tellus relem amet commodo telemque olemit. Sed posuere consectetur est at lobortis. Maecenas sed diam eget risus varius blandit sit amet non magna. Cras justo odio, dapibus ac facilisis in, egestas eget quam.
  </p>
  <p>
    Donec id elit non mi porta gravida at eget metus. Aenean eu leo quam. Pellentesque ornare sem lantaarnpaal quam venenatis vestibulum. Donec sed odio dui. Maecenas faucibus mollis interdum. Nullam quis risus eget urna salsa tequila vel eu leo. Donec id elit non mi porta gravida at eget metus.
  </p>
</div>
```

```html
<div class="clearfix">
  <img src="..." class="col-md-6 float-md-right mb-3 ml-md-3" alt="...">
  <p>...</p>
  <p>...</p>
  <p>...</p>
</div>
```

## Gutters-槽宽

Gutters是列之间的填充宽度，用于响应式的间隔和对齐Bootstrap网格系统中的内容。

### Gutters是如何工作

- Gutters是列之间的间距，由水平`padding`创建的。我们在每一列设置`padding-righ`t和`padding-left`，并在每一行的开头和结尾使用负margin来抵消，以对齐内容。
- Gutters开始是`1.5rem`（`20px`）宽。这使我们能够根据padding和margin spacers的比例来匹配我们的网格。
- Gutters可以响应的缩放宽度。使用断点特定的gutter类来修改水平间距、垂直间距和所有间距。

|类名|响应类|说明|
|----|-------|-----|
|`gx-{0~5}`|`gx-{xs\|sm\|md\|lg\|xl\|xxl}-{0~5}`|水平间距|
|`gy-{0~5}`|`gy-{xs\|sm\|md\|lg\|xl\|xxl}-{0~5}`|垂直间距|
|`g-{0~5}`|`g-{xs\|sm\|md\|lg\|xl\|xxl}-{0~5}`|水平+垂直间距|

这类类名需设置在`.row`容器上。

### 水平间距

`.gx-*`类可以用来控制水平间隔宽度。如果使用较大的间隔，可能需要调整`.container`或`.container-fluid`父类，以避免溢出，使用匹配的padding工具。  
例如，在下面的例子2中，我们用`.px-4`增加`padding`。

```demo
<div class="container bg-light mb-2">
  <div class="row gx-5">
    <div class="col">
     <div class="p-2 border bg-light">Custom column padding</div>
    </div>
    <div class="col">
      <div class="p-2 border bg-light">Custom column padding</div>
    </div>
  </div>
</div>
<div class="container px-4 bg-light mb-2">
  <div class="row gx-5">
    <div class="col">
     <div class="p-2 border bg-light">Custom column padding</div>
    </div>
    <div class="col">
      <div class="p-2 border bg-light">Custom column padding</div>
    </div>
  </div>
</div>
<div class="container overflow-hidden bg-light">
  <div class="row gx-5">
    <div class="col">
     <div class="p-2 border bg-light">Custom column padding</div>
    </div>
    <div class="col">
      <div class="p-2 border bg-light">Custom column padding</div>
    </div>
  </div>
</div>
```

```html
<div class="container">
  <div class="row gx-5">
    <div class="col">Custom column padding</div>
    <div class="col">Custom column padding</div>
  </div>
</div>

<!-- 使用. px-4 -->
<div class="container px-4">
  <div class="row gx-5">
    <div class="col">Custom column padding</div>
    <div class="col">Custom column padding</div>
  </div>
</div>

<!-- 使用overflow-hidden -->
<div class="container overflow-hidden">
  <div class="row gx-5">
    <div class="col">Custom column padding</div>
    <div class="col">Custom column padding</div>
  </div>
</div>
```

### 垂直间距

`.gy-*`类可以用来控制垂直槽的宽度。像水平间隔一样，垂直间隔可能会在页面末尾的`.row`下面造成一些溢出。如果发生这种情况，你可以使用`.overflow-hidden`类在`.row`外层添加一个包装器。

```demo
<div class="container overflow-hidden">
  <div class="row gy-5">
    <div class="col-6">
      <div class="p-2 border bg-light">Custom column padding</div>
    </div>
    <div class="col-6">
      <div class="p-2 border bg-light">Custom column padding</div>
    </div>
    <div class="col-6">
      <div class="p-2 border bg-light">Custom column padding</div>
    </div>
    <div class="col-6">
      <div class="p-2 border bg-light">Custom column padding</div>
    </div>
  </div>
</div>
```

```html
<div class="container overflow-hidden">
  <div class="row gy-5">
    <div class="col-6">Custom column padding</div>
    <div class="col-6">Custom column padding</div>
    <div class="col-6">Custom column padding</div>
    <div class="col-6">Custom column padding</div>
  </div>
</div>

```

### 水平 & 垂直间隔

`.g-*`类可以用来控制水平间隔宽度，在下面的例子中，我们使用较小的间隔宽度，所以不需要添加`.overflow-hidden`包装类。

```demo
<div class="container">
  <div class="row g-2">
    <div class="col-6">
      <div class="p-2 border bg-light">Custom column padding</div>
    </div>
    <div class="col-6">
      <div class="p-2 border bg-light">Custom column padding</div>
    </div>
    <div class="col-6">
      <div class="p-2 border bg-light">Custom column padding</div>
    </div>
    <div class="col-6">
      <div class="p-2 border bg-light">Custom column padding</div>
    </div>
  </div>
</div>

```

```html
<div class="container">
  <div class="row g-2">
    <div class="col-6">
      <div class="p-2 border bg-light">Custom column padding</div>
    </div>
    <div class="col-6">
      <div class="p-2 border bg-light">Custom column padding</div>
    </div>
    <div class="col-6">
      <div class="p-2 border bg-light">Custom column padding</div>
    </div>
    <div class="col-6">
      <div class="p-2 border bg-light">Custom column padding</div>
    </div>
  </div>
</div>

```

### 行列间距

还可以在行列中添加间隔类。在下面的例子中，我们使用响应的行列和响应的间隔。

```demo
<div class="container">
  <div class="row row-cols-2 row-cols-lg-5 g-2 g-lg-3">
    <div class="col">
      <div class="p-2 border bg-light">Row column</div>
    </div>
    <div class="col">
      <div class="p-2 border bg-light">Row column</div>
    </div>
    <div class="col">
      <div class="p-2 border bg-light">Row column</div>
    </div>
    <div class="col">
      <div class="p-2 border bg-light">Row column</div>
    </div>
    <div class="col">
      <div class="p-2 border bg-light">Row column</div>
    </div>
    <div class="col">
      <div class="p-2 border bg-light">Row column</div>
    </div>
    <div class="col">
      <div class="p-2 border bg-light">Row column</div>
    </div>
    <div class="col">
      <div class="p-2 border bg-light">Row column</div>
    </div>
    <div class="col">
      <div class="p-2 border bg-light">Row column</div>
    </div>
    <div class="col">
      <div class="p-2 border bg-light">Row column</div>
    </div>
  </div>
</div>

```

```html
<div class="container">
  <div class="row row-cols-2 row-cols-lg-5 g-2 g-lg-3">
    <div class="col">
      <div class="p-2 border bg-light">Row column</div>
    </div>
    <div class="col">
      <div class="p-2 border bg-light">Row column</div>
    </div>
    <div class="col">
      <div class="p-2 border bg-light">Row column</div>
    </div>
    <div class="col">
      <div class="p-2 border bg-light">Row column</div>
    </div>
    <div class="col">
      <div class="p-2 border bg-light">Row column</div>
    </div>
    <div class="col">
      <div class="p-2 border bg-light">Row column</div>
    </div>
    <div class="col">
      <div class="p-2 border bg-light">Row column</div>
    </div>
    <div class="col">
      <div class="p-2 border bg-light">Row column</div>
    </div>
    <div class="col">
      <div class="p-2 border bg-light">Row column</div>
    </div>
    <div class="col">
      <div class="p-2 border bg-light">Row column</div>
    </div>
  </div>
</div>
```

### 源码修改间距

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

[查看官方文档](https://v5.getbootstrap.com/docs/5.0/layout/z-index/)
