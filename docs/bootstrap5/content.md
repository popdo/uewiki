# 内容

## 全局设置

为了在媒体响应上具有更好的体验bootstrap使用rem作为尺寸单位。为了更容易地跨设备大小缩放，块元素应该使用rem作为边距。尽可能使用inherit，尽量减少字体相关属性不必要的声明。

更新`<html>`和`<body>`元素以提供更好的页面范围默认值。更具体地说：

- `box-sizing:border-box`是在每个元素上全局设置的，包括`*::before`和`*::after`，以确保不会超过此元素的边框宽度。
- `<html>`上没有声明基本字体大小，但假定为16px（浏览器默认值）。字体大小：1rem应用于`<body>`上，以便通过媒体查询轻松响应类型缩放，同时尊重用户偏好并确保更易访问的方法。可以通过修改`$font-size`根变量来覆盖此浏览器默认值。
- `<body>`还设置了全局`font-family`, `font-weight`, `line-height`和`color`。某些表单元素会继承这一特性，以防止字体不一致。
- 为了安全起见，`<body>`有一个声明的背景色，默认为#fff。

### 常用标签

|标签|类名支持|说明|示例|
|---|-------|---|----|
|`<code>`||内联代码|`.cc{color:#ccc}`|
|`<pre>`<br>`<code>...</code>`<br>`</pre>`||代码块||
|`<var>`||变量|<var>var</var>|
|`<kbd>`||键盘符|<kbd>Shift</kbd>|
|`<samp>`||是一个短语标签，用来定义计算机程序的样本文本|<samp>样本文本</samp>|
|`<address>`||地址|<address><a href="mailto:first.last@example.com">first.last@example.com</a></address>|
|`<abbr>`||标记一个简称、缩写|Nulla <abbr title="attribute">attr</abbr> vitae elit libero, a pharetra augue.|
|`<blockquote>`|.blockquote|引用文档中其他来源的内容块，更详细查看[官方文档](https://v5.getbootstrap.com/docs/5.0/content/typography/#blockquotes)|<blockquote>小鸟飞的很高，很远...</blockquote>|
|`<mark>`||表示标记或突出显示以供参考或表示的文本。||
|`<small>`||代表旁注和小字体，如版权和法律文本。||
|`<s>`||表示不再相关或不再准确的元素。||
|`<u>`||表示应以指示其具有非文本批注的方式呈现的内联文本的范围。||
|`<b>`||为了突出单词或短语而不传达额外的重要性||
|`<em>`||||
|`<i>`||主要用于语音、技术术语等||

## 版式设计

### 标题和段落

如果想在`h1~h6`以外的元素上使用同样的标题效果可以添加`.h1`~`.h6`类名 即可。

|Heading|Example|更大的标题(类名:display-*)|
|-------|-------|--------|
|h1|<span class="h1">h1. Bootstrap heading</span>|<span class="display-1">Display1 Bootstrap heading</span>|
|h2|<span class="h2">h2. Bootstrap heading</span>|<span class="display-2">Display2 Bootstrap heading</span>|
|h3|<span class="h3">h3. Bootstrap heading</span>|<span class="display-3">Display3 Bootstrap heading</span>|
|h4|<span class="h4">h4. Bootstrap heading</span>|<span class="display-4">Display4 Bootstrap heading</span>|
|h5|<span class="h5">h5. Bootstrap heading</span>|<span class="display-5">Display5 Bootstrap heading</span>|
|h6|<span class="h6">h6. Bootstrap heading</span>|<span class="display-6">Display6 Bootstrap heading</span>|

### 列表

所有列表-`<ul>`、`<ol>`和`<dl>`都删除了它们的页边距顶部和底部边距：1rem。嵌套列表没有边距底端。我们还重置了左边的元素。

<!-- tabs:start -->

#### **ul列表**

```demo
<ul>
  <li>一级li</li>
  <li>Consectetur adipiscing elit</li>
  <li>Facilisis in pretium nisl aliquet</li>
  <li>Nulla volutpat aliquam velit
    <ul>
      <li>二级li</li>
      <li>Purus sodales ultricies</li>
      <li>Vestibulum laoreet porttitor sem</li>
    </ul>
  </li>
</ul>
<hr>
<ul class="list-unstyled">
  <li>无样式列表</li>
  <li>Aenean sit amet erat nunc</li>
  <li>Eget porttitor lorem</li>
</ul>
<hr>
<ul class="list-inline">
  <li class="list-inline-item">行内列表li1</li>
  <li class="list-inline-item">行内列表li2</li>
  <li class="list-inline-item">行内列表li3</li>
</ul>
```

```html
<ul>
  <li>一级li</li>
  <li>Nulla volutpat aliquam velit
    <ul>
      <li>二级li</li>
    </ul>
  </li>
</ul>
<hr>

<!-- 无样式列表 -->
<ul class="list-unstyled">
  <li>无样式列表</li>
</ul>

<!-- 行内列表 -->
<ul class="list-inline">
  <li class="list-inline-item">行内列表li1</li>
  <li class="list-inline-item">行内列表li2</li>
  <li class="list-inline-item">行内列表li3</li>
</ul>
```

#### **ol列表**

```demo
<ol>
  <li>一级li</li>
  <li>Consectetur adipiscing elit</li>
  <li>Facilisis in pretium nisl aliquet</li>
  <li>Nulla volutpat aliquam velit
    <ol>
      <li>二级li</li>
      <li>Purus sodales ultricies</li>
      <li>Vestibulum laoreet porttitor sem</li>
    </ol>
  </li>
</ol>
<hr>
<!-- 无样式列表 -->
<ol class="list-unstyled">
  <li>无样式列表</li>
  <li>Aenean sit amet erat nunc</li>
  <li>Eget porttitor lorem</li>
</ol>
```

```html
<ol>
  <li>一级li</li>
  <li>Nulla volutpat aliquam velit
    <ol>
      <li>二级li</li>
    </ol>
  </li>
</ol>
<hr>

<!-- 无样式列表 -->
<ol class="list-unstyled">
  <li>无样式列表</li>
</ol>
```

#### **dl列表**

```demo
<dl>
    <dt>Description lists</dt>
    <dd>A description list is perfect for defining terms.</dd>
    <dt>Euismod</dt>
    <dd>Vestibulum id ligula porta felis euismod semper eget lacinia odio sem.</dd>
    <dd>Donec id elit non mi porta gravida at eget metus.</dd>
    <dt>Malesuada porta</dt>
    <dd>Etiam porta sem malesuada magna mollis euismod.</dd>
</dl>
```

```html
<dl>
    <dt>Description lists</dt>
    <dd>A description list is perfect for defining terms.</dd>
    <dt>Euismod</dt>
    <dd>Vestibulum id ligula porta felis euismod semper eget lacinia odio sem.</dd>
    <dd>Donec id elit non mi porta gravida at eget metus.</dd>
    <dt>Malesuada porta</dt>
    <dd>Etiam porta sem malesuada magna mollis euismod.</dd>
</dl>
```

<!-- tabs:end -->

### 突出段落

通过加上"`.lead`"使段落突出。
```demo
<p>
  Vivamus sagittis lacus vel augue laoreet rutrum faucibus dolor auctor. Duis mollis, est non commodo luctus.
</p>
<p class="lead">
  Vivamus sagittis lacus vel augue laoreet rutrum faucibus dolor auctor. Duis mollis, est non commodo luctus.
</p>
```

```html
<p>
  Vivamus sagittis lacus vel augue laoreet rutrum faucibus dolor auctor. Duis mollis, est non commodo luctus.
</p>
<p class="lead">
  Vivamus sagittis lacus vel augue laoreet rutrum faucibus dolor auctor. Duis mollis, est non commodo luctus.
</p>
```

### 内嵌文本元素

为常见的内联HTML5元素设计样式。

```demo
<p>mark:You can use the mark tag to <mark>highlight</mark> text.</p>
<p>del:<del>This line of text is meant to be treated as deleted text.</del></p>
<p>s:<s>This line of text is meant to be treated as no longer accurate.</s></p>
<p>ins:<ins>This line of text is meant to be treated as an addition to the document.</ins></p>
<p>u:<u>This line of text will render as underlined</u></p>
<p>small:<small>This line of text is meant to be treated as fine print.</small></p>
<p>strong:<strong>This line rendered as bold text.</strong></p>
<p>em:<em>This line rendered as italicized text.</em></p>
```

```html
<p>You can use the mark tag to <mark>highlight</mark> text.</p>
<p><del>This line of text is meant to be treated as deleted text.</del></p>
<p><s>This line of text is meant to be treated as no longer accurate.</s></p>
<p><ins>This line of text is meant to be treated as an addition to the document.</ins></p>
<p><u>This line of text will render as underlined</u></p>
<p><small>This line of text is meant to be treated as fine print.</small></p>
<p><strong>This line rendered as bold text.</strong></p>
<p><em>This line rendered as italicized text.</em></p>
```

