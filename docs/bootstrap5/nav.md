# 导航菜单

## 默认样式

<nav class="navbar bo"><div class="nav-box"><ul class="nav"><li class="nav-item active"><a class="nav-link"href="http://">首页</a></li><li class="nav-item"><a class="nav-link"href="http://"><span class="icon"><svg class="svg-inline--fa fa-play-circle fa-w-16"aria-hidden="true"data-prefix="fas"data-icon="play-circle"role="img"xmlns="http://www.w3.org/2000/svg"viewBox="0 0 512 512"data-fa-i2svg=""><path fill="currentColor"d="M256 8C119 8 8 119 8 256s111 248 248 248 248-111 248-248S393 8 256 8zm115.7 272l-176 101c-15.8 8.8-35.7-2.5-35.7-21V152c0-18.4 19.8-29.8 35.7-21l176 107c16.4 9.2 16.4 32.9 0 42z"></path></svg></span><span>前端</span></a></li><li class="nav-item"><a class="nav-link"href="http://">设计</a></li><li class="nav-item dropdown"><a class="nav-link arrow"href="javascript:void(0);"><span>下拉</span></a><ul class="drop-menu"><li class="menu-item"><a class="menu-link"href="http://">二级栏目1</a></li><li class="menu-item"><a class="menu-link"href="http://">二级栏目2</a></li></ul></li><li class="nav-item"><a class="nav-link"href="http://">人工智能</a></li></ul></div></nav>

```HTML
<nav class="navbar bo my-2">
    <div class="nav-box">
        <ul class="nav">
            <li class="nav-item active"><a class="nav-link" href="http://">首页</a></li>
            <li class="nav-item">
                <a class="nav-link" href="http://">
                    <span class="icon"><svg class="svg-inline--fa fa-play-circle fa-w-16" aria-hidden="true" data-prefix="fas" data-icon="play-circle" role="img" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 512 512" data-fa-i2svg=""><path fill="currentColor" d="M256 8C119 8 8 119 8 256s111 248 248 248 248-111 248-248S393 8 256 8zm115.7 272l-176 101c-15.8 8.8-35.7-2.5-35.7-21V152c0-18.4 19.8-29.8 35.7-21l176 107c16.4 9.2 16.4 32.9 0 42z"></path></svg></span>
                    <span>前端</span>
                </a>
            </li>
            <li class="nav-item"><a class="nav-link" href="http://">设计</a></li>
            <li class="nav-item dropdown">
                <a class="nav-link arrow" href="javascript:void(0);"><span>下拉</span></a>
                <ul class="drop-menu">
                    <li class="menu-item"><a class="menu-link" href="http://">二级栏目1</a></li>
                    <li class="menu-item"><a class="menu-link" href="http://">二级栏目2</a></li>
                </ul>
            </li>
            <li class="nav-item"><a class="nav-link" href="http://">人工智能</a></li>
        </ul>
    </div>
</nav>
```

## 适应高度样式

 `.nav`添加 `.nav-fluid` 既为高度自适应模式

<nav class="navbar bo"><div class="nav-box"><ul class="nav nav-fluid"><li class="nav-item active"><a class="nav-link"href="http://">首页</a></li><li class="nav-item"><a class="nav-link"href="http://"><span class="icon"><svg class="svg-inline--fa fa-play-circle fa-w-16"aria-hidden="true"data-prefix="fas"data-icon="play-circle"role="img"xmlns="http://www.w3.org/2000/svg"viewBox="0 0 512 512"data-fa-i2svg=""><path fill="currentColor"d="M256 8C119 8 8 119 8 256s111 248 248 248 248-111 248-248S393 8 256 8zm115.7 272l-176 101c-15.8 8.8-35.7-2.5-35.7-21V152c0-18.4 19.8-29.8 35.7-21l176 107c16.4 9.2 16.4 32.9 0 42z"></path></svg></span><span>前端</span></a></li><li class="nav-item"><a class="nav-link"href="http://">设计</a></li><li class="nav-item dropdown"><a class="nav-link arrow"href="javascript:void(0);"><span>下拉</span></a><ul class="drop-menu"><li class="menu-item"><a class="menu-link"href="http://">二级栏目1</a></li><li class="menu-item"><a class="menu-link"href="http://">二级栏目2</a></li></ul></li><li class="nav-item"><a class="nav-link"href="http://">人工智能</a></li></ul></div></nav>

```HTML
<nav class="navbar">
    <div class="nav-box">
        <!-- .nav添加 .nav-fluid 既为高度自适应模式 -->
        <ul class="nav nav-fluid">……</ul>
    </div>
</nav>
```

## 高度收缩样式

<nav class="navbar bo"><div class="nav-box"><ul class="nav nav-sm"><li class="nav-item active"><a class="nav-link"href="http://">首页</a></li><li class="nav-item"><a class="nav-link"href="http://"><span class="icon"><svg class="svg-inline--fa fa-play-circle fa-w-16"aria-hidden="true"data-prefix="fas"data-icon="play-circle"role="img"xmlns="http://www.w3.org/2000/svg"viewBox="0 0 512 512"data-fa-i2svg=""><path fill="currentColor"d="M256 8C119 8 8 119 8 256s111 248 248 248 248-111 248-248S393 8 256 8zm115.7 272l-176 101c-15.8 8.8-35.7-2.5-35.7-21V152c0-18.4 19.8-29.8 35.7-21l176 107c16.4 9.2 16.4 32.9 0 42z"></path></svg></span><span>前端</span></a></li><li class="nav-item"><a class="nav-link"href="http://">设计</a></li><li class="nav-item dropdown"><a class="nav-link arrow"href="javascript:void(0);"><span>下拉</span></a><ul class="drop-menu"><li class="menu-item"><a class="menu-link"href="http://">二级栏目1</a></li><li class="menu-item"><a class="menu-link"href="http://">二级栏目2</a></li></ul></li><li class="nav-item"><a class="nav-link"href="http://">人工智能</a></li></ul></div></nav>

```HTML
<nav class="navbar">
    <div class="nav-box">
        <!-- .nav添加 .nav-sm 既为高度缩小模式 -->
        <ul class="nav nav-sm">……</ul>
    </div>
</nav>
```

## 右侧菜单

<nav class="navbar bo"><div class="nav-box"><ul class="nav"><li class="nav-item active"><a class="nav-link"href="http://">首页</a></li><li class="nav-item"><a class="nav-link"href="http://"><span class="icon"><svg class="svg-inline--fa fa-play-circle fa-w-16"aria-hidden="true"data-prefix="fas"data-icon="play-circle"role="img"xmlns="http://www.w3.org/2000/svg"viewBox="0 0 512 512"data-fa-i2svg=""><path fill="currentColor"d="M256 8C119 8 8 119 8 256s111 248 248 248 248-111 248-248S393 8 256 8zm115.7 272l-176 101c-15.8 8.8-35.7-2.5-35.7-21V152c0-18.4 19.8-29.8 35.7-21l176 107c16.4 9.2 16.4 32.9 0 42z"></path></svg></span><span>前端</span></a></li></ul><ul class="nav nav-right"><li class="nav-item"><a class="nav-link"href="http://">设计</a></li><li class="nav-item dropdown"><a class="nav-link arrow"href="javascript:void(0);"><span>下拉</span></a><ul class="drop-menu"><li class="menu-item"><a class="menu-link"href="http://">二级栏目1</a></li><li class="menu-item"><a class="menu-link"href="http://">二级栏目2</a></li></ul></li><li class="nav-item"><a class="nav-link"href="http://">人工智能</a></li></ul></div></nav>

```HTML
<nav class="navbar">
    <div class="nav-box">
        <!-- .nav添加 .nav-right 既为右侧菜单 -->
        <ul class="nav nav-right">……</ul>
    </div>
</nav>
```

## 下拉菜单箭头风格

<div class="navbar bo"><div class="nav-box"><ul class="nav"><li class="nav-item dropdown"><a href=""class="nav-link arrow">普通箭头下拉</a><ul class="drop-menu"><li class="menu-item"><a href=""class="menu-link">下拉菜单</a></li><li class="menu-item"><a href=""class="menu-link">下拉菜单</a></li></ul></li></ul><ul class="nav"><li class="nav-item dropdown"><a href=""class="nav-link arrow arrow-a">三角形下拉</a><ul class="drop-menu"><li class="menu-item"><a href=""class="menu-link">下拉菜单</a></li><li class="menu-item"><a href=""class="menu-link">下拉菜单</a></li></ul></li></ul><ul class="nav nav-right"><li class="nav-item dropdown"><a href=""class="nav-link">无箭头下拉</a><ul class="drop-menu"><li class="menu-item"><a href=""class="menu-link">下拉菜单</a></li><li class="menu-item"><a href=""class="menu-link">下拉菜单</a></li></ul></li></ul></div></div>

```HTML
<li class="nav-item dropdown">
    <a href=""class="nav-link arrow">普通箭头下拉</a>
    <!-- 三角箭头下拉图标 -->
    <a class="nav-link arrow arrow-a">三角箭头下拉图标 </a>
    <!-- 不显示下拉图标 -->
    <a class="nav-link">不显示下拉图标</a>
    <ul class="drop-menu">
        ...
    </ul>
</li>
```

## 独立nav(不依赖navbar)

<div class="nav-box bo"><ul class="nav"><li class="nav-item active"><a class="nav-link"href="http://">首页</a></li><li class="nav-item"><a class="nav-link"href="http://"><span class="icon"><svg class="svg-inline--fa fa-play-circle fa-w-16"aria-hidden="true"data-prefix="fas"data-icon="play-circle"role="img"xmlns="http://www.w3.org/2000/svg"viewBox="0 0 512 512"data-fa-i2svg=""><path fill="currentColor"d="M256 8C119 8 8 119 8 256s111 248 248 248 248-111 248-248S393 8 256 8zm115.7 272l-176 101c-15.8 8.8-35.7-2.5-35.7-21V152c0-18.4 19.8-29.8 35.7-21l176 107c16.4 9.2 16.4 32.9 0 42z"></path></svg></span><span>前端</span></a></li></ul><ul class="nav nav-right"><li class="nav-item"><a class="nav-link"href="http://">设计</a></li><li class="nav-item dropdown"><a class="nav-link arrow"href="javascript:void(0);"><span>下拉</span></a><ul class="drop-menu"><li class="menu-item"><a class="menu-link"href="http://">二级栏目1</a></li><li class="menu-item"><a class="menu-link"href="http://">二级栏目2</a></li></ul></li><li class="nav-item"><a class="nav-link"href="http://">人工智能</a></li></ul></div>

```HTML
<div class="nav-box bo-bottom">
    <ul class="nav">
        ...
    </ul>
    <ul class="nav nav-right">
        ...
    </ul>
</div>
```