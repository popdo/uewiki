# 消息框

## 消息类型

<div class="msg mb-1 is-primary"><i class="icon icon-msg-info text-primary"></i><strong>primary</strong>world!</div><div class="msg mb-1 is-secondary"><i class="icon icon-msg-info text-secondary"></i><strong>secondary</strong>world!</div><div class="msg mb-1 is-success"><i class="icon icon-msg-success text-success"></i><strong>success</strong>hello,world!</div><div class="msg mb-1 is-info"><i class="icon icon-msg-notice text-info"></i><strong>info</strong>一条带有关闭按钮的提示消息！<button type="button"class="close"aria-label="Close"><span aria-hidden="true">&times;</span></button></div><div class="msg mb-1 is-warning"><i class="icon icon-msg-warning text-warning"></i><strong>warning</strong>hello,world!</div><div class="msg mb-1 is-danger"><i class="icon icon-msg-danger text-danger"></i><strong>danger</strong>hello,world!</div>

```html
<div class="msg mb-1 is-primary">
    <i class="icon icon-msg-info text-primary"></i>
    <strong>primary</strong> world!
</div>
<div class="msg mb-1 is-secondary">
    <i class="icon icon-msg-info text-secondary"></i>
    <strong>secondary</strong> world!
</div>
<div class="msg mb-1 is-success">
    <i class="icon icon-msg-success text-success"></i>
    <strong>success</strong> hello,world!
</div>
<div class="msg mb-1 is-info">
    <i class="icon icon-msg-notice text-info"></i>
    <strong>info</strong>
    一条带有关闭按钮的提示消息！
    <button type="button" class="close" aria-label="Close">
        <span aria-hidden="true">&times;</span>
    </button>
</div>
<div class="msg mb-1 is-warning">
    <i class="icon icon-msg-warning text-warning"></i>
    <strong>warning</strong> hello,world!
</div>
<div class="msg mb-1 is-danger">
    <i class="icon icon-msg-danger text-danger"></i>
    <strong>danger</strong> hello,world!
</div>
```

## 浅色背景

<div class="msg sbg-primary mb-1"><i class="icon icon-msg-info text-primary"></i><strong>primary</strong>world!</div><div class="msg mb-1 sbg-secondary"><i class="icon icon-msg-info text-secondary"></i><strong>secondary</strong>world!</div><div class="msg mb-1 sbg-success"><i class="icon icon-msg-success text-success"></i><strong>success</strong>hello,world!</div><div class="msg mb-1 sbg-info hover-shadow"><i class="icon icon-msg-notice text-info"></i><strong>info</strong>一条带有关闭按钮的提示消息！<button type="button"class="close"aria-label="Close"><span aria-hidden="true">&times;</span></button></div><div class="msg mb-1 sbg-warning"><i class="icon icon-msg-warning text-warning"></i><strong>warning</strong>hello,world!</div><div class="msg mb-2 sbg-danger"><i class="icon icon-msg-danger text-danger"></i><strong>danger</strong>hello,world!</div>

通过添加`.sbg-color`实现浅色背景

```html
<div class="msg sbg-primary">
    <i class="icon icon-msg-info text-primary"></i>
    <strong>primary</strong> world!
</div>
```

## Alert弹层

<div class="alert is-primary bo"><div class="alert-hd"><i class="icon icon-click-s text-primary"></i><h5 class="title">温馨提示</h5></div><div class="alert-bd">关于暂停用户发布功能，并全面清查平台内容</div><div class="alert-ft flex-xy-c"><button class="btn is-success">确定</button><button class="btn is-light">取消</button></div></div>

```html
<div class="alert is-primary bo">
    <div class="alert-hd">
        <i class="icon icon-click-s text-primary"></i>
        <h5 class="title">温馨提示</h5> 
    </div>
    <div class="alert-bd">
        关于暂停用户发布功能，并全面清查平台内容
    </div>
    <div class="alert-ft flex-xy-c">
        <button class="btn is-success">确定</button>
        <button class="btn is-light">取消</button>
    </div>
</div>
```

<div class="alert is-success bo"><div class="alert-hd"><i class="icon icon-msg-checkb text-success"></i><h5 class="title">发布成功</h5></div><div class="alert-bd">恭喜你！操作成功了……</div><div class="alert-ft flex-xy-c"><button class="btn is-success">知道了</button></div></div>

```html
<div class="alert is-success bo">
    <div class="alert-hd">
        <i class="icon icon-msg-checkb text-success"></i>
        <h5 class="title">发布成功</h5> 
    </div>
    <div class="alert-bd">
        恭喜你！操作成功了……
    </div>
    <div class="alert-ft flex-xy-c">
        <button class="btn is-success">知道了</button>
    </div>
</div>
```

<div class="alert is-danger bo"><div class="alert-hd text-danger"><i class="icon icon-msg-danger"></i><h5 class="title">出错了</h5></div><div class="alert-bd">很抱歉，您未能设置成功……</div><div class="alert-ft flex-xy-c"><button class="btn is-success">确定</button><button class="btn is-light">取消</button></div></div>

```html
<div class="alert is-danger bo">
    <div class="alert-hd text-danger">
        <i class="icon icon-msg-danger"></i>
        <h5 class="title">出错了</h5> 
    </div>
    <div class="alert-bd">
        很抱歉，您未能设置成功……
    </div>
    <div class="alert-ft flex-xy-c">
        <button class="btn is-success">确定</button>
        <button class="btn is-light">取消</button>
    </div>
</div>
```
<div class="alert is-warning bo"><div class="alert-hd"><i class="icon icon-msg-question text-warning"></i><h5 class="title">确认信息</h5></div><div class="alert-bd">你确定要删除该用户吗?</div><div class="alert-ft flex-xy-c"><button class="btn is-success">确定</button><button class="btn is-light">取消</button></div></div>

```html
<div class="alert is-warning bo">
    <div class="alert-hd">
        <i class="icon icon-msg-question text-warning"></i>
        <h5 class="title">确认信息</h5> 
    </div>
    <div class="alert-bd">
        你确定要删除该用户吗?
    </div>
    <div class="alert-ft flex-xy-c">
        <button class="btn is-success">确定</button>
        <button class="btn is-light">取消</button>
    </div>
</div>
```