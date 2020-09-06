# 表格

## 条纹表格
表格添加class名`is-striped`即可！
<table class="is-striped"><thead><tr><th>#</th><th>标题1</th><th>标题2</th><th>标题3</th></tr></thead><tbody><tr><td>1</td><td>td内容</td><td>td内容</td><td>td内容</td></tr><tr><td>2</td><td>td内容</td><td>td内容</td><td>td内容</td></tr><tr><td>3</td><td>td内容</td><td>td内容</td><td>td内容</td></tr></tbody></table>

```html
<table class="is-striped">
    <thead>
    <tr>
        <th>#</th>
        <th>标题1</th>
        <th>标题2</th>
        <th>标题3</th>
    </tr>
    </thead>
    <tbody>
    <tr>
        <td>id</td>
        <td>td内容</td>
        <td>td内容</td>
        <td>td内容</td>
    </tr>
    </tbody>
</table>
```

## 悬停表格
表格添加class名`is-hovered`即可！
<table class="is-hovered"><thead><tr><th>#</th><th>标题1</th><th>标题2</th><th>标题3</th></tr></thead><tbody><tr><td>1</td><td>td内容</td><td>td内容</td><td>td内容</td></tr><tr><td>2</td><td>td内容</td><td>td内容</td><td>td内容</td></tr><tr><td>3</td><td>td内容</td><td>td内容</td><td>td内容</td></tr></tbody></table>

```html
<table class="is-hovered">
    ...
</table>
```

## 边框表格
表格添加class名`is-bordered`即可！
<table class="is-bordered"><thead><tr><th>#</th><th>标题1</th><th>标题2</th><th>标题3</th></tr></thead><tbody><tr><td>1</td><td>td内容</td><td>td内容</td><td>td内容</td></tr><tr><td>2</td><td>td内容</td><td>td内容</td><td>td内容</td></tr><tr><td>3</td><td>td内容</td><td>td内容</td><td>td内容</td></tr></tbody></table>

```html
<table class="is-bordered">
    ...
</table>
```

## 数据表格
表格添加class名`is-data`即可！

<table class="is-hovered is-data"><thead><tr><th width="40"><input class="is-checkbox no-border"id="cc"type="checkbox"name="Checkbox3"><label for="cc"></label></th><th>昵称</th><th>邮箱</th><th>电话</th><th>权限</th><th>操作</th></tr></thead><tbody class=""><tr><th scope="row"><input class="is-checkbox no-border"id="cc1"type="checkbox"name="Checkbox3"><label for="cc1"></label></th><td><div class="flex-y-c"><div class="is-up mr-2"><span class="dot dot-lt"></span><img class="avatar o"src="assets/images/face1.jpg"alt=""></div>Constance Satterfield</div></td><td>bme@qq.com</td><td>123456789</td><td><span class="tag is-primary oo">管理员</span></td><td><button class="btn-space"type="button"><i class="icon icon-edit-m"></i></button><button class="btn-space"type="button"><i class="icon icon-delete-m"></i></button></td></tr><tr><th scope="row"><input class="is-checkbox no-border"id="cc1"type="checkbox"name="Checkbox3"><label for="cc1"></label></th><td><div class="flex-y-c"><div class="is-up mr-2"><span class="dot dot-lt"></span><img class="avatar o"src="assets/images/face2.jpg"alt=""></div>Constance Satterfield</div></td><td>bme@qq.com</td><td>123456789</td><td><span class="tag is-secondary oo">编辑</span></td><td><button class="btn-space"type="button"><i class="icon icon-edit-m"></i></button><button class="btn-space"type="button"><i class="icon icon-delete-m"></i></button></td></tr><tr><th scope="row"><input class="is-checkbox no-border"id="cc1"type="checkbox"name="Checkbox3"><label for="cc1"></label></th><td><div class="flex-y-c"><div class="is-up mr-2"><span class="dot dot-lt"></span><img class="avatar o"src="assets/images/face3.jpg"alt=""></div>Constance Satterfield</div></td><td>bme@qq.com</td><td>123456789</td><td><span class="tag is-danger oo">作者</span></td><td><button class="btn-space"type="button"><i class="icon icon-edit-m"></i></button><button class="btn-space"type="button"><i class="icon icon-delete-m"></i></button></td></tr><tr><th scope="row"><input class="is-checkbox no-border"id="cc1"type="checkbox"name="Checkbox3"><label for="cc1"></label></th><td><input class="form-item is-sm"type="text"name=""value="我是input 可以点击"></td><td><input class="form-item is-sm"type="text"name=""value="我是input 可以点击"></td><td><input class="form-item is-sm"type="text"name=""value="我是input 可以点击"></td><td>-</td><td>-</td></tr></tbody></table>

```html
<table class="is-data">
    ...
</table>
```

## 表格大小

总共三种表格尺寸：

### 大尺寸表格
`is-lg`
<table class="is-bordered is-lg"><thead><tr><th>#</th><th>标题1</th><th>标题2</th><th>标题3</th></tr></thead><tbody><tr><td>1</td><td>td内容</td><td>td内容</td><td>td内容</td></tr><tr><td>2</td><td>td内容</td><td>td内容</td><td>td内容</td></tr><tr><td>3</td><td>td内容</td><td>td内容</td><td>td内容</td></tr></tbody></table>

### 中尺寸表格
<table class="is-bordered"><thead><tr><th>#</th><th>标题1</th><th>标题2</th><th>标题3</th></tr></thead><tbody><tr><td>1</td><td>td内容</td><td>td内容</td><td>td内容</td></tr><tr><td>2</td><td>td内容</td><td>td内容</td><td>td内容</td></tr><tr><td>3</td><td>td内容</td><td>td内容</td><td>td内容</td></tr></tbody></table>

### 小尺寸表格
`is-sm`
<table class="is-bordered is-sm"><thead><tr><th>#</th><th>标题1</th><th>标题2</th><th>标题3</th></tr></thead><tbody><tr><td>1</td><td>td内容</td><td>td内容</td><td>td内容</td></tr><tr><td>2</td><td>td内容</td><td>td内容</td><td>td内容</td></tr><tr><td>3</td><td>td内容</td><td>td内容</td><td>td内容</td></tr></tbody></table>