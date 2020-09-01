# 按钮

## 多色按钮

```demo
<button type="button" class="btn btn-primary">Primary</button>
<button type="button" class="btn btn-secondary">Secondary</button>
<button type="button" class="btn btn-success">Success</button>
<button type="button" class="btn btn-danger">Danger</button>
<button type="button" class="btn btn-warning">Warning</button>
<button type="button" class="btn btn-info">Info</button>
<button type="button" class="btn btn-light">Light</button>
<button type="button" class="btn btn-dark">Dark</button>
<button type="button" class="btn btn-link">Link</button>
```

```html
<button type="button" class="btn btn-primary">Primary</button>
<button type="button" class="btn btn-secondary">Secondary</button>
<button type="button" class="btn btn-success">Success</button>
<button type="button" class="btn btn-danger">Danger</button>
<button type="button" class="btn btn-warning">Warning</button>
<button type="button" class="btn btn-info">Info</button>
<button type="button" class="btn btn-light">Light</button>
<button type="button" class="btn btn-dark">Dark</button>
<button type="button" class="btn btn-link">Link</button>
```

## 禁止换行

如果不希望按钮文字换行，则可以向按钮添加`.text-nowrap`类。 在Sass中，您可以设置`$ btn-white-space：nowrap`来禁用每个按钮的文本换行。

## 按钮标签

`.btn`类设计为与`<button>`元素一起使用。但是，也可以在`<a>`或`<input>`元素上使用（尽管某些浏览器可能会使用略有不同的呈现方式）。  
当在用于触发页内功能（如折叠内容）的元素`<a>`上使用按钮类时，而不是触发链接跳转，应为这些链接提供一个`"role ="button"`将其目的适当传达给屏幕阅读器等辅助技术。

```demo
<a class="btn btn-primary" href="#" role="button">Link</a>
<button class="btn btn-primary" type="submit">Button</button>
<input class="btn btn-primary" type="button" value="Input">
<input class="btn btn-primary" type="submit" value="Submit">
<input class="btn btn-primary" type="reset" value="Reset">
```

```html
<a class="btn btn-primary" href="#" role="button">Link</a>
<button class="btn btn-primary" type="submit">Button</button>
<input class="btn btn-primary" type="button" value="Input">
<input class="btn btn-primary" type="submit" value="Submit">
<input class="btn btn-primary" type="reset" value="Reset">
```

## 空心按钮

用`.btn-outline-*`替换默认修饰符类，这样则会变成空心的反转默认的按钮样式

```demo
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

## 按钮大小

喜欢更大或更小的按钮吗？添加`.btn-lg`或`.btn-sm`以获取其他大小尺寸，使用`.btn-block`则能让按钮平铺整个宽度。

```demo
<button type="button" class="btn btn-primary btn-sm">Small button</button>
<button type="button" class="btn btn-primary">default button</button>
<button type="button" class="btn btn-primary btn-lg">Large button</button>
<button type="button" class="btn btn-primary btn-lg btn-block mt-1">Block level button</button>
```

```html
<button type="button" class="btn btn-primary btn-sm">Small button</button>
<button type="button" class="btn btn-primary">default button</button>
<button type="button" class="btn btn-primary btn-lg">Large button</button>
<button type="button" class="btn btn-primary btn-lg btn-block">Block level button</button>
```

## 禁用状态

- 通过将`disabled`属性添加到按钮元素中，使按钮不能点击。禁用的按钮具有`pointer-events: none`事件，可防止触发悬停和活动状态。
- `<a>`不支持`disabled`属性，因此必须添加`.disabled`类以使其在视觉上显示为禁用,禁用的a应包含`aria-disabled="true`属性，以指示辅助技术的元素状态。

```demo
<a href="#" class="btn btn-primary btn-lg disabled" tabindex="-1" role="button" aria-disabled="true">Primary link</a>
<button type="button" class="btn btn-lg btn-primary" disabled>Primary button</button>
<button type="button" class="btn btn-secondary btn-lg" disabled>Button</button>
```

```html
<a href="#" class="btn btn-primary btn-lg disabled" tabindex="-1" role="button" aria-disabled="true">Primary link</a>
<button type="button" class="btn btn-lg btn-primary" disabled>Primary button</button>
<button type="button" class="btn btn-secondary btn-lg" disabled>Button</button>
```

!> **连接功能警告:** `.disabled`类使用`pointer-events: none`尝试禁用`<a>`的链接功能，但该CSS属性尚未标准化。另外，即使在支持pointer-events: none的浏览器中，keyboard事件也不受影响，这意味着有键盘用户和辅助技术用户仍将能够激活这些链接。为安全起见，请在这些链接上添加`tabindex="-1"`属性（以防止它们获得键盘焦点），并使用自定义JavaScript禁用其功能。

## 切换状态

添加`data-toggle="button"`来切换按钮的有效状态。如果要预切换按钮，则必须手动将`.active`类和`aria-pressed="true"`添加到`<button>`中。

```demo
<a href="#" class="btn btn-primary" role="button" data-toggle="button">切换链接</a>
<a href="#" class="btn btn-primary active" role="button" data-toggle="button" aria-pressed="true">默认切换链接</a>
<a href="#" class="btn btn-primary disabled" role="button" data-toggle="button">禁用切换链接</a>
<button type="button" class="btn btn-primary" data-toggle="button" autocomplete="off">Toggle button</button>
<button type="button" class="btn btn-primary active" data-toggle="button" autocomplete="off" aria-pressed="true">Active toggle button</button>
<button type="button" class="btn btn-primary" disabled data-toggle="button" autocomplete="off">Disabled toggle button</button>
```

```html
<a href="#" class="btn btn-primary" role="button" data-toggle="button">切换链接</a>
<a href="#" class="btn btn-primary active" role="button" data-toggle="button" aria-pressed="true">默认切换链接</a>
<a href="#" class="btn btn-primary disabled" role="button" data-toggle="button">禁用切换链接</a>

<button type="button" class="btn btn-primary" data-toggle="button" autocomplete="off">Toggle button</button>
<button type="button" class="btn btn-primary active" data-toggle="button" autocomplete="off" aria-pressed="true">Active toggle button</button>
<button type="button" class="btn btn-primary" disabled data-toggle="button" autocomplete="off">Disabled toggle button</button>
```


## 圆角按钮

待完善~

```html
<button class="btn oo is-white" type="button">white</button>
<button class="btn oo is-light" type="button">light</button>
<button class="btn oo is-default" type="button">默认</button>
<button class="btn oo is-primary" type="button">primary</button>
<button class="btn oo is-secondary" type="button">secondary</button>
<button class="btn oo is-info" type="button">info</button>
<button class="btn oo is-success" type="button">success</button>
<button class="btn oo is-danger" type="button">danger</button>
<button class="btn oo is-warning" type="button">warning</button>
<button class="btn oo is-dark" type="button">dark</button>
```

## 图标元素

<div class="buttons bo-2 p-2 mb-0">
<button class="btn is-primary" disabled><span class="spinner-border spinner-border-sm" role="status" aria-hidden="true"></span><span class="sr-only">Loading...</span></button><button class="btn is-secondary" type="button" disabled><span class="spinner-border spinner-border-sm mr-1"></span> Loading...</button><button class="btn is-danger" type="button" disabled><span class="spinner-grow spinner-grow-sm"></span><span class="sr-only">Loading...</span></button><button class="btn is-info" type="button" disabled><span class="spinner-grow spinner-grow-sm mr-1"></span> Loading...</button>
</div>

```html
<button class="btn is-primary" disabled>
    <span class="spinner-border spinner-border-sm" role="status" aria-hidden="true"></span>
    <span class="sr-only">Loading...</span>
</button>
<button class="btn is-secondary" type="button" disabled>
    <span class="spinner-border spinner-border-sm mr-1"></span> Loading...
</button>
<button class="btn is-danger" type="button" disabled>
    <span class="spinner-grow spinner-grow-sm"></span>
    <span class="sr-only">Loading...</span>
</button>
<button class="btn is-info" type="button" disabled>
    <span class="spinner-grow spinner-grow-sm mr-1"></span> Loading...
</button>
```

## 按钮组

将需要编组的按钮包裹到`.btn-group`之中，为了支持其它的辅助技术，我们还需要添加`role="group"` `aria-label="xxx"`属性

<!-- tabs:start -->

### **基础按钮组**

```demo
<div class="btn-group" role="group" aria-label="Basic example">
  <button type="button" class="btn btn-primary">Left</button>
  <button type="button" class="btn btn-primary">Middle</button>
  <button type="button" class="btn btn-primary">Right</button>
</div>
<div class="btn-group" role="group" aria-label="Basic outlined example">
  <button type="button" class="btn btn-outline-primary">Left</button>
  <button type="button" class="btn btn-outline-primary">Middle</button>
  <button type="button" class="btn btn-outline-primary">Right</button>
</div>
<div class="btn-group">
  <a href="#" class="btn btn-primary active" aria-current="page">Active link</a>
  <a href="#" class="btn btn-primary">Link</a>
  <a href="#" class="btn btn-primary">Link</a>
</div>
```

```html
<!-- 普通按钮组 -->
<div class="btn-group" role="group" aria-label="Basic example">
  <button type="button" class="btn btn-primary">Left</button>
  <button type="button" class="btn btn-primary">Middle</button>
  <button type="button" class="btn btn-primary">Right</button>
</div>

<!-- 空心按钮组 -->
<div class="btn-group" role="group" aria-label="Basic outlined example">
  <button type="button" class="btn btn-outline-primary">Left</button>
  <button type="button" class="btn btn-outline-primary">Middle</button>
  <button type="button" class="btn btn-outline-primary">Right</button>
</div>

<!-- 链接按钮组 -->
<div class="btn-group">
  <a href="#" class="btn btn-primary active" aria-current="page">Active link</a>
  <a href="#" class="btn btn-primary">Link</a>
  <a href="#" class="btn btn-primary">Link</a>
</div>
```

### **Checkbox、radio按钮组**

将类似按钮的复选框和单选切换按钮组合成一个无缝的按钮组。

```demo
<div class="btn-group" role="group" aria-label="Basic checkbox toggle button group">
  <input type="checkbox" class="btn-check" id="btncheck1" autocomplete="off">
  <label class="btn btn-outline-primary" for="btncheck1">Checkbox 1</label>

  <input type="checkbox" class="btn-check" id="btncheck2" autocomplete="off">
  <label class="btn btn-outline-primary" for="btncheck2">Checkbox 2</label>

  <input type="checkbox" class="btn-check" id="btncheck3" autocomplete="off">
  <label class="btn btn-outline-primary" for="btncheck3">Checkbox 3</label>
</div>
<div class="btn-group" role="group" aria-label="Basic radio toggle button group">
  <input type="radio" class="btn-check" name="btnradio" id="btnradio1" autocomplete="off" checked>
  <label class="btn btn-outline-primary" for="btnradio1">Radio 1</label>

  <input type="radio" class="btn-check" name="btnradio" id="btnradio2" autocomplete="off">
  <label class="btn btn-outline-primary" for="btnradio2">Radio 2</label>

  <input type="radio" class="btn-check" name="btnradio" id="btnradio3" autocomplete="off">
  <label class="btn btn-outline-primary" for="btnradio3">Radio 3</label>
</div>
```

```html
<!-- checkbox按钮组 -->
<div class="btn-group" role="group" aria-label="Basic checkbox toggle button group">
  <input type="checkbox" class="btn-check" id="btncheck1" autocomplete="off">
  <label class="btn btn-outline-primary" for="btncheck1">Checkbox 1</label>

  <input type="checkbox" class="btn-check" id="btncheck2" autocomplete="off">
  <label class="btn btn-outline-primary" for="btncheck2">Checkbox 2</label>

  <input type="checkbox" class="btn-check" id="btncheck3" autocomplete="off">
  <label class="btn btn-outline-primary" for="btncheck3">Checkbox 3</label>
</div>

<!-- radio按钮组 -->
<div class="btn-group" role="group" aria-label="Basic radio toggle button group">
  <input type="radio" class="btn-check" name="btnradio" id="btnradio1" autocomplete="off" checked>
  <label class="btn btn-outline-primary" for="btnradio1">Radio 1</label>

  <input type="radio" class="btn-check" name="btnradio" id="btnradio2" autocomplete="off">
  <label class="btn btn-outline-primary" for="btnradio2">Radio 2</label>

  <input type="radio" class="btn-check" name="btnradio" id="btnradio3" autocomplete="off">
  <label class="btn btn-outline-primary" for="btnradio3">Radio 3</label>
</div>
```

### **按钮组尺寸**

若想获得更大的按钮组追加类名`.btn-group-lg`反之想获取更小的按钮组追加类名`.btn-group-sm`即可。

```demo
<div class="btn-group btn-group-lg" role="group" aria-label="Large button group">
    <button type="button" class="btn btn-outline-dark">Left</button>
    <button type="button" class="btn btn-outline-dark">Middle</button>
    <button type="button" class="btn btn-outline-dark">Right</button>
</div>
<div class="btn-group" role="group" aria-label="Default button group">
    <button type="button" class="btn btn-outline-dark">Left</button>
    <button type="button" class="btn btn-outline-dark">Middle</button>
    <button type="button" class="btn btn-outline-dark">Right</button>
</div>
<div class="btn-group btn-group-sm" role="group" aria-label="Small button group">
    <button type="button" class="btn btn-outline-dark">Left</button>
    <button type="button" class="btn btn-outline-dark">Middle</button>
    <button type="button" class="btn btn-outline-dark">Right</button>
</div>
```

```html
<!-- 大尺寸按钮组 -->
<div class="btn-group btn-group-lg" role="group" aria-label="Large button group">
    <button type="button" class="btn btn-outline-dark">Left</button>
    <button type="button" class="btn btn-outline-dark">Middle</button>
    <button type="button" class="btn btn-outline-dark">Right</button>
</div>

<!-- 默认尺寸 -->
<div class="btn-group" role="group" aria-label="Default button group">
    <button type="button" class="btn btn-outline-dark">Left</button>
    <button type="button" class="btn btn-outline-dark">Middle</button>
    <button type="button" class="btn btn-outline-dark">Right</button>
</div>

<!-- 小尺寸按钮组 -->
<div class="btn-group btn-group-sm" role="group" aria-label="Small button group">
    <button type="button" class="btn btn-outline-dark">Left</button>
    <button type="button" class="btn btn-outline-dark">Middle</button>
    <button type="button" class="btn btn-outline-dark">Right</button>
</div>
```

### **嵌套按钮组**

为了实现更复杂的效果，我们还可以把一个`.btn-group`嵌套到另外一个`.btn-group`中。  
> 该例Dropdown效果需要引入bootstrap的js文件才能正常展示。

```demo
<div class="btn-group" role="group" aria-label="Button group with nested dropdown">
  <button type="button" class="btn btn-primary">1</button>
  <button type="button" class="btn btn-primary">2</button>

  <div class="btn-group" role="group">
    <button id="btnGroupDrop1" type="button" class="btn btn-primary dropdown-toggle" data-toggle="dropdown" aria-expanded="false">
      Dropdown
    </button>
    <ul class="dropdown-menu" aria-labelledby="btnGroupDrop1">
      <li><a class="dropdown-item" href="#">Dropdown link</a></li>
      <li><a class="dropdown-item" href="#">Dropdown link</a></li>
    </ul>
  </div>
</div>
```

```html
<div class="btn-group" role="group" aria-label="Button group with nested dropdown">
  <button type="button" class="btn btn-primary">1</button>
  <button type="button" class="btn btn-primary">2</button>

  <div class="btn-group" role="group">
    <button id="btnGroupDrop1" type="button" class="btn btn-primary dropdown-toggle" data-toggle="dropdown" aria-expanded="false">
      Dropdown
    </button>
    <ul class="dropdown-menu" aria-labelledby="btnGroupDrop1">
      <li><a class="dropdown-item" href="#">Dropdown link</a></li>
      <li><a class="dropdown-item" href="#">Dropdown link</a></li>
    </ul>
  </div>
</div>
```
<!-- tabs:end -->
