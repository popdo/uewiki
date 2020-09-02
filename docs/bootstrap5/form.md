# 表单

## 表单对照表

|类名|说明|
|-----|-----|
|`.form-text`|表单文字，一般用于对表单内容的补充和说明|
|`.form-label`|单元行的label标签|
|`.col-form-label`|单元行的label标签|
|`.form-control`<br>`.form-control .form-control-sm`<br>`.form-control .form-control-lg`|表单大小控制|
|`disabled`标签|禁用|
|`readonly`标签|只读|
|`.form-control-plaintext`|让input看起来像普通文本，一般配合readonly标签使用|

## 禁用表单

### 禁用表单元素 <!-- {docsify-ignore} -->

给表单元素添加`disabled`类可以禁止点击。

```demo
<input class="form-control" type="text" placeholder="Disabled input here..." disabled>
```

```html
<input class="form-control" type="text" placeholder="Disabled input here..." disabled>
```

### 禁用整个表单 <!-- {docsify-ignore} -->

将`disabled`属性添加到`<fieldset>`以禁用表单中的所有控件。  
默认情况下，浏览器将把`<fieldset disabled>`中的所有原生表单控件（`<input>`、`<select>`和`<button>`元素）视为禁用，从而阻止键盘和鼠标的交互。  
但是，如果您的表格中还包括`<a ... class="btn btn-*">`元素，这些元素将只被赋予css样式`pointer-events:none`。

```demo
<form>
  <fieldset disabled aria-label="Disabled fieldset example">
    <div class="mb-3">
      <label for="disabledTextInput" class="form-label">Disabled input</label>
      <input type="text" id="disabledTextInput" class="form-control" placeholder="Disabled input">
    </div>
    <div class="mb-3">
      <label for="disabledSelect" class="form-label">Disabled select menu</label>
      <select id="disabledSelect" class="form-select">
        <option>Disabled select</option>
      </select>
    </div>
    <div class="mb-3">
      <div class="form-check">
        <input class="form-check-input" type="checkbox" id="disabledFieldsetCheck" disabled>
        <label class="form-check-label" for="disabledFieldsetCheck">
          Can't check this
        </label>
      </div>
    </div>
    <button type="submit" class="btn btn-primary">Submit</button>
  </fieldset>
</form>
```

```html
<form>
  <fieldset disabled aria-label="Disabled fieldset example">
    ...
  </fieldset>
</form>
```

