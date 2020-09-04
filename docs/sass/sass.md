# Sass

## sass语法表

## 颜色函数

| 函数名称                          | 说明      |
|-------------------------------|---------|
| color: lighten\(\#000, 85%\); | 减淡颜色    |
| color:darken\(\#fff, 10%\)    | 加深颜色    |
| saturate\($color, $amount\)   | 增加颜色饱和度 |
| desaturate\($color, $amount\) | 降低颜色饱和度 |
| grayscale\($color\)           | 灰度颜色    |

## 运算符

`not(var) | and | or | == | != | < | > | <= | =>`

## 数学函数

| 函数                     | 描述 & 实例                                                            |
|------------------------|--------------------------------------------------------------------|
| abs(number)            | 返回一个数值的绝对值。    实例:abs(15) 结果: 15、abs(-15) 结果: 15                   |
| ceil(number)           | 向上取整。    实例:ceil(15.20) 结果: 16                                     |
| comparable(num1, num2) | 返回一个布尔值，判断 num1 与 num2 是否可以进行比较。实例:comparable(35px, 2em) 结果: false |
| floor(number)          | 向下取整。实例: floor(15.80) 结果: 15                                       |
| max(number)            | 返回最大值。实例:max(5, 7, 9, 0, -3, -7) 结果: 9                             |
| min(number)            | 返回最小值。实例:min(5, 7, 9, 0, -3, -7) 结果: -3                            |
| percentage(number)     | 将数字转化为百分比的表达形式。实例:percentage(1.2) 结果: 120                          |
| random()               | 返回 0-1 区间内的随机小数。实例:random() 结果: 0.45673                            |
| random(number)         | 返回 1 至 number 之间的随机整数，包括 1 和 limit。实例:random(6) 结果: 5              |
| round(number)          | 返回最接近该数的一个整数，四舍五入。实例:round(15.20) 结果: 15、round(15.80) 结果: 16       |

## 字符串函数

| 函数                                | 描述 & 实例                                                                                                |
|-----------------------------------|--------------------------------------------------------------------------------------------------------|
| quote(string)                     | 给字符串添加引号。 实例:quote(runoob) 结果: "runoob"                                                                |
| str-index(string, substring)      | 返回 substring 子字符串第一次在 string 中出现的位置。如果没有匹配到子字符串，则返回 null。                                              |
| str-insert(string, insert, index) | 在字符串 string 中  index 位置插入 insert。实例:str-insert("Hello world!", " runoob", 6) 结果: "Hello runoob world!" |
| str-length(string)                | 返回字符串的长度。实例:str-length("runoob") 结果: 6                                                                 |
| str-slice(string, start, end)     | 从 string 中截取子字符串，通过  start-at 和 end-at 设置始末位置，未指定结束索引值则默认截取到字符串末尾。                                     |
| to-lower-case(string)             | 将字符串转成小写    实例:to-lower-case("RUNOOB") 结果: "runoob"                                                    |
| to-upper-case(string)             | 将字符串转成大写    实例:to-upper-case("runoob") 结果: "RUNOOB"                                                    |
| unique-id()                       | 返回一个无引号的随机字符串作为 id。不过也只能保证在单次的 Sass 编译中确保这个 id 的唯一性。实例:unique-id() Result:     uad053b1c   |
| unquote(string)                   | 移除字符串的引号。实例:unquote("runoob") 结果: runoob                                                               |

## map函数

| 函数                       | 描述 & 实例                                           |
|--------------------------|---------------------------------------------------|
| map-get(map, key)        | 返回 Map 中 key 所对应的 value(值)。如没有对应的 key，则返回 null 值。 |
| map-has-key(map, key)    | 判断 map 是否有对应的 key，存在返回 true，否则返回 false。           |
| map-keys(map)            | 返回 map 中所有的 key 组成的队列。                            |
| map-values(map)          | 返回 map 中所有的 value 并生成一个队列。                        |
| map-merge(map1, map2)    | 合并两个 map 形成一个新的 map 类型，即将 map2 添加到 map1的尾部。       |
| map-remove(map, keys...) | 移除 map 中的 keys，多个 key 使用逗号隔开。                     |

map语法：

```scss
$map: (
    key1: value1,
    key2: (
        key-1: value-1,
        key-2: value-2,
    ),
    key3: value3
);
```

## 检查函数

Sass`Introspection`函数比较少用于构建样式表，一般用于代码的调试上。  
下表列出了 Sass 的 Introspection 函数：

| 函数                                     | 描述 & 实例                                                                                                 |
|----------------------------------------|---------------------------------------------------------------------------------------------------------|
| call(function, arguments...)           | 函数的动态调用，即调用函数 function 参数为 arguments，并返回结果。                                                             |
| content-exists()                       | 查看当前的混入是否传递 @content 块。                                                                                 |
| feature-exists(feature)                | 检查当前的 Sass 实现是否支持该特性。实例:feature-exists("at-error"); 结果: true                                            |
| function-exists(functionname)          | 检测指定的函数是否存在。实例:function-exists("nonsense") 结果: false                                                    |
| get-function(functionname, css: false) | 返回指定函数。如果 css 为 true，则返回纯 CSS 函数。                                                                       |
| global-variable-exists(variablename)   | 检测某个全局变量是否定义。实例:variable-exists(a) 结果: true                                                             |
| inspect(value)                         | 返回一个字符串的表示形式，value 是一个 sass 表达式。                                                                        |
| mixin-exists(mixinname)                | 检测指定混入 (mixinname) 是否存在。 实例:mixin-exists("important-text") 结果: true                                     |
| type-of(value)                         | 返回值类型。返回值可以是 number, string, color, list,map, bool, null, function, arglist。实例:type-of(15px) 结果: number |
| unit(number)                           | 返回传入数字的单位（或复合单位）。实例:unit(15px)结果: px                                                                    |
| unitless(number)                       | 返回一个布尔值，判断传入的数字是否带有单位。实例:unitless(15px) 结果: false                                                       |
| variable-exists(variablename)          | 判断变量是否在当前的作用域下。实例:variable-exists(b) 结果: true                                                           |

## mixin混合

```scss
// 一个简单的mixin
@mixin demo1 {
  color: red;
  font-size: 25px;
  font-weight: bold;
}

// 带参数的mixin ----------------------------------------------
@mixin demo2($border,$width) {
  color: red;
  width: $width;
  border: $border solid blue;
}

// mixin可以再调用其它mixin ----------------------------------
@mixin demo3 {
  font-weight:700;
  @include demo1;
}
// -------------------------------------------------------------
// 有时，不能确定一个混入（mixin）或者一个函数（function）使用多少个参数，这时我们就可以使用 ... 来设置可变参数。
@mixin box-shadow($shadows...) {
      -moz-box-shadow: $shadows;
      -webkit-box-shadow: $shadows;
      box-shadow: $shadows;
}

.shadows {
  @include box-shadow(0px 4px 5px #666, 2px 6px 10px #999);
}
// 生成的css是
.shadows {
  -moz-box-shadow: 0px 4px 5px #666, 2px 6px 10px #999;
  -webkit-box-shadow: 0px 4px 5px #666, 2px 6px 10px #999;
  box-shadow: 0px 4px 5px #666, 2px 6px 10px #999;
}
```

调用mixin：

```scss
.hello {
  @include demo2(1px,200px);
}
```

## extend继承

`@extend` 指令告诉 Sass 一个选择器的样式从另一选择器继承。  
如果一个样式与另外一个样式几乎相同，只有少量的区别，则使用`@extend` 就显得很有用。

```scss
.btn-1  {
  border: none;
  font-size: 16px;
  cursor: pointer;
}

.btn-2  {
  @extend .btn-1;
  background-color: red;
}

.btn-3  {
  @extend .btn-1;
  background-color: green;
  color: white;
}
```

生成的css是：

```css
.btn-1,.btn-2,.btn-3  {
  border: none;
  font-size: 16px;
  cursor: pointer;
}

.btn-2  {
  background-color: red;
}

.btn-3  {
  background-color: green;
  color: white;
}
```

如果不想继承的主体输出，可以使用`%`（占位符）

```scss
%btn-1  {
  border: none;
  font-size: 16px;
  cursor: pointer;
}

.btn-2  {
  @extend %btn-1;
  background-color: red;
}

.btn-3  {
  @extend %btn-1;
  background-color: green;
  color: white;
}
```

生成的css是这样的：

```css
.btn-2,.btn-3  {
  border: none;
  font-size: 16px;
  cursor: pointer;
}

.btn-2  {
  background-color: red;
}

.btn-3  {
  background-color: green;
  color: white;
}
```

## map遍历

```scss
// map地图
/*
语法：
$map: (
    key1: value1,
    key2: (
        key-1: value-1,
        key-2: value-2,
    ),
    key3: value3
);
*/

$theme-colors: (
  "primary":    #0d6efd,
  "secondary":  #6f42c1,
  "success":    #28a745,
  "light":      #f8f9fa
) !default;

// 遍历map地图：$theme-colors
@each $key,$var in $theme-colors {
    // 判断排除掉key是"light"的项
    @if ($key != "light") {
        // 批量生成css
        .sbg-#{$key}{
            background:lighten($var,35%);
        }
    }
}
```

生成的css：

```css
.sbg-primary {
  background: #bed8fe;
}

.sbg-secondary {
  background: #d5c8ed;
}

.sbg-success {
  background: #9be7ac;
}
```

## 自定义实用工具

传送到[自定义实用工具文档](/bootstrap5/diy-utilities.md)
