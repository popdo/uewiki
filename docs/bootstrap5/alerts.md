# Alerts

## 颜色样式

警告框(Alerts)可用于任何长度的文本。以下提供了`8`个不同风格的样式。对于删除按钮，使用的是[alerts](#dismissing) JavaScript插件。

> alert中的链接请添加`.alert-link`类，这样才能保证颜色风格统一。

```demo
<div class="alert alert-primary" role="alert">
  A simple primary alert with <a href="#" class="alert-link">an example link</a>. Give it a click if you like.
</div>
<div class="alert alert-secondary" role="alert">
  A simple secondary alert with <a href="#" class="alert-link">an example link</a>. Give it a click if you like.
</div>
<div class="alert alert-success" role="alert">
  A simple success alert with <a href="#" class="alert-link">an example link</a>. Give it a click if you like.
</div>
<div class="alert alert-danger" role="alert">
  A simple danger alert with <a href="#" class="alert-link">an example link</a>. Give it a click if you like.
</div>
<div class="alert alert-warning" role="alert">
  A simple warning alert with <a href="#" class="alert-link">an example link</a>. Give it a click if you like.
</div>
<div class="alert alert-info" role="alert">
  A simple info alert with <a href="#" class="alert-link">an example link</a>. Give it a click if you like.
</div>
<div class="alert alert-light" role="alert">
  A simple light alert with <a href="#" class="alert-link">an example link</a>. Give it a click if you like.
</div>
<div class="alert alert-dark" role="alert">
  A simple dark alert with <a href="#" class="alert-link">an example link</a>. Give it a click if you like.
</div>
```

```html
<div class="alert alert-primary" role="alert">
  A simple primary alert with <a href="#" class="alert-link">an example link</a>. Give it a click if you like.
</div>
<div class="alert alert-secondary" role="alert">
  A simple secondary alert with <a href="#" class="alert-link">an example link</a>. Give it a click if you like.
</div>
<div class="alert alert-success" role="alert">
  A simple success alert with <a href="#" class="alert-link">an example link</a>. Give it a click if you like.
</div>
<div class="alert alert-danger" role="alert">
  A simple danger alert with <a href="#" class="alert-link">an example link</a>. Give it a click if you like.
</div>
<div class="alert alert-warning" role="alert">
  A simple warning alert with <a href="#" class="alert-link">an example link</a>. Give it a click if you like.
</div>
<div class="alert alert-info" role="alert">
  A simple info alert with <a href="#" class="alert-link">an example link</a>. Give it a click if you like.
</div>
<div class="alert alert-light" role="alert">
  A simple light alert with <a href="#" class="alert-link">an example link</a>. Give it a click if you like.
</div>
<div class="alert alert-dark" role="alert">
  A simple dark alert with <a href="#" class="alert-link">an example link</a>. Give it a click if you like.
</div>
```

## 包含html元素

Alerts还可以包含额外的HTML元素，如标题、段落和分隔符。

```demo
<div class="alert alert-success" role="alert">
  <h4 class="alert-heading">Well done!</h4>
  <p>Aww yeah, you successfully read this important alert message. This example text is going to run a bit longer so that you can see how spacing within an alert works with this kind of content.</p>
  <hr>
  <p class="mb-0">Whenever you need to, be sure to use margin utilities to keep things nice and tidy.</p>
</div>
```

```html
<div class="alert alert-success" role="alert">
  <h4 class="alert-heading">Well done!</h4>
  <p>Aww yeah, you successfully read this important alert message. This example text is going to run a bit longer so that you can see how spacing within an alert works with this kind of content.</p>
  <hr>
  <p class="mb-0">Whenever you need to, be sure to use margin utilities to keep things nice and tidy.</p>
</div>
```

## 关闭功能

使用alert JavaScript插件，可以关闭任何内联alert。方法如下：

- 确保您已经加载了alert插件或编译的Bootstrap5 JavaScript文件。
- 添加[close](/bootstrap5/components?id=关闭按钮)按钮和`.alert-dismissible`类，这将在alert的右侧添加一个关闭按钮。
- 在close按钮上，添加`data-dismiss="alert"`属性，它触发JavaScript功能。按钮一定要使用`<button>`元素，以便在所有设备上都能正常工作。
- 若要在关闭alert时设置动画，请确保添加`.fade`和`.show`类。

```demo
<div class="alert alert-warning alert-dismissible fade show" role="alert">
  <strong>Holy guacamole!</strong> You should check in on some of those fields below.
  <button type="button" class="close" data-dismiss="alert" aria-label="Close">
    <span aria-hidden="true">&times;</span>
  </button>
</div>
```

```html
<div class="alert alert-warning alert-dismissible fade show" role="alert">
  <strong>Holy guacamole!</strong> You should check in on some of those fields below.
  <button type="button" class="close" data-dismiss="alert" aria-label="Close">
    <span aria-hidden="true">&times;</span>
  </button>
</div>
```

## JavaScript事件

### 触发器 <!-- {docsify-ignore} -->

通过JavaScript关闭警报的功能：

```js
var alertList = document.querySelectorAll('.alert')
alertList.forEach(function (alert) {
  new bootstrap.Alert(alert)
})

```

或在alert内的button上加上`data`属性，如上所示：

```demo
<button type="button" class="close" data-dismiss="alert" aria-label="Close">
  <span aria-hidden="true">&times;</span>
</button>

```

```html
<button type="button" class="close" data-dismiss="alert" aria-label="Close">
  <span aria-hidden="true">&times;</span>
</button>

```

> 请注意，关闭alert会将其从DOM中删除。

### 方法 <!-- {docsify-ignore} -->

例如，你可以使用alert构造函数创建一个alert实例。

```demo
<div id="myAlert" class="alert alert-primary" role="alert">
    A simple primary alert—check it out!
</div>
```

```js
var myAlert = document.getElementById('myAlert')
var bsAlert = new bootstrap.Alert(myAlert)
```

这将使警报侦听具有`data-dismiss="alert"`属性的子元素上的单击事件。（使用数据api的自动初始化时不需要。）

|Method|Description|
|------|-----------|
|close|通过从DOM中删除alert来关闭警报。如果元素上存在`.fade`和`.show`类，则警报将在删除之前淡出。|
|dispose|销毁元素的警报|
|getInstance|静态方法，它允许您获取与DOM元素关联的警报实例，您可以这样使用它：`bootstrap.Alert.getInstance(alert)`|

```js
var alertNode = document.querySelector('.alert')
var alert = bootstrap.Alert.getInstance(alertNode)
alert.close()
```

### 事件 <!-- {docsify-ignore} -->

Bootstrap的alert插件公开了一些事件，用于挂接警报功能。

|Method|Description|
|------|-----------|
|close.bs.alert|调用`close`实例方法时立即触发。|
|closed.bs.alert|当警报已关闭且CSS转换完成时触发。|
