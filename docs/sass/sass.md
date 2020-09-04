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

`not(var)、and、or、==、!=、<、>`

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

## map函数

| 函数                       | 描述 & 实例                                           |
|--------------------------|---------------------------------------------------|
| map-get(map, key)        | 返回 Map 中 key 所对应的 value(值)。如没有对应的 key，则返回 null 值。 |
| map-has-key(map, key)    | 判断 map 是否有对应的 key，存在返回 true，否则返回 false。           |
| map-keys(map)            | 返回 map 中所有的 key 组成的队列。                            |
| map-values(map)          | 返回 map 中所有的 value 并生成一个队列。                        |
| map-merge(map1, map2)    | 合并两个 map 形成一个新的 map 类型，即将 map2 添加到 map1的尾部。       |
| map-remove(map, keys...) | 移除 map 中的 keys，多个 key 使用逗号隔开。                     |

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
