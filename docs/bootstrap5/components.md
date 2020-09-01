# 更多组件

## 徽章 :id=Badges

- [官方文档入口](https://v5.getbootstrap.com/docs/5.0/components/badge/)

徽章（Badges）通过使用相对的字体大小和em单位来匹配直接父元素的大小。

<!-- tabs:start -->

### **徽章颜色样式**

```demo
<span class="badge bg-primary">Primary</span>
<span class="badge bg-secondary">Secondary</span>
<span class="badge bg-success">Success</span>
<span class="badge bg-danger">Danger</span>
<span class="badge bg-warning text-dark">Warning</span>
<span class="badge bg-info">Info</span>
<span class="badge bg-light text-dark">Light</span>
<span class="badge bg-dark">Dark</span>
<span class="badge rounded-pill bg-primary">Primary</span>
<span class="badge rounded-pill bg-secondary">Secondary</span>
<span class="badge rounded-pill bg-success">Success</span>
```

```html
<span class="badge bg-primary">Primary</span>
<span class="badge bg-secondary">Secondary</span>
<span class="badge bg-success">Success</span>
<span class="badge bg-danger">Danger</span>
<span class="badge bg-warning text-dark">Warning</span>
<span class="badge bg-info">Info</span>
<span class="badge bg-light text-dark">Light</span>
<span class="badge bg-dark">Dark</span>

<!-- 结合 .rounded-pill实现半径圆角效果 -->
<span class="badge rounded-pill bg-primary">Primary</span>
<span class="badge rounded-pill bg-secondary">Secondary</span>
<span class="badge rounded-pill bg-success">Success</span>
```

浅色背景的徽章需要 `.text-{color}`类来辅助定义文字颜色

### **匹配父元素大小**

```demo
<h1>Example heading <span class="badge bg-secondary">New</span></h1>
<h2>Example heading <span class="badge bg-secondary">New</span></h2>
<h3>Example heading <span class="badge bg-secondary">New</span></h3>
<h4>Example heading <span class="badge bg-secondary">New</span></h4>
<h5>Example heading <span class="badge bg-secondary">New</span></h5>
<h6>Example heading <span class="badge bg-secondary">New</span></h6>
```

```html
<h1>Example heading <span class="badge bg-secondary">New</span></h1>
<h2>Example heading <span class="badge bg-secondary">New</span></h2>
<h3>Example heading <span class="badge bg-secondary">New</span></h3>
<h4>Example heading <span class="badge bg-secondary">New</span></h4>
<h5>Example heading <span class="badge bg-secondary">New</span></h5>
<h6>Example heading <span class="badge bg-secondary">New</span></h6>
```

### **结合按钮使用**

```demo
<button type="button" class="btn btn-primary">
  Notifications <span class="badge bg-secondary">4</span>
</button>
<button type="button" class="btn btn-success">
  Profile <span class="badge rounded-pill bg-white text-body">9</span>
  <span class="sr-only">unread messages</span>
</button>
```

```html
<button type="button" class="btn btn-primary">
  Notifications <span class="badge bg-secondary">4</span>
</button>

<!-- 辅助阅读 -->
<button type="button" class="btn btn-success">
  Profile <span class="badge rounded-pill bg-white text-body">9</span>
  <span class="sr-only">unread messages</span>
</button>
```

<!-- tabs:end -->

## 面包屑导航 :id=Breadcrumb

- [官方文档入口](https://v5.getbootstrap.com/docs/5.0/components/breadcrumb/)

面包屑导航(Breadcrumb)一般用于页面位置导航提示。

```demo
<nav aria-label="breadcrumb">
  <ol class="breadcrumb">
    <li class="breadcrumb-item active" aria-current="page">Home</li>
  </ol>
</nav>
<nav aria-label="breadcrumb">
  <ol class="breadcrumb">
    <li class="breadcrumb-item"><a href="#">Home</a></li>
    <li class="breadcrumb-item active" aria-current="page">Library</li>
  </ol>
</nav>
<nav aria-label="breadcrumb">
  <ol class="breadcrumb">
    <li class="breadcrumb-item"><a href="#">Home</a></li>
    <li class="breadcrumb-item"><a href="#">Library</a></li>
    <li class="breadcrumb-item active" aria-current="page">Data</li>
  </ol>
</nav>
```

```html
<nav aria-label="breadcrumb">
  <ol class="breadcrumb">
    <li class="breadcrumb-item active" aria-current="page">Home</li>
  </ol>
</nav>

<nav aria-label="breadcrumb">
  <ol class="breadcrumb">
    <li class="breadcrumb-item"><a href="#">Home</a></li>
    <li class="breadcrumb-item active" aria-current="page">Library</li>
  </ol>
</nav>

<nav aria-label="breadcrumb">
  <ol class="breadcrumb">
    <li class="breadcrumb-item"><a href="#">Home</a></li>
    <li class="breadcrumb-item"><a href="#">Library</a></li>
    <li class="breadcrumb-item active" aria-current="page">Data</li>
  </ol>
</nav>
```

面包屑导航中我们最好添加一个有意义的标签，如`aria-label="breadcrumb"`来描述`<nav>`元素中提供的导航类型，并将`aria-current="page"`应用到集合的最后一项，以指示它表示当前页。

**更换分割符：**

如需更换分隔符 我们可以在源码中对变量`$breadcrumb-divider`进行修改定义。

```scss
// 修改分隔符
$breadcrumb-divider: quote(">");

// 它还支持使用svg
$breadcrumb-divider: url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='8' height='8'%3E%3Cpath d='M2.5 0L1 1.5 3.5 4 1 6.5 2.5 8l4-4-4-4z' fill='currentColor'/%3E%3C/svg%3E");

// 若无需分隔符，设置none即可
$breadcrumb-divider: none;
```

## 关闭按钮

一个通用的关闭按钮，用于关闭modal和alert等内容。

> 禁用的关闭按钮使用`pointer-events:none`功能，可防止触发悬停和活动状态。

```demo
<button type="button" class="close" aria-label="Close">
  <span aria-hidden="true">&times;</span>
</button>

<button type="button" class="close" disabled aria-label="Close">
  <span aria-hidden="true">&times;</span>
</button>
```

```html
<button type="button" class="close" aria-label="Close">
  <span aria-hidden="true">&times;</span>
</button>

<button type="button" class="close" disabled aria-label="Close">
  <span aria-hidden="true">&times;</span>
</button>
```

## 分页

由于页面中可能有不止一个这样的导航组件，最好为`<nav>`提供一个描述性的`aria-label`以反映其目的。例如，如果分页组件用于在一组搜索结果之间导航，相对的标签可以是`aria-label="Search results pages"`

<!-- tabs:start -->

### **普通效果**

```demo
<nav aria-label="Page navigation example">
  <ul class="pagination">
    <li class="page-item"><a class="page-link" href="#">Previous</a></li>
    <li class="page-item"><a class="page-link" href="#">1</a></li>
    <li class="page-item"><a class="page-link" href="#">2</a></li>
    <li class="page-item"><a class="page-link" href="#">3</a></li>
    <li class="page-item"><a class="page-link" href="#">Next</a></li>
  </ul>
</nav>
```

```html
<nav aria-label="Page navigation example">
  <ul class="pagination">
    <li class="page-item"><a class="page-link" href="#">Previous</a></li>
    <li class="page-item"><a class="page-link" href="#">1</a></li>
    <li class="page-item"><a class="page-link" href="#">2</a></li>
    <li class="page-item"><a class="page-link" href="#">3</a></li>
    <li class="page-item"><a class="page-link" href="#">Next</a></li>
  </ul>
</nav>
```

### **使用icon**

想要在某些分页链接中使用图标或符号代替文本？ 只要确保提供具有`aria`属性。

```demo
<nav aria-label="Page navigation example">
  <ul class="pagination">
    <li class="page-item">
      <a class="page-link" href="#" aria-label="Previous">
        <span aria-hidden="true">&laquo;</span>
      </a>
    </li>
    <li class="page-item"><a class="page-link" href="#">1</a></li>
    <li class="page-item"><a class="page-link" href="#">2</a></li>
    <li class="page-item"><a class="page-link" href="#">3</a></li>
    <li class="page-item">
      <a class="page-link" href="#" aria-label="Next">
        <span aria-hidden="true">&raquo;</span>
      </a>
    </li>
  </ul>
</nav>
```

```html
<nav aria-label="Page navigation example">
  <ul class="pagination">
    <li class="page-item">
      <a class="page-link" href="#" aria-label="Previous">
        <span aria-hidden="true">&laquo;</span>
      </a>
    </li>
    <li class="page-item"><a class="page-link" href="#">1</a></li>
    <li class="page-item"><a class="page-link" href="#">2</a></li>
    <li class="page-item"><a class="page-link" href="#">3</a></li>
    <li class="page-item">
      <a class="page-link" href="#" aria-label="Next">
        <span aria-hidden="true">&raquo;</span>
      </a>
    </li>
  </ul>
</nav>
```

### **禁用和活动状态**

- 分页链接可针对不同情况进行自定义。 使用`.disabled`表示不可点击的链接，`.active`表示当前页面。
- 尽管`.disabled`类可以使用`pointer-events：none`来尝试禁用`<a>`的链接功能，但是CSS属性尚未标准化，因此不能用于键盘导航。 因此，您应始终在禁用的链接上添加`tabindex="-1"`，并使用自定义`JavaScript`完全禁用其功能。
- 您可以选择将活动锚或禁用锚替换为`<span>`，或者在上一个/下一个箭头的情况下省略该锚，以删除单击功能并在保留预期样式的同时防止键盘聚焦。

```demo
<nav class="d-inline-block" aria-label="...">
  <ul class="pagination">
    <li class="page-item disabled">
      <a class="page-link" href="#" tabindex="-1" aria-disabled="true">Previous</a>
    </li>
    <li class="page-item"><a class="page-link" href="#">1</a></li>
    <li class="page-item active" aria-current="page">
      <a class="page-link" href="#">2 <span class="sr-only">(current)</span></a>
    </li>
    <li class="page-item"><a class="page-link" href="#">3</a></li>
    <li class="page-item">
      <a class="page-link" href="#">Next</a>
    </li>
  </ul>
</nav>
<nav class="d-inline-block" aria-label="...">
  <ul class="pagination">
    <li class="page-item disabled">
      <span class="page-link">Previous</span>
    </li>
    <li class="page-item"><a class="page-link" href="#">1</a></li>
    <li class="page-item active" aria-current="page">
      <span class="page-link">
        2
        <span class="sr-only">(current)</span>
      </span>
    </li>
    <li class="page-item"><a class="page-link" href="#">3</a></li>
    <li class="page-item">
      <a class="page-link" href="#">Next</a>
    </li>
  </ul>
</nav>

```

```html
<nav aria-label="...">
  <ul class="pagination">
    <li class="page-item disabled">
      <a class="page-link" href="#" tabindex="-1" aria-disabled="true">Previous</a>
    </li>
    <li class="page-item"><a class="page-link" href="#">1</a></li>
    <li class="page-item active" aria-current="page">
      <a class="page-link" href="#">2 <span class="sr-only">(current)</span></a>
    </li>
    <li class="page-item"><a class="page-link" href="#">3</a></li>
    <li class="page-item">
      <a class="page-link" href="#">Next</a>
    </li>
  </ul>
</nav>

<!-- disabled和active状态的链接可以使用span替代 -->
<nav aria-label="...">
  <ul class="pagination">
    <li class="page-item disabled">
      <span class="page-link">Previous</span>
    </li>
    <li class="page-item"><a class="page-link" href="#">1</a></li>
    <li class="page-item active" aria-current="page">
      <span class="page-link">
        2
        <span class="sr-only">(current)</span>
      </span>
    </li>
    <li class="page-item"><a class="page-link" href="#">3</a></li>
    <li class="page-item">
      <a class="page-link" href="#">Next</a>
    </li>
  </ul>
</nav>
```

### **尺寸大小**

想要更大或更小的页码吗？添加`.pagination-lg`或`.pagination-sm`以获取其他尺寸。

```demo
<nav class="d-inline-block" aria-label="...">
  <ul class="pagination pagination-sm">
    <li class="page-item active" aria-current="page">
      <span class="page-link">
        1
        <span class="sr-only">(current)</span>
      </span>
    </li>
    <li class="page-item"><a class="page-link" href="#">2</a></li>
    <li class="page-item"><a class="page-link" href="#">3</a></li>
  </ul>
</nav>
<nav class="d-inline-block" aria-label="...">
  <ul class="pagination">
    <li class="page-item active" aria-current="page">
      <span class="page-link">
        1
        <span class="sr-only">(current)</span>
      </span>
    </li>
    <li class="page-item"><a class="page-link" href="#">2</a></li>
    <li class="page-item"><a class="page-link" href="#">3</a></li>
  </ul>
</nav>
<nav class="d-inline-block" aria-label="...">
  <ul class="pagination pagination-lg">
    <li class="page-item active" aria-current="page">
      <span class="page-link">
        1
        <span class="sr-only">(current)</span>
      </span>
    </li>
    <li class="page-item"><a class="page-link" href="#">2</a></li>
    <li class="page-item"><a class="page-link" href="#">3</a></li>
  </ul>
</nav>
```

```html
<!-- 小尺寸 -->
<nav aria-label="...">
  <ul class="pagination pagination-sm">
      ...
  </ul>
</nav>

<!-- 普通尺寸 -->
<nav aria-label="...">
  <ul class="pagination">
    ...
  </ul>
</nav>

<!-- 大尺寸 -->
<nav aria-label="...">
  <ul class="pagination pagination-lg">
      ...
  </ul>
</nav>
```

### **水平对齐**

居中对齐 ul`.justify-content-center`

```demo
<nav aria-label="Page navigation example">
  <ul class="pagination justify-content-center">
    <li class="page-item disabled">
      <a class="page-link" href="#" tabindex="-1" aria-disabled="true">Previous</a>
    </li>
    <li class="page-item"><a class="page-link" href="#">1</a></li>
    <li class="page-item"><a class="page-link" href="#">2</a></li>
    <li class="page-item"><a class="page-link" href="#">3</a></li>
    <li class="page-item">
      <a class="page-link" href="#">Next</a>
    </li>
  </ul>
</nav>
```

```html
<nav aria-label="Page navigation example">
  <ul class="pagination justify-content-center">
      ...
  </ul>
</nav>
```

居右对齐 ul`.justify-content-end`

```demo
<nav aria-label="Page navigation example">
  <ul class="pagination justify-content-end">
    <li class="page-item disabled">
      <a class="page-link" href="#" tabindex="-1" aria-disabled="true">Previous</a>
    </li>
    <li class="page-item"><a class="page-link" href="#">1</a></li>
    <li class="page-item"><a class="page-link" href="#">2</a></li>
    <li class="page-item"><a class="page-link" href="#">3</a></li>
    <li class="page-item">
      <a class="page-link" href="#">Next</a>
    </li>
  </ul>
</nav>
```

```html
<nav aria-label="Page navigation example">
  <ul class="pagination justify-content-end">
      ...
  </ul>
</nav>
```

<!-- tabs:end -->

## 滚动监听

滚动监听(Scrollspy)需要条件要求：

- 它必须用于`nav` 或者 `list group`。
- 滚动监听需要在要监视的元素上添加`position:relative;`，通常是`<body>`。
- 当监视`<body>`以外的元素时，请确保设置了`height`和`overflow-y: scroll;` 锚（`<a>`）是必需的，并且必须指向具有该id的元素。

成功实现后，nav或list group将相应地更新，根据相关的目标将`.active`类从一个项目移动到下一个项目。

[查看nav中示例](https://v5.getbootstrap.com/docs/5.0/components/scrollspy/#example-in-navbar)  
[查看list-group中示例](https://v5.getbootstrap.com/docs/5.0/components/scrollspy/#example-with-list-group)

### 通过data属性使用 <!-- {docsify-ignore} -->

要方便地将滚动监听(scrollspy)行为添加到顶栏导航中，请将`data-spy="scroll"`添加到要监视的元素（最典型的是`<body>`）。然后将`nav`组件的父元素的ID或类添加`data-target`属性。

```css
body {
  position: relative;
}
```

```html
<body data-spy="scroll" data-target="#navbar-example">
  ...
  <div id="navbar-example">
    <ul class="nav nav-tabs" role="tablist">
      ...
    </ul>
  </div>
  ...
</body>
```

### 通过JavaScript使用 <!-- {docsify-ignore} -->

在CSS中添加`position:relative`之后，通过JavaScript调用滚动监听(scrollspy)：

```js
var scrollSpy = new bootstrap.ScrollSpy(document.body, {
  target: '#navbar-example'
})
```

!> 不可见的目标元素将被忽略，它们对应的导航项永远不会被突出显示。

### methods方法 <!-- {docsify-ignore} -->

#### 刷新

将滚动监听(scrollspy)与添加或删除DOM中的元素结合使用时，需要调用`refresh`方法，如下所示：

```js
var dataSpyList = [].slice.call(document.querySelectorAll('[data-spy="scroll"]'))
dataSpyList.forEach(function (dataSpyEl) {
  bootstrap.ScrollSpy.getInstance(dataSpyEl)
    .refresh()
})
```

#### 获取实例

静态方法，该方法允许您获取与DOM元素关联的滚动监听(scrollspy)实例

```js
var scrollSpyContentEl = document.getElementById('content')
var scrollSpy = bootstrap.ScrollSpy.getInstance(scrollSpyContentEl) // Returns a Bootstrap scrollspy instance
```

#### 选项设置

选项可以通过data属性或JavaScript传递。对于data属性，将选项名称附加到`data-`，如`data-offset=""`。

|Name|Type|Default|Description|
|----|----|-------|-----------|
|offset|number|10|计算滚动位置时从顶部偏移的像素。|
|method|string|auto|找到被监视元素所在的区域。`auto`将选择获得滚动坐标的最佳方法。<br>偏移量将使用元素[Element.getBoundingClientRect()](https://developer.mozilla.org/en-US/docs/Web/API/Element/getBoundingClientRect) 获取滚动坐标的方法。<br>位置将使用[HTMLElement.offsetTop](https://developer.mozilla.org/en-US/docs/Web/API/HTMLElement/offsetTop)以及[HTMLElement.offsetLeft](https://developer.mozilla.org/en-US/docs/Web/API/HTMLElement/offsetLeft)属性获取滚动坐标。|
|target|string <br>jQuery<br>object<br>DOM<br>element||指定要应用滚动监听(scrollspy)插件的元素。|

#### 事件

|Event type|Description|
|----------|-----------|
|activate.bs.scrollspy|每当滚动监听(scrollspy)激活一个新项目时，此事件就在scroll元素上激活。|

```js
var firstScrollSpyEl = document.querySelector('[data-spy="scroll"]')
firstScrollSpyEl.addEventListener('activate.bs.scrollspy', function () {
  // do something...
})
```
