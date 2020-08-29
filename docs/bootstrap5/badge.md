# tag标签

## 徽章尺寸

总共`3`个尺寸，可以单独设置，也可以集体设置。

### 单独配置：
<div class="tags bo p-2">
    <span class="tag">默认大小</span>
    <span class="tag is-md">中尺寸</span>
    <span class="tag is-lg">大尺寸</span>
</div>

```html
<!-- 单独配置 -->
<div class="tags">
    <span class="tag">默认大小</span>
    <span class="tag is-md">中尺寸</span>
    <span class="tag is-lg">大尺寸</span>
</div>
```
### 集体配置：

<div class="tags are-md bo p-2"><span class="tag">All</span><span class="tag">Medium</span><span class="tag">Size</span></div>

```html
<!-- 集体配置 -->
<div class="tags are-md">
    <span class="tag">All</span>
    <span class="tag">Medium</span>
    <span class="tag">Size</span>
</div>
```

## 徽章颜色

<div class="tags bo p-2">
    <span class="tag is-black">Black</span>
    <span class="tag is-dark">Dark</span>
    <span class="tag is-light">Light</span>
    <span class="tag is-white">White</span>
    <span class="tag is-primary">Primary</span>
    <span class="tag is-link">Link</span>
    <span class="tag is-info">Info</span>
    <span class="tag is-success">Success</span>
    <span class="tag is-warning">Warning</span>
    <span class="tag is-danger">Danger</span>
</div>

```html
<div class="tags">
    <span class="tag is-black">Black</span>
    <span class="tag is-dark">Dark</span>
    <span class="tag is-light">Light</span>
    <span class="tag is-white">White</span>
    <span class="tag is-primary">Primary</span>
    <span class="tag is-link">Link</span>
    <span class="tag is-info">Info</span>
    <span class="tag is-success">Success</span>
    <span class="tag is-warning">Warning</span>
    <span class="tag is-danger">Danger</span>
</div>
```

## 徽章群组
外层结构使用class`is-group`包裹，tag标签添加class `item` 即可。
<div class="is-group  bo p-2 mb-1"><span class="item tag is-black">Black</span><span class="item tag is-dark">Dark</span><span class="item tag is-light">Light</span><span class="item tag is-white">White</span><span class="item tag is-primary">Primary</span><span class="item tag is-link">Link</span><span class="item tag is-info">Info</span><span class="item tag is-success">Success</span><span class="item tag is-warning">Warning</span><span class="item tag is-danger">Danger</span></div>

<div class="bo p-2"><div class="is-group is-inflex mb-1"><span class="item tag is-dark">npm</span><span class="item tag is-info">0.5.0</span></div><div class="is-group is-inflex mb-1"><span class="item tag is-dark">build</span><span class="item tag is-primary">passing</span></div><div class="is-group is-inflex mb-1"><span class="item tag is-dark">版本</span><span class="item tag is-success">v2.0.1</span></div></div>

```html
<!-- 群组1 -->
<div class="is-group">
    <span class="item tag is-black">Black</span>
    <span class="item tag is-dark">Dark</span>
    <span class="item tag is-light">Light</span>
    <span class="item tag is-white">White</span>
    <span class="item tag is-primary">Primary</span>
    <span class="item tag is-link">Link</span>
    <span class="item tag is-info">Info</span>
    <span class="item tag is-success">Success</span>
    <span class="item tag is-warning">Warning</span>
    <span class="item tag is-danger">Danger</span>
</div>
<!-- 群组2 -->
<div class="is-group is-inflex">
    <span class="item tag is-dark">npm</span>
    <span class="item tag is-info">0.5.0</span>
</div>

<div class="is-group is-inflex">
    <span class="item tag is-dark">build</span>
    <span class="item tag is-primary">passing</span>
</div>

<div class="is-group is-inflex">
    <span class="item tag is-dark">版本</span>
    <span class="item tag is-success">v2.0.1</span>
</div>
```

## 结合按钮

<div class="btns bo p-2"><button class="btn is-primary">演示效果<span class="tag bg-white oo">6</span></button><button class="btn is-info">演示效果<span class="tag bg-white oo">6</span></button></div>

```html
<button class="btn is-primary">
    演示效果
    <span class="tag bg-white oo">6</span>
</button>
<button class="btn is-info">
    演示效果
    <span class="tag bg-white oo">6</span>
</button>
```


```html

```


```html

```