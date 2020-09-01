# 表格

由于`<table>`元素在第三方（如日历和日期选择器）中的广泛使用，Bootstrap的表格是可选的。将基类`.table`添加到任何的`<table>`中，然后用我们可选的修饰类或自定义样式进行扩展。在Bootstrap中，所有的表格样式都是不继承的，这意味着任何嵌套的表格都可以独立于父表的样式。

## 表格样式

<!-- tabs:start -->

### **基础表格**

```demo
<table class="table d-table">
  <thead>
    <tr>
      <th scope="col">#</th>
      <th scope="col">First</th>
      <th scope="col">Last</th>
      <th scope="col">Handle</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th scope="row">1</th>
      <td>Mark</td>
      <td>Otto</td>
      <td>@mdo</td>
    </tr>
    <tr>
      <th scope="row">2</th>
      <td>Jacob</td>
      <td>Thornton</td>
      <td>@fat</td>
    </tr>
    <tr>
      <th scope="row">3</th>
      <td colspan="2">Larry the Bird</td>
      <td>@twitter</td>
    </tr>
  </tbody>
</table>
<table class="table table-dark d-table">
      <thead>
    <tr>
      <th scope="col">#</th>
      <th scope="col">First</th>
      <th scope="col">Last</th>
      <th scope="col">Handle</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th scope="row">1</th>
      <td>Mark</td>
      <td>Otto</td>
      <td>@mdo</td>
    </tr>
    <tr>
      <th scope="row">2</th>
      <td>Jacob</td>
      <td>Thornton</td>
      <td>@fat</td>
    </tr>
    <tr>
      <th scope="row">3</th>
      <td colspan="2">Larry the Bird</td>
      <td>@twitter</td>
    </tr>
  </tbody>

  </table>
```

```html
<table class="table">
  ...
</table>

<!-- 所有.table都支持添加配色类 -->
<table class="table table-dark">
  ...
</table>
```

### **条纹表格**

```demo
<table class="table table-striped d-table">
      <thead>
        <tr>
          <th scope="col">#</th>
          <th scope="col">First</th>
          <th scope="col">Last</th>
          <th scope="col">Handle</th>
        </tr>
      </thead>
      <tbody>
        <tr>
          <th scope="row">1</th>
          <td>Mark</td>
          <td>Otto</td>
          <td>@mdo</td>
        </tr>
        <tr>
          <th scope="row">2</th>
          <td>Jacob</td>
          <td>Thornton</td>
          <td>@fat</td>
        </tr>
        <tr>
          <th scope="row">3</th>
          <td colspan="2">Larry the Bird</td>
          <td>@twitter</td>
        </tr>
      </tbody>
  </table>
  <table class="table table-dark table-striped d-table">
      <thead>
        <tr>
          <th scope="col">#</th>
          <th scope="col">First</th>
          <th scope="col">Last</th>
          <th scope="col">Handle</th>
        </tr>
      </thead>
      <tbody>
        <tr>
          <th scope="row">1</th>
          <td>Mark</td>
          <td>Otto</td>
          <td>@mdo</td>
        </tr>
        <tr>
          <th scope="row">2</th>
          <td>Jacob</td>
          <td>Thornton</td>
          <td>@fat</td>
        </tr>
        <tr>
          <th scope="row">3</th>
          <td colspan="2">Larry the Bird</td>
          <td>@twitter</td>
        </tr>
      </tbody>
  </table>
```

```html
<table class="table table-striped">
  ...
</table>

<table class="table table-dark table-striped">
  ...
</table>
```

### **悬停表格**

```demo
<table class="table table-hover d-table">
      <thead>
        <tr>
          <th scope="col">#</th>
          <th scope="col">First</th>
          <th scope="col">Last</th>
          <th scope="col">Handle</th>
        </tr>
      </thead>
      <tbody>
        <tr>
          <th scope="row">1</th>
          <td>Mark</td>
          <td>Otto</td>
          <td>@mdo</td>
        </tr>
        <tr>
          <th scope="row">2</th>
          <td>Jacob</td>
          <td>Thornton</td>
          <td>@fat</td>
        </tr>
        <tr>
          <th scope="row">3</th>
          <td colspan="2">Larry the Bird</td>
          <td>@twitter</td>
        </tr>
      </tbody>
  </table>
  <table class="table table-dark table-hover d-table">
      <thead>
        <tr>
          <th scope="col">#</th>
          <th scope="col">First</th>
          <th scope="col">Last</th>
          <th scope="col">Handle</th>
        </tr>
      </thead>
      <tbody>
        <tr>
          <th scope="row">1</th>
          <td>Mark</td>
          <td>Otto</td>
          <td>@mdo</td>
        </tr>
        <tr>
          <th scope="row">2</th>
          <td>Jacob</td>
          <td>Thornton</td>
          <td>@fat</td>
        </tr>
        <tr>
          <th scope="row">3</th>
          <td colspan="2">Larry the Bird</td>
          <td>@twitter</td>
        </tr>
      </tbody>
  </table>
```

```html
<table class="table table-hover">
  ...
</table>

<table class="table table-dark table-hover">
  ...
</table>
```

### **活动表格**

通过添加`.table-active`类突出显示表格行或单元格。

```demo
<table class="table d-table">
    <thead>
      <tr>
        <th scope="col">#</th>
        <th scope="col">First</th>
        <th scope="col">Last</th>
        <th scope="col">Handle</th>
      </tr>
    </thead>
    <tbody>
      <tr class="table-active">
        <th scope="row">1</th>
        <td>Mark</td>
        <td>Otto</td>
        <td>@mdo</td>
      </tr>
      <tr>
        <th scope="row">2</th>
        <td>Jacob</td>
        <td>Thornton</td>
        <td>@fat</td>
      </tr>
      <tr>
        <th scope="row">3</th>
        <td colspan="2" class="table-active">Larry the Bird</td>
        <td>@twitter</td>
      </tr>
    </tbody>
  </table>
<table class="table table-dark d-table">
    <thead>
      <tr>
        <th scope="col">#</th>
        <th scope="col">First</th>
        <th scope="col">Last</th>
        <th scope="col">Handle</th>
      </tr>
    </thead>
    <tbody>
      <tr class="table-active">
        <th scope="row">1</th>
        <td>Mark</td>
        <td>Otto</td>
        <td>@mdo</td>
      </tr>
      <tr>
        <th scope="row">2</th>
        <td>Jacob</td>
        <td>Thornton</td>
        <td>@fat</td>
      </tr>
      <tr>
        <th scope="row">3</th>
        <td colspan="2" class="table-active">Larry the Bird</td>
        <td>@twitter</td>
      </tr>
    </tbody>
  </table>
```

```html
<table class="table">
  <thead>
    ...
  </thead>
  <tbody>
    <tr class="table-active">
      ...
    </tr>
    <tr>
      ...
    </tr>
    <tr>
      <th scope="row">3</th>
      <td colspan="2" class="table-active">Larry the Bird</td>
      <td>@twitter</td>
    </tr>
  </tbody>
</table>
```

### **边框表格**

```demo
<table class="table table-bordered d-table">
      <thead>
    <tr>
      <th scope="col">#</th>
      <th scope="col">First</th>
      <th scope="col">Last</th>
      <th scope="col">Handle</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th scope="row">1</th>
      <td>Mark</td>
      <td>Otto</td>
      <td>@mdo</td>
    </tr>
    <tr>
      <th scope="row">2</th>
      <td>Jacob</td>
      <td>Thornton</td>
      <td>@fat</td>
    </tr>
    <tr>
      <th scope="row">3</th>
      <td colspan="2">Larry the Bird</td>
      <td>@twitter</td>
    </tr>
  </tbody>
  </table>
<table class="table table-bordered border-primary d-table">
      <thead>
    <tr>
      <th scope="col">#</th>
      <th scope="col">First</th>
      <th scope="col">Last</th>
      <th scope="col">Handle</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th scope="row">1</th>
      <td>Mark</td>
      <td>Otto</td>
      <td>@mdo</td>
    </tr>
    <tr>
      <th scope="row">2</th>
      <td>Jacob</td>
      <td>Thornton</td>
      <td>@fat</td>
    </tr>
    <tr>
      <th scope="row">3</th>
      <td colspan="2">Larry the Bird</td>
      <td>@twitter</td>
    </tr>
  </tbody>
  </table>
```

```html
<table class="table table-bordered">
  ...
</table>

<table class="table table-bordered border-primary">
  ...
</table>
```

### **极简表格**

```demo
<table class="table table-borderless d-table">
      <thead>
    <tr>
      <th scope="col">#</th>
      <th scope="col">First</th>
      <th scope="col">Last</th>
      <th scope="col">Handle</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th scope="row">1</th>
      <td>Mark</td>
      <td>Otto</td>
      <td>@mdo</td>
    </tr>
    <tr>
      <th scope="row">2</th>
      <td>Jacob</td>
      <td>Thornton</td>
      <td>@fat</td>
    </tr>
    <tr>
      <th scope="row">3</th>
      <td colspan="2">Larry the Bird</td>
      <td>@twitter</td>
    </tr>
  </tbody>
  </table>
  <table class="table table-primary table-borderless d-table">
      <thead>
    <tr>
      <th scope="col">#</th>
      <th scope="col">First</th>
      <th scope="col">Last</th>
      <th scope="col">Handle</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th scope="row">1</th>
      <td>Mark</td>
      <td>Otto</td>
      <td>@mdo</td>
    </tr>
    <tr>
      <th scope="row">2</th>
      <td>Jacob</td>
      <td>Thornton</td>
      <td>@fat</td>
    </tr>
    <tr>
      <th scope="row">3</th>
      <td colspan="2">Larry the Bird</td>
      <td>@twitter</td>
    </tr>
  </tbody>
  </table>
```

```html
<table class="table table-borderless">
  ...
</table>

<table class="table table-primary table-borderless">
  ...
</table>
```

### **小尺寸表格**

```demo
<table class="table table-dark table-sm d-table">
      <thead>
    <tr>
      <th scope="col">#</th>
      <th scope="col">First</th>
      <th scope="col">Last</th>
      <th scope="col">Handle</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th scope="row">1</th>
      <td>Mark</td>
      <td>Otto</td>
      <td>@mdo</td>
    </tr>
    <tr>
      <th scope="row">2</th>
      <td>Jacob</td>
      <td>Thornton</td>
      <td>@fat</td>
    </tr>
    <tr>
      <th scope="row">3</th>
      <td colspan="2">Larry the Bird</td>
      <td>@twitter</td>
    </tr>
  </tbody>

  </table>
```

```html
<table class="table table-dark table-sm">
  ...
</table>
```

<!-- tabs:end -->

## 垂直对齐

```demo
<div class="table-responsive">
    <table class="table align-middle">
      <thead>
        <tr>
          <th scope="col" class="w-25">Heading 1</th>
          <th scope="col" class="w-25">Heading 2</th>
          <th scope="col" class="w-25">Heading 3</th>
          <th scope="col" class="w-25">Heading 4</th>
        </tr>
      </thead>
      <tbody>
        <tr>
          <td>此单元格继承了table的<code>.align-middle</code></td>
          <td>此单元格继承了table的<code>.align-middle</code></td>
          <td>此单元格继承了table的<code>.align-middle</code></td>
          <td>Nulla vitae elit libero, a pharetra augue. Cras mattis consectetur purus sit amet fermentum. Vestibulum id ligula porta felis euismod semper.</td>
        </tr>
        <tr class="align-bottom">
          <td>此单元格继承了tr的<code>.align-bottom</code></td>
          <td>此单元格继承了tr的<code>.align-bottom</code></td>
          <td>此单元格继承了tr的<code>.align-bottom</code></td>
          <td>Nulla vitae elit libero, a pharetra augue. Cras mattis consectetur purus sit amet fermentum. Vestibulum id ligula porta felis euismod semper.</td>
        </tr>
        <tr>
          <td>此单元格继承了table的<code>.align-middle</code></td>
          <td>此单元格继承了table的<code>.align-middle</code></td>
          <td class="align-top">此单元格单独<code>.align-top</code></td>
          <td>Nulla vitae elit libero, a pharetra augue. Cras mattis consectetur purus sit amet fermentum. Vestibulum id ligula porta felis euismod semper.</td>
        </tr>
      </tbody>
    </table>
  </div>
```

```html
<div class="table-responsive">
  <table class="table align-middle">
    <thead>
      <tr>
        ...
      </tr>
    </thead>
    <tbody>
      <tr>
        ...
      </tr>
      <tr class="align-bottom">
        ...
      </tr>
      <tr>
        <td>...</td>
        <td>...</td>
        <td class="align-top">This cell is aligned to the top.</td>
        <td>...</td>
      </tr>
    </tbody>
  </table>
</div>
```

## 表格上色

多色表格的样式类是`.table-{color}`,它可以单独放置在表格中的任意`table`、`thead`、`tbody`、`tr`、`td`等元素上面。

```demo
<table class="table d-table">
    <thead>
      <tr>
        <th scope="col">Class</th>
        <th scope="col">Heading</th>
        <th scope="col">Heading</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <th scope="row">Default</th>
        <td>Cell</td>
        <td>Cell</td>
      </tr>

        <tr class="table-primary">
          <th scope="row">Primary</th>
          <td>Cell</td>
          <td>Cell</td>
        </tr>
        <tr class="table-secondary">
          <th scope="row">Secondary</th>
          <td>Cell</td>
          <td>Cell</td>
        </tr>
        <tr class="table-success">
          <th scope="row">Success</th>
          <td>Cell</td>
          <td>Cell</td>
        </tr>
        <tr class="table-danger">
          <th scope="row">Danger</th>
          <td>Cell</td>
          <td>Cell</td>
        </tr>
        <tr class="table-warning">
          <th scope="row">Warning</th>
          <td>Cell</td>
          <td>Cell</td>
        </tr>
        <tr class="table-info">
          <th scope="row">Info</th>
          <td>Cell</td>
          <td>Cell</td>
        </tr>
        <tr class="table-light">
          <th scope="row">Light</th>
          <td>Cell</td>
          <td>Cell</td>
        </tr>
        <tr class="table-dark">
          <th scope="row">Dark</th>
          <td>Cell</td>
          <td>Cell</td>
        </tr>
    </tbody>
  </table>
```

```html
<!-- On tables -->
<table class="table-primary">...</table>
<table class="table-secondary">...</table>
<table class="table-success">...</table>
<table class="table-danger">...</table>
<table class="table-warning">...</table>
<table class="table-info">...</table>
<table class="table-light">...</table>
<table class="table-dark">...</table>

<!-- On rows -->
<tr class="table-primary">...</tr>
<tr class="table-secondary">...</tr>
<tr class="table-success">...</tr>
<tr class="table-danger">...</tr>
<tr class="table-warning">...</tr>
<tr class="table-info">...</tr>
<tr class="table-light">...</tr>
<tr class="table-dark">...</tr>

<!-- On cells (`td` or `th`) -->
<tr>
  <td class="table-primary">...</td>
  <td class="table-secondary">...</td>
  <td class="table-success">...</td>
  <td class="table-danger">...</td>
  <td class="table-warning">...</td>
  <td class="table-info">...</td>
  <td class="table-light">...</td>
  <td class="table-dark">...</td>
</tr>

```

## 响应式表格

响应式表格可以轻松的水平滚动表格,尤其是在可视尺寸有限的手机屏幕上，响应式表格可以通过触摸划动屏幕以完整的显示表格所有内容。

- 通过将`.table`放置于一个类名称为`.table-responsive`的容器中即可。
- 也可以给响应表格的父容器选择一个最大断点`.table-responsible-{sm|md|lg|xl|-xxl}`。

可以在小尺寸的屏幕上滑动该表格试试：

```demo
<div class="table-responsive">
    <table class="table d-table">
      <thead>
        <tr>
          <th scope="col">#</th>
          <th scope="col">Heading</th>
          <th scope="col">Heading</th>
          <th scope="col">Heading</th>
          <th scope="col">Heading</th>
          <th scope="col">Heading</th>
          <th scope="col">Heading</th>
          <th scope="col">Heading</th>
          <th scope="col">Heading</th>
          <th scope="col">Heading</th>
        </tr>
      </thead>
      <tbody>
        <tr>
          <th scope="row">1</th>
          <td>Cell</td>
          <td>Cell</td>
          <td>Cell</td>
          <td>Cell</td>
          <td>Cell</td>
          <td>Cell</td>
          <td>Cell</td>
          <td>Cell</td>
          <td>Cell</td>
        </tr>
        <tr>
          <th scope="row">2</th>
          <td>Cell</td>
          <td>Cell</td>
          <td>Cell</td>
          <td>Cell</td>
          <td>Cell</td>
          <td>Cell</td>
          <td>Cell</td>
          <td>Cell</td>
          <td>Cell</td>
        </tr>
        <tr>
          <th scope="row">3</th>
          <td>Cell</td>
          <td>Cell</td>
          <td>Cell</td>
          <td>Cell</td>
          <td>Cell</td>
          <td>Cell</td>
          <td>Cell</td>
          <td>Cell</td>
          <td>Cell</td>
        </tr>
      </tbody>
    </table>
  </div>
```

```html
<div class="table-responsive">
  <table class="table">
    ...
  </table>
</div>
```

## 在sass中自定义表格

- The factor variables (`$table-striped-bg-factor`, `$table-active-bg-factor` & `$table-hover-bg-factor`) are used to determine the contrast in table variants.
- Apart from the light & dark table variants, theme colors are lightened by the `$table-bg-level` variable.

```scss
$table-cell-padding-y:        .5rem;
$table-cell-padding-x:        .5rem;
$table-cell-padding-y-sm:     .25rem;
$table-cell-padding-x-sm:     .25rem;

$table-cell-vertical-align:   top;

$table-color:                 $body-color;
$table-bg:                    transparent;

$table-striped-color:         $table-color;
$table-striped-bg-factor:     .05;
$table-striped-bg:            rgba($black, $table-striped-bg-factor);

$table-active-color:          $table-color;
$table-active-bg-factor:      .1;
$table-active-bg:             rgba($black, $table-active-bg-factor);

$table-hover-color:           $table-color;
$table-hover-bg-factor:       .075;
$table-hover-bg:              rgba($black, $table-hover-bg-factor);

$table-border-factor:         .1;
$table-border-width:          $border-width;
$table-border-color:          $border-color;

$table-striped-order:         odd;

$table-group-seperator-color: currentColor;

$table-caption-color:         $text-muted;

$table-bg-level:              -9;

$table-variants: (
  "primary":    color-level($primary, $table-bg-level),
  "secondary":  color-level($secondary, $table-bg-level),
  "success":    color-level($success, $table-bg-level),
  "info":       color-level($info, $table-bg-level),
  "warning":    color-level($warning, $table-bg-level),
  "danger":     color-level($danger, $table-bg-level),
  "light":      $light,
  "dark":       $dark,
);
```
