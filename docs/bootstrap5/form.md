# 表单

## input

**#尺寸**
<div style="padding:10px;background:#f5f5f5"><input class="form-item is-sm mb-1" type="text" placeholder="Small input">
<input class="form-item mb-1" type="text" placeholder="Normal input">
<input class="form-item is-md mb-1" type="text" placeholder="Medium input">
<input class="form-item is-lg" type="text" placeholder="Large input"></div>

```html
<input class="form-item is-sm" type="text" placeholder="Small input">
<input class="form-item" type="text" placeholder="Normal input">
<input class="form-item is-md" type="text" placeholder="Medium input">
<input class="form-item is-lg" type="text" placeholder="Large input">
```

## textarea

<div class="bo p-2"><textarea class="form-item" placeholder="Explain how we can form-text you"></textarea></div>

```html
<textarea class="form-item" placeholder="Explain how we can form-text you"></textarea>
```

## select

**#单选**
<div class="select is-fullwidth"><select class="form-item"><option>Business development</option><option>Marketing</option><option>Sales</option></select></div>

```html
<div class="select is-fullwidth">
    <select class="form-item">
        <option>Business development</option>
        <option>Marketing</option>
        <option>Sales</option>
    </select>
</div>
```

**#多选**

待完善~
<div class="select is-multiple"><select class="form-item h-auto" multiple size="8"><option value="Argentina">Argentina</option><option value="Bolivia">Bolivia</option><option value="Brazil">Brazil</option><option value="Chile">Chile</option><option value="Colombia">Colombia</option></select></div>

```html
<div class="select is-multiple">
    <select class="form-item h-auto" multiple size="8">
        <option value="Argentina">Argentina</option>
        <option value="Bolivia">Bolivia</option>
        <option value="Brazil">Brazil</option>
        <option value="Chile">Chile</option>
        <option value="Colombia">Colombia</option>
    </select>
</div>
```

## radio

<div class="field-bd bo p-2 mb-1"><input class="is-radio" type="radio" name="x_1" id="x_1_1" checked="checked"><label for="x_1_1">Yes</label><input class="is-radio" type="radio" name="x_1" id="x_1_2"><label for="x_1_2">No</label><input class="is-radio" type="radio" name="x_1" id="x_1_3" disabled="disabled"><label for="x_1_3">disabled</label></div>

<div class="field-bd bo p-2"><input class="is-radio is-success" type="radio" name="" id="radio1" checked="checked"><label for="radio1">success</label><input class="is-radio is-danger" type="radio" name="" id="radio2" checked="checked"><label for="radio2">danger</label><input class="is-radio is-info" type="radio" name="" id="radio3" checked="checked"><label for="radio3">info</label><input class="is-radio is-warning" type="radio" name="" id="radio4" checked="checked"><label for="radio4">warning</label><input class="is-radio is-dark" type="radio" name="" id="radio5" checked="checked"><label for="radio5">dark</label><input class="is-radio" type="radio" name="" id="radio6" checked="checked"><label for="radio6">primary</label><input class="is-radio" type="radio" name="" id="radio6" checked="checked" disabled="disabled"><label for="radio6">disabled</label></div>

```html
<div class="field-bd">
	<input class="is-radio is-success" type="radio" name="" id="radio1" checked="checked">
	<label for="radio1">success</label>

	<input class="is-radio is-danger" type="radio" name="" id="radio2" checked="checked">
	<label for="radio2">danger</label>

	<input class="is-radio is-info" type="radio" name="" id="radio3" checked="checked">
	<label for="radio3">info</label>

	<input class="is-radio is-warning" type="radio" name="" id="radio4" checked="checked">
	<label for="radio4">warning</label>

	<input class="is-radio is-dark" type="radio" name="" id="radio5" checked="checked">
	<label for="radio5">dark</label>

	<input class="is-radio" type="radio" name="" id="radio6" checked="checked">
	<label for="radio6">primary</label>

	<input class="is-radio" type="radio" name="" id="radio6" checked="checked" disabled>
	<label for="radio6">disabled</label>
</div>
```

## checkbox

<div class="field-bd bo p-2 mb-1"><input class="is-checkbox is-success" id="suc1" type="checkbox" name="x_2" checked="checked"><label for="suc1">选项1</label><input class="is-checkbox is-danger" id="suc2" type="checkbox" name="x_2" checked="checked"><label for="suc2">选项2</label><input class="is-checkbox is-info" id="suc3" type="checkbox" name="x_2" checked="checked"><label for="suc3">选项3</label><input class="is-checkbox is-warning" id="suc4" type="checkbox" name="x_2" checked="checked"><label for="suc4">选项4</label><input class="is-checkbox is-link" id="suc5" type="checkbox" name="x_2" checked="checked"><label for="suc5">选项5</label><input class="is-checkbox" id="suc6" type="checkbox" name="x_2" checked="checked" disabled="disabled"><label for="suc6">disabled</label></div><div class="field-bd bo p-2"><input class="is-checkbox is-success" id="suc1" type="checkbox" name="x_2" checked="checked"><label for="suc1"></label><input class="is-checkbox is-danger" id="suc2" type="checkbox" name="x_2" checked="checked"><label for="suc2"></label><input class="is-checkbox is-info" id="suc3" type="checkbox" name="x_2" checked="checked"><label for="suc3"></label><input class="is-checkbox is-warning" id="suc4" type="checkbox" name="x_2" checked="checked"><label for="suc4"></label><input class="is-checkbox is-link" id="suc5" type="checkbox" name="x_2" checked="checked"><label for="suc5"></label><input class="is-checkbox" id="suc6" type="checkbox" name="x_2" checked="checked" disabled="disabled"><label for="suc6"></label></div>

```html
<div class="field-bd">
    <input class="is-checkbox is-success" id="suc1" type="checkbox" name="x_2" checked="checked">
    <label for="suc1"></label>

    <input class="is-checkbox is-danger" id="suc2" type="checkbox" name="x_2" checked="checked">
    <label for="suc2"></label>

    <input class="is-checkbox is-info" id="suc3" type="checkbox" name="x_2" checked="checked">
    <label for="suc3"></label>

    <input class="is-checkbox is-warning" id="suc4" type="checkbox" name="x_2" checked="checked">
    <label for="suc4"></label>

    <input class="is-checkbox is-link" id="suc5" type="checkbox" name="x_2" checked="checked">
    <label for="suc5"></label>

    <input class="is-checkbox" id="suc6" type="checkbox" name="x_2" checked="checked" disabled>
    <label for="suc6">disabled</label>
</div>
```

## switch

<div class="field-bd bo p-2 mb-1"><input class="is-switch" id="com_0" type="checkbox" name=""><label for="com_0"><span class="ico" data-tip="OFF"><i>ON</i></span>描述信息</label><input class="is-switch is-success" id="com_1" type="checkbox"name="" checked="checked"><label for="com_1"><span class="ico" data-tip="已关闭"><i>已开启</i></span>描述信息</label></div>

<div class="field-bd bo p-2"><input class="is-switch is-success" id="x_xx_3" type="checkbox" name="" checked="checked"><label for="x_xx_3"><span class="ico" data-tip=""></span></label><input class="is-switch is-info" id="x_xx_4" type="checkbox" name="" checked="checked"><label for="x_xx_4"><span class="ico" data-tip=""></span></label><input class="is-switch is-danger" id="x_xx_5" type="checkbox" name="" checked="checked"><label for="x_xx_5"><span class="ico" data-tip=""></span></label><input class="is-switch is-warning" id="x_xx_6" type="checkbox" name="" checked="checked" disabled="disabled"><label for="x_xx_6"><span class="ico" data-tip=""></span></label><input class="is-switch" id="x_xx_7" type="checkbox" name="" checked="checked"><label for="x_xx_7"><span class="ico" data-tip=""></span></label></div>

```html

<div class="field-bd">
    <!-- 带文字的开关 -->
    <input class="is-switch" id="com_0" type="checkbox" name="">
    <label for="com_0">
        <span class="ico" data-tip="OFF">
            <i>ON</i>
        </span>
        描述信息
    </label>

    <input class="is-switch is-success" id="com_1" type="checkbox" name="" checked="checked">
    <label for="com_1">
        <span class="ico" data-tip="已关闭">
            <i>已开启</i>
        </span>
        描述信息
    </label>

    <!-- 开关颜色 -->
    <input class="is-switch is-primary" id="x_xx_3" type="checkbox" name="" checked="checked">
    <label for="x_xx_3">
        <span class="ico" data-tip=""></span>
    </label>
</div>
```

## file

<div class="field-bd"><input class="is-file" type="file" name="file_1" id="file_1"><label class="is-group" for="file_1"><span class="item btn is-link"><i class="icon">&#xe601;</i>点击上传...</span><span class="item btn is-default">Screen Shot 2019-07-29 at 15.54.25.png</span></label></div>

```html
<div class="field-bd">
    <input class="is-file" type="file" name="file_1" id="file_1">
    <label class="is-group" for="file_1">
        <span class="item btn is-link">
            <i class="icon">&#xe601;</i> 点击上传...
        </span>
        <span class="item btn is-default">
            Screen Shot 2019-07-29 at 15.54.25.png
        </span>
    </label>
</div>
```
结合`is-boxed`制作更多样式的文件框

<div class="field-bd"><input class="is-file" type="file" name="file_1" id="file_1"><label class="is-boxed" for="file_1"><span class="item btn is-info box-hd"><i class="icon">&#xe600;</i>点击下载</span></label><input class="is-file" type="file" name="file_1" id="file_1" disabled><label class="is-boxed" for="file_1"><span class="item btn is-light box-hd"><i class="icon">&#xe601;</i>点击上传...</span></label></div>

```html
<div class="field-bd">
    <input class="is-file" type="file" name="file_1" id="file_1">
    <label class="is-boxed" for="file_1">
        <span class="item btn is-info box-hd">
            <i class="icon">&#xe600;</i>点击下载
        </span>
    </label>
    <input class="is-file" type="file" name="file_1" id="file_1" disabled>
    <label class="is-boxed" for="file_1">
        <span class="item btn is-light box-hd">
            <i class="icon">&#xe601;</i>点击上传...
        </span>
    </label>
</div>
```
更多样式:可定制尺寸、背景
<div class="field-bd"><input class="is-file" type="file" name="file_1" id="file_1"><label class="is-boxed" for="file_1"><span class="item btn is-warning box-hd" style="height:160px"><i class="icon ico-upload">&#xe601;</i>点击上传...</span><span class="item btn is-default">Screen Shot 2019-07-29 at 15.54.25.png</span></label><input class="is-file is-pic-file" type="file" name="facePic" id="facePic"><label class="is-boxed" for="facePic"><span class="item btn box-hd is-mask" id="showPic" style="background-image: url(assets/images/img3.jpg);height:160px"><i class="icon ico-upload">&#xe601;</i>点击上传...</span><span class="item btn is-default">Screen Shot 2019-07-29 at 15.54.25.png</span></label></div>

```html
<div class="field-bd">
    <input class="is-file is-pic-file" type="file" name="facePic" id="facePic">
    <label class="is-boxed" for="facePic">
        <!-- 通过is-mask和背景图制作遮罩的效果 -->
        <span class="item btn box-hd is-mask" id="showPic" style="background-image: url(assets/images/ss1.jpg);height:160px">
            <i class="icon ico-upload">&#xe601;</i>点击上传...
        </span>
        <span class="item btn is-default">
            Screen Shot 2019-07-29 at 15.54.25.png
        </span>
    </label>
</div>
```
## 普通排版

<form method="get" class="bo p-3"><div class="field"><label class="x-label" for="f1">普通</label><div class="field-bd"><div class="has-tip"><input type="text" class="form-item" name="" id="f1" placeholder="提示文字"> <small class="form-text">显示这里的文字上层嵌套一层`.has-tip`即可</small></div></div></div><hr><div class="field"><label class="x-label" for="f1">group普通</label><div class="field-bd is-group"><label class="item in-label">性别</label><input class="item form-item w-auto" type="text" name="" id="f1"> <button class="item btn is-primary" type="button">提交</button></div></div><div class="field"><label class="x-label" for="f1">group全屏</label><div class="field-bd is-group"><input class="item form-item" type="text" name="" id="f1"> <button class="item btn is-info" type="button">提交</button></div></div><hr><div class="field"><label class="x-label" for="f1">内联</label><div class="field-bd"><div class="d-flex"><input type="text" class="form-item" name="" id=""><label class="the-label">走起来</label><div class="has-tip"><input type="text" class="form-item" name="" id="f1"> <small class="form-text">显示这里的文字上层嵌套一层`.has-tip`即可</small></div></div></div></div><hr><div class="field"><label class="x-label" for="f1">禁用</label><div class="field-bd"><input type="text" class="form-item w-100" name="" id="" value="bme@qq.com" disabled="disabled"></div></div><hr><div class="field"><label class="x-label">下拉菜单</label><div class="field-bd"><div class="select is-fullwidth"><select class="form-item"><option>Business development</option><option>Marketing</option><option>Sales</option></select></div></div></div><hr><div class="field"><label class="x-label">内联单选</label><div class="field-bd"><input class="is-radio" type="radio" name="x_1" id="x_1_1" checked="checked"><label for="x_1_1">Yes</label><input class="is-radio" type="radio" name="x_1" id="x_1_2"><label for="x_1_2">No</label><input class="is-radio" type="radio" name="x_1" id="x_1_3" disabled="disabled"><label for="x_1_3">disabled</label></div></div><div class="field"><label class="x-label">内联多选</label><div class="field-bd"><input class="is-checkbox" id="x_2_1" type="checkbox" name="x_2" checked="checked"><label for="x_2_1">op1</label><input class="is-checkbox" id="x_2_2" type="checkbox" name="x_2"><label for="x_2_2">op2</label><input class="is-checkbox" id="x_2_3" type="checkbox" name="x_2" checked="checked" disabled="disabled"><label for="x_2_3">checkbox</label></div></div><hr><div class="field"><label class="x-label">上传</label><div class="field-bd"><input class="is-file" type="file" name="file_1" id="file_1"><label class="is-group" for="file_1"><span class="item btn is-link"><i class="icon">&#xe601;</i> 点击上传...</span> <span class="item btn is-default">Screen Shot 2019-07-29 at 15.54.25.png</span></label></div></div><hr><div class="field"><label class="x-label">文本域</label><div class="field-bd"><textarea class="form-item" placeholder="Explain how we can form-text you"></textarea></div></div><div class="field"><label class="x-label"></label><div class="field-bd"><button class="btn is-primary">Send message</button></div></div></form>

```html
<form method="get" class="">
    <div class="field">
        <label class="" for="f1">说明</label>
        <div class="field-bd">
            <!-- code... -->
        </div>
    </div>
</form>
```

## 内联排版:x-form

<form method="get" class="x-form bo p-3"><div class="field"><label class="x-label" for="f1">普通</label><div class="field-bd"><div class="has-tip"><input type="text" class="form-item" name="" id="f1" placeholder="提示文字"> <small class="form-text">显示这里的文字上层嵌套一层`.has-tip`即可</small></div></div></div><hr><div class="field"><label class="x-label" for="f1">group普通</label><div class="field-bd is-group"><label class="item in-label">性别</label><input class="item form-item w-auto" type="text" name="" id="f1"> <button class="item btn is-primary" type="button">提交</button></div></div><div class="field"><label class="x-label" for="f1">group全屏</label><div class="field-bd is-group"><input class="item form-item" type="text" name="" id="f1"> <button class="item btn is-info" type="button">提交</button></div></div><hr><div class="field"><label class="x-label" for="f1">内联</label><div class="field-bd"><div class="d-flex"><input type="text" class="form-item" name="" id=""><label class="the-label">走起来</label><div class="has-tip"><input type="text" class="form-item" name="" id="f1"> <small class="form-text">显示这里的文字上层嵌套一层`.has-tip`即可</small></div></div></div></div><hr><div class="field"><label class="x-label" for="f1">禁用</label><div class="field-bd"><input type="text" class="form-item w-100" name="" id="" value="bme@qq.com" disabled="disabled"></div></div><hr><div class="field"><label class="x-label">下拉菜单</label><div class="field-bd"><div class="select is-fullwidth"><select class="form-item"><option>Business development</option><option>Marketing</option><option>Sales</option></select></div></div></div><hr><div class="field"><label class="x-label">内联单选</label><div class="field-bd"><input class="is-radio" type="radio" name="x_1" id="x_1_1" checked="checked"><label for="x_1_1">Yes</label><input class="is-radio" type="radio" name="x_1" id="x_1_2"><label for="x_1_2">No</label><input class="is-radio" type="radio" name="x_1" id="x_1_3" disabled="disabled"><label for="x_1_3">disabled</label></div></div><div class="field"><label class="x-label">内联多选</label><div class="field-bd"><input class="is-checkbox" id="x_2_1" type="checkbox" name="x_2" checked="checked"><label for="x_2_1">op1</label><input class="is-checkbox" id="x_2_2" type="checkbox" name="x_2"><label for="x_2_2">op2</label><input class="is-checkbox" id="x_2_3" type="checkbox" name="x_2" checked="checked" disabled="disabled"><label for="x_2_3">checkbox</label></div></div><hr><div class="field"><label class="x-label">上传</label><div class="field-bd"><input class="is-file" type="file" name="file_1" id="file_1"><label class="is-group" for="file_1"><span class="item btn is-link"><i class="icon">&#xe601;</i> 点击上传...</span> <span class="item btn is-default">Screen Shot 2019-07-29 at 15.54.25.png</span></label></div></div><hr><div class="field"><label class="x-label">文本域</label><div class="field-bd"><textarea class="form-item" placeholder="Explain how we can form-text you"></textarea></div></div><div class="field"><label class="x-label"></label><div class="field-bd"><button class="btn is-primary">Send message</button></div></div></form>

```html
<form method="get" class="x-form">
    <div class="field">
        <label class="x-label" for="f1">说明</label>
        <div class="field-bd">
            <!-- code... -->
        </div>
    </div>
</form>
```

## 内联排版:in-form

<form method="post" class="in-form bo p-3"><div class="field is-group"><div class="is-group"><label class="item in-label" for="">普通</label><input class="item form-item is-auto" type="text" name="" placeholder="提示文字"></div><small class="form-text flex-1-0-auto">Do not enter the first zero</small></div><hr><div class="field is-group"><label class="item in-label" for="">group普通</label><input class="item form-item w-auto" type="text" name=""> <button class="item btn is-primary" type="button">提交</button></div><div class="field is-group"><label class="item in-label" for="">group全屏</label><input class="item form-item" type="text" name=""> <button class="item btn is-info" type="button">提交</button></div><hr><div class="field"><div class="is-group"><label class="item in-label" for="">group1</label><input type="text" class="item form-item" name=""></div><div class="is-group"><label class="item in-label" for="">group2</label><input type="text" class="item form-item" name=""></div></div><div class="field"><div class="is-group"><label class="item in-label" for="">label1</label><input type="text" class="item form-item" name=""><label class="item in-label" for="">label2</label><input type="date" class="item form-item" name=""></div></div><hr><div class="field is-group select"><label class="item in-label">下拉菜单</label><select class="item form-item"><option>Business development</option><option>Marketing</option><option>Sales</option></select></div><hr><div class="field is-group"><label class="item in-label">内联单选</label><div class="item form-item"><input class="is-radio" type="radio" name="a_1" id="a_1_1" checked="checked"><label for="a_1_1">Yes</label><input class="is-radio" type="radio" name="a_1" id="a_1_2"><label for="a_1_2">No</label><input class="is-radio" type="radio" name="a_1" id="a_1_3" disabled="disabled"><label for="a_1_3">disabled</label></div></div><div class="field is-group"><label class="item in-label">内联多选</label><div class="item form-item"><input class="is-checkbox" id="b_2_1" type="checkbox" name="b_2" checked="checked"><label for="b_2_1">op1</label><input class="is-checkbox" id="b_2_2" type="checkbox" name="b_2"><label for="b_2_2">op2</label><input class="is-checkbox" id="b_2_3" type="checkbox" name="b_2" checked="checked" disabled="disabled"><label for="x_2_3">checkbox</label></div></div><hr><div class="field is-group"><label class="item in-label">开关</label><div class="item form-item"><input class="is-switch is-success" id="t3_1" type="checkbox" name="" checked="checked"><label for="t3_1"><span class="ico" data-tip="已关闭"><i>已开启</i></span> 评论审核</label></div></div><hr><div class="field"><div class="field-bd"><input class="is-file" type="file" name="file-d1" id="file-d1"><label class="is-group" for="file-d1"><span class="item btn is-link"><i class="icon">&#xe601;</i> 点击上传...</span> <span class="item btn is-default">Screen Shot 2019-07-29 at 15.54.25.png</span></label></div></div><hr><div class="field"><textarea class="form-item" placeholder="Explain how we can form-text you"></textarea></div><div class="field"><button class="btn is-primary">Send message</button></div></form>


```html
<form method="post" class="in-form">
    <div class="field is-group">
        <label class="item in-label" for="">说明</label>
        <input class="item form-item" type="text" name="" placeholder="提示文字">
    </div>
</form>
```


```html

```


```html

```