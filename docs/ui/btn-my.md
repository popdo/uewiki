# 按钮

## 多色按钮

```demo
<button class="btn btn-white" type="button">white</button>
<button class="btn btn-lighter" type="button">lighter</button>
<button class="btn btn-light" type="button">light</button>
<button class="btn btn-default" type="button">默认</button>
<button class="btn btn-primary" type="button">primary</button>
<button class="btn btn-secondary" type="button">secondary</button>
<button class="btn btn-info" type="button">info</button>
<button class="btn btn-success" type="button">success</button>
<button class="btn btn-danger" type="button">danger</button>
<button class="btn btn-warning" type="button">warning</button>
<button class="btn btn-dark" type="button">dark</button>
<button class="btn btn-info" type="button" disabled>disabled</button>
```

```html
<button class="btn btn-white" type="button">white</button>
<button class="btn btn-lighter" type="button">lighter</button>
<button class="btn btn-light" type="button">light</button>
<button class="btn btn-default" type="button">默认</button>
<button class="btn btn-primary" type="button">primary</button>
<button class="btn btn-secondary" type="button">secondary</button>
<button class="btn btn-info" type="button">info</button>
<button class="btn btn-success" type="button">success</button>
<button class="btn btn-danger" type="button">danger</button>
<button class="btn btn-warning" type="button">warning</button>
<button class="btn btn-dark" type="button">dark</button>
```

## 空心按钮

```demo
<button type="button" class="btn btn-outline-white">Primary</button>
<button type="button" class="btn btn-outline-primary">Primary</button>
<button type="button" class="btn btn-outline-secondary">Secondary</button>
<button type="button" class="btn btn-outline-success">Success</button>
<button type="button" class="btn btn-outline-danger">Danger</button>
<button type="button" class="btn btn-outline-warning">Warning</button>
<button type="button" class="btn btn-outline-info">Info</button>
<button type="button" class="btn btn-outline-light">Light</button>
<button type="button" class="btn btn-outline-dark">Dark</button>
```

```html
<button type="button" class="btn btn-outline-primary">Primary</button>
<button type="button" class="btn btn-outline-secondary">Secondary</button>
<button type="button" class="btn btn-outline-success">Success</button>
<button type="button" class="btn btn-outline-danger">Danger</button>
<button type="button" class="btn btn-outline-warning">Warning</button>
<button type="button" class="btn btn-outline-info">Info</button>
<button type="button" class="btn btn-outline-light">Light</button>
<button type="button" class="btn btn-outline-dark">Dark</button>
```

## 浅色按钮

```demo
<button class="btn sbtn-primary" type="button">primary</button>
<button class="btn sbtn-secondary" type="button">secondary</button>
<button class="btn sbtn-info" type="button">info</button>
<button class="btn sbtn-success" type="button">success</button>
<button class="btn sbtn-danger" type="button">danger</button>
<button class="btn sbtn-warning" type="button">warning</button>
<button class="btn sbtn-dark" type="button">dark</button>
<button class="btn sbtn-success" type="button" disabled>disabled</button>
```

```html
<button class="btn sbtn-primary" type="button">primary</button>
<button class="btn sbtn-secondary" type="button">secondary</button>
<button class="btn sbtn-info" type="button">info</button>
<button class="btn sbtn-success" type="button">success</button>
<button class="btn sbtn-danger" type="button">danger</button>
<button class="btn sbtn-warning" type="button">warning</button>
<button class="btn sbtn-dark" type="button">dark</button>
```

## 圆角按钮

```demo
<button class="btn oo btn-default" type="button">默认</button>
<button class="btn oo btn-primary" type="button">primary</button>
<button class="btn oo btn-secondary" type="button">secondary</button>
<button class="btn oo btn-info" type="button">info</button>
<button class="btn oo btn-success" type="button">success</button>
<button class="btn oo btn-danger" type="button">danger</button>
<button class="btn oo btn-warning" type="button">warning</button>
<button class="btn oo btn-dark" type="button">dark</button>
```

```html
<button class="btn oo btn-default" type="button">默认</button>
<button class="btn oo btn-primary" type="button">primary</button>
<button class="btn oo btn-secondary" type="button">secondary</button>
<button class="btn oo btn-info" type="button">info</button>
<button class="btn oo btn-success" type="button">success</button>
<button class="btn oo btn-danger" type="button">danger</button>
<button class="btn oo btn-warning" type="button">warning</button>
<button class="btn oo btn-dark" type="button">dark</button>
```

## DOM元素

```demo
<div class="btn btn-default not-btn">div元素</div>
<span class="btn btn-primary not-btn">span元素</span>
<a class="btn btn-secondary not-btn">a元素</a>
<a class="btn btn-default">元素</a>
<a class="btn btn-light">元素</a>
<input class="btn btn-info" type="submit" value="提交">
<input class="btn btn-success" type="reset" value="重置">
<button class="btn btn-danger" type="button">button</button>
<em class="btn btn-warning">em元素</em>
<b class="btn btn-dark">粗体</b>
```

```html
<div class="btn btn-default not-btn">div元素</div>
<span class="btn btn-primary not-btn">span元素</span>
<a class="btn btn-secondary not-btn">a元素</a>
<a class="btn btn-default">元素</a>
<a class="btn btn-light">元素</a>
<input class="btn btn-info" type="submit" value="提交">
<input class="btn btn-success" type="reset" value="重置">
<button class="btn btn-danger" type="button">button</button>
<em class="btn btn-warning">em元素</em>
<b class="btn btn-dark">粗体</b>
```

## 图标元素

```demo
<button class="btn btn-primary" disabled>
    <span class="spinner-border spinner-border-sm" role="status" aria-hidden="true"></span>
    <span class="sr-only">Loading...</span>
</button>
<button class="btn btn-secondary" type="button" disabled>
    <span class="spinner-border spinner-border-sm mr-1"></span> Loading...
</button>
<button class="btn btn-danger" type="button" disabled>
    <span class="spinner-grow spinner-grow-sm"></span>
    <span class="sr-only">Loading...</span>
</button>
<button class="btn btn-info" type="button" disabled>
    <span class="spinner-grow spinner-grow-sm mr-1"></span> Loading...
</button>
```

```html
<button class="btn btn-primary" disabled>
    <span class="spinner-border spinner-border-sm" role="status" aria-hidden="true"></span>
    <span class="sr-only">Loading...</span>
</button>
<button class="btn btn-secondary" type="button" disabled>
    <span class="spinner-border spinner-border-sm mr-1"></span> Loading...
</button>
<button class="btn btn-danger" type="button" disabled>
    <span class="spinner-grow spinner-grow-sm"></span>
    <span class="sr-only">Loading...</span>
</button>
<button class="btn btn-info" type="button" disabled>
    <span class="spinner-grow spinner-grow-sm mr-1"></span> Loading...
</button>
```

## 多尺寸按钮

```demo
<button type="button" class="btn is-xs">small:is-xs</button>
<button type="button" class="btn is-sm">small:is-sm</button>
<button type="button" class="btn is-md">medium:is-md</button>
<button type="button" class="btn">default</button>
<button type="button" class="btn is-lg">large:is-lg</button>
```

```html
<button type="button" class="btn is-xs">small:is-xs</button>
<button type="button" class="btn is-sm">small:is-sm</button>
<button type="button" class="btn is-md">medium:is-md</button>
<button type="button" class="btn">default</button>
<button type="button" class="btn is-lg">large:is-lg</button>
```

## 按钮组

```demo
<div class="is-group mb-2">
    <div class="item btn btn-info">info</div>
    <div class="item btn btn-default">默认</div>
    <div class="item btn btn-default">默认</div>
    <div class="item btn btn-success">success</div>
    <div class="item btn btn-default">默认</div>
    <input class="item form-item w-auto" type="text">
    <div class="item btn btn-default">默认</div>
    <div class="item btn btn-default">默认</div>
</div>
<div class="is-group mb-2">
    <div class="item btn obtn-primary">primary</div>
    <div class="item btn obtn-secondary">secondary</div>
    <div class="item btn btn-info">info</div>
    <div class="item btn obtn-success">success</div>
    <div class="item btn obtn-danger">danger</div>
    <div class="item btn obtn-warning">warning</div>
</div>
<div class="is-group">
    <div class="item item-text">primary</div>
    <input class="item form-item w-auto" type="text">
    <button class="item btn btn-primary" type="button">submit</button>
</div>
```

```html
<div class="is-group">
    <div class="item btn btn-info">info</div>
    <div class="item btn btn-default">默认</div>
    <div class="item btn btn-default">默认</div>
    <div class="item btn btn-success">success</div>
    <div class="item btn btn-default">默认</div>
    <div class="item btn btn-default">默认</div>
    <div class="item btn btn-default">默认</div>
</div>
<div class="is-group">
    <div class="item btn obtn-primary">primary</div>
    <div class="item btn obtn-secondary">secondary</div>
    <div class="item btn btn-info">info</div>
    <div class="item btn obtn-success">success</div>
    <div class="item btn obtn-danger">danger</div>
    <div class="item btn obtn-warning">warning</div>
</div>
<div class="is-group">
    <div class="item item-text">primary</div>
    <input class="item form-item w-auto" type="text">
    <button class="item btn btn-primary" type="button">submit</button>
</div>
```

## disabled

```demo
<button class="btn btn-white" type="button" disabled>white</button>
<button class="btn btn-light" type="button" disabled>light</button>
<button class="btn" type="button" disabled>default</button>
<div class="btn btn-primary" disabled>div</div>
<span class="btn btn-link" disabled>span</span>
<label class="btn btn-info" disabled>label</label>
<a class="btn btn-success" disabled>a</a>
<button class="btn btn-danger" type="button" disabled>danger</button>
<button class="btn btn-warning" type="button" disabled>warning</button>
<button class="btn btn-dark" type="button" disabled>dark</button>
<button type="button" disabled>原始</button>
```

```html
<button class="btn btn-white" type="button" disabled>white</button>
<button class="btn btn-light" type="button" disabled>light</button>
<button class="btn" type="button" disabled>default</button>
<div class="btn btn-primary" disabled>div</div>
<span class="btn btn-link" disabled>span</span>
<label class="btn btn-info" disabled>label</label>
<a class="btn btn-success" disabled>a</a>
<button class="btn btn-danger" type="button" disabled>danger</button>
<button class="btn btn-warning" type="button" disabled>warning</button>
<button class="btn btn-dark" type="button" disabled>dark</button>
<button type="button" disabled>原始</button>
```
