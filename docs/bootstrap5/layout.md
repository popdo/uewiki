# 布局

## 媒体断点

每个断点大小被设置为12的倍数，并代表通用设备大小和窗口尺寸的子集。它们没有专门针对每个设备，但是近乎为任意尺寸的设备提供了强大的一致性的基础。

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
