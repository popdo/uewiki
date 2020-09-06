# tag标签

## 徽章尺寸

总共`3`个尺寸，可以单独设置，也可以集体设置。

单独配置:

```demo
<div class="tags">
    <span class="tag">默认大小</span>
    <span class="tag tag-md">中尺寸</span>
    <span class="tag tag-lg">大尺寸</span>
</div>
```

```html
<!-- 单独配置 -->
<div class="tags">
    <span class="tag">默认大小</span>
    <span class="tag tag-md">中尺寸</span>
    <span class="tag tag-lg">大尺寸</span>
</div>
```

集体配置:

```demo
<div class="tags">
    <span class="tag">All</span>
    <span class="tag">Medium</span>
    <span class="tag">Size</span>
</div>
<div class="tags tags-md">
    <span class="tag">All</span>
    <span class="tag">Medium</span>
    <span class="tag">Size</span>
</div>
<div class="tags tags-lg">
    <span class="tag">All</span>
    <span class="tag">Medium</span>
    <span class="tag">Size</span>
</div>
```

```html
<!-- 集体配置 -->
<div class="tags">
    <span class="tag">All</span>
    <span class="tag">Medium</span>
    <span class="tag">Size</span>
</div>
<div class="tags tags-md">
    <span class="tag">All</span>
    <span class="tag">Medium</span>
    <span class="tag">Size</span>
</div>
<div class="tags tags-lg">
    <span class="tag">All</span>
    <span class="tag">Medium</span>
    <span class="tag">Size</span>
</div>
```

## 徽章颜色

```demo
<div class="tags">
    <span class="tag tag-black">Black</span>
    <span class="tag tag-dark">Dark</span>
    <span class="tag tag-light">Light</span>
    <span class="tag tag-white">White</span>
    <span class="tag tag-primary">Primary</span>
    <span class="tag tag-link">Link</span>
    <span class="tag tag-info">Info</span>
    <span class="tag tag-success">Success</span>
    <span class="tag tag-warning">Warning</span>
    <span class="tag tag-danger">Danger</span>
</div>
```

```html
<div class="tags">
    <span class="tag tag-black">Black</span>
    <span class="tag tag-dark">Dark</span>
    <span class="tag tag-light">Light</span>
    <span class="tag tag-white">White</span>
    <span class="tag tag-primary">Primary</span>
    <span class="tag tag-link">Link</span>
    <span class="tag tag-info">Info</span>
    <span class="tag tag-success">Success</span>
    <span class="tag tag-warning">Warning</span>
    <span class="tag tag-danger">Danger</span>
</div>
```

## 徽章群组

外层结构使用class`is-group`包裹，tag标签添加class `item` 即可。

```demo
<div class="is-group mb-1">
    <span class="item tag tag-black">Black</span>
    <span class="item tag tag-dark">Dark</span>
    <span class="item tag tag-light">Light</span>
    <span class="item tag tag-white">White</span>
    <span class="item tag tag-primary">Primary</span>
    <span class="item tag tag-link">Link</span>
    <span class="item tag tag-info">Info</span>
    <span class="item tag tag-success">Success</span>
    <span class="item tag tag-warning">Warning</span>
    <span class="item tag tag-danger">Danger</span>
</div>
<div class="is-group mb-1">
    <span class="item tag tag-dark">npm</span>
    <span class="item tag tag-info">0.5.0</span>
</div>

<div class="is-group mb-1">
    <span class="item tag tag-dark">build</span>
    <span class="item tag tag-primary">passing</span>
</div>

<div class="is-group mb-1">
    <span class="item tag tag-dark">版本</span>
    <span class="item tag tag-success">v2.0.1</span>
</div>
```

```html
<!-- 群组1 -->
<div class="is-group">
    <span class="item tag tag-black">Black</span>
    <span class="item tag tag-dark">Dark</span>
    <span class="item tag tag-light">Light</span>
    <span class="item tag tag-white">White</span>
    <span class="item tag tag-primary">Primary</span>
    <span class="item tag tag-link">Link</span>
    <span class="item tag tag-info">Info</span>
    <span class="item tag tag-success">Success</span>
    <span class="item tag tag-warning">Warning</span>
    <span class="item tag tag-danger">Danger</span>
</div>
<!-- 群组2 -->
<div class="is-group">
    <span class="item tag tag-dark">npm</span>
    <span class="item tag tag-info">0.5.0</span>
</div>

<div class="is-group">
    <span class="item tag tag-dark">build</span>
    <span class="item tag tag-primary">passing</span>
</div>

<div class="is-group">
    <span class="item tag tag-dark">版本</span>
    <span class="item tag tag-success">v2.0.1</span>
</div>
```

## 结合按钮

```demo
<button class="btn btn-primary" type="button">
    演示效果
    <span class="tag tag-white o-50">6</span>
</button>
<button class="btn obtn-info">
    演示效果
    <span class="tag tag-success o-50" type="button">6</span>
</button>
```

```html
<button class="btn btn-primary" type="button">
    演示效果
    <span class="tag tag-white o-50">6</span>
</button>
<button class="btn obtn-info">
    演示效果
    <span class="tag tag-success o-50" type="button">6</span>
</button>
```
