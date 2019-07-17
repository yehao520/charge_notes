JavaScript显示方案：

- `alert()`写入警告框
- `document.write()`写入HTML输出
- `innerHTML`写入HTML元素
- `console.log()`写入浏览器控制台

关键字：

`break, continue, debugger, do...while, for, function, if...else, return, switch, try...catch, var`

`null`和`undefine`的区别：值相等、类型不一样。

常见的HTML事件：

|     事件      |         描述         |
| :-----------: | :------------------: |
|  `onchange`   |   HTML元素已被改变   |
|   `onclick`   |   用户点击HTML元素   |
| `onmouseover` | 鼠标移动到HTNL元素上 |
| `onmouseiut`  |   鼠标移开HTML元素   |
|  `onkeydown`  |     按下键盘按键     |
|   `onload`    |    浏览器完成加载    |

字符串属性和方法：

`str.length`: 返回字符串长度

`str.constructor`: 对创建该对象的函数的引用

`str.protoype`: 允许向对象添加属性和方法



`str.indexOf('xs')`: 返回指定文本在字符串中出现的位置，未找到返回-1

`str.lastIndexOf('xs')`: 返回指定文本在字符串中最后一次出现的索引，未找到返回-1

`str.search('xs')`: 搜索指定的字符串并返回匹配的位置

`str.slice(start, end)`: 字符串切片，接受负索引

`str.substring()`：类似`slice()`但不接受负索引

`str.substr()`: 类似`slice()`但第二个参数为被提取部分的长度

`str.replace()`: 用一个值替换字符串中匹配到的第一个指定的值

`str.toUpperCase()`: 将字符串装换为大写

`str.toLowerCase()`:将字符串装换为小写

`str.concat()`: 连接两个或多个字符串

`str.trim()`: 删除字符串两端的空白符

`str.charAt()`: 返回字符串中指定下标的字符

`str.charCodeAt()`: 返回指定索引字符的unicode编码

`str.split(symbol)`: 字符串切割



Number方法和属性：

`num.toString()`: 以字符串返回数值

`num.toExponential()`: 返回字符串值，参数定义小数点后的字符数

`num.toFixed()`: 返回字符串值，包含指定位数小数的数字

`num.toPrecision()`: 返回字符串值，包含指定长度的数字

`num.valueOf()`: 以数值返回数值



全局JavaScript方法:

`Number()`: 返回数字

`parseFloat()`: 解析参数并返回浮点数

`parseInt()`: 解析参数并返回整数



数组：创建数组时避免使用`new Array`，推荐`[]`

数组方法：

`arr.join()`:使用参数将`arr`中的元素连接起来

`arr.pop()`: 删除数组中的最后一个元素，返回删除的元素

`arr.push(x)`: 将`x`添加到数组末尾，返回数值长度

`arr.shift()`: 删除首个数组元素， 返回被删除的元素

`arr.unshift(x)`: 向数组首部插入`x`元素，返回数组的长度

`arr.splice(index, howmany, items)`: 向数组指定位置删除多少个元素并添加多个元素

`arr1.concat(arr2)`: 合并数组

`arr.slice(start, end)`: 切片数组

`arr.sort()`: 数组排序

`arr.reverse()`: 反转数组

数组迭代：`forEach()`、`for(var i = 0; i < arr.length; i++)`、`for(let x in arr)` 

```js
/* 控制台打印出数组中的每个元素 */
var numbers = [1, 2, 3, 4, 5];
numbers.forEach(function(value) {
    console.log(value);
});
```

```js
/* 控制台打印出数组中的每个元素 */
var numbers = [1, 2, 3, 4, 5];
for (let index in numbers) {
    console.log(numbers[index]);
};
```

`Array.map()`：

- 对每个数组元素执行函数来创建新的数组
- 不会对没有值的数组元素执行函数
- 不会更改原始数组

```js
/* 数组每个元素乘以2 */
var numbers1 = [1, 2, 3, 4, 5];
var numbers2 = numbers1.map(function(value) {
    return value * 2;
});
```

`Array.filter()`：

- 创建一个包含通过测试的数组元素的新数组

```js
/* 筛选出值大于2的元素并创建新的数组 */
var numbers1 = [1, 2, 3, 4, 5];
var numbers2 = numbers1.filter(function(value) {
    return value > 2;
});
```

`Array.reduce()`：

- 在每个数组元素上运行函数，用户生成（减少）单个值
- 在数组中从左到右执行
- 不会减少原始数组

```js
/* 计算总和 */
var numbers1 = [1, 2, 3, 4, 5];
var sum = numbers1.reduce(function (total, value) {
    return total + value;
})
```

`Array.reduceRight()`：

`Array.every()`：

- 检查数组所有元素是否通过测试

```js
/* 检查数组中所有元素是否大于0 */
var numbers1 = [1, 2, 3, 4, 5];
var sum = numbers1.every(function (value) {
    return value > 0;
})
```

`Array.some()`：

- 检查数组某些元素是否通过测试

```js
/* 检查数组中所有元素是否大于0 */
var numbers1 = [1, 2, 3, 4, 5];
var sum = numbers1.some(function (value) {
    return value > 0;
})
```

日期：

四种方法创建Date对象：

- `new Date()`
- `new Date(year, month, day, hours, minutes, seconds, milliseconds)`
- `new Date(milliseconds)`
- `new Date(data string)`

日期格式：

|   类型   |              实例               |
| :------: | :-----------------------------: |
| ISO日期  |          "2019-07-16"           |
|  短日期  | "07/16/20119" 或者"2019/07/16"  |
|  长日期  | "Jul 16 2019" 或者"16 Jul 2019" |
| 完整日期 |     "Tuesday July 16 2019"      |

日期获取方法：

`getData()`: 以数值返回天(1-31)

`getDay()`: 以数值返回周名(0-6)

`getFullYear()`: 获取四位的年(yyyy)

`getHours()`: 获取小时(0-23)

`getMilliseconds()`: 获取毫秒(0-999)

`getMinutes()`: 获取分(0-59)

`getMonth()`: 获取月(0-11)

`getSeconds()`: 获取秒(0-59)

`getTime()`: 获取时间(从 1970 年 1 月 1 日至今)

日期设置方法：

`setDate()`: 以数值(1-31)设置日

`setFullYear()`: 设置年(可选月和日)

`setHour()`: 设置小时(0-23)

`setMilliseconds()`: 设置毫秒(0-999)

`setMinutes()`: 设置分(0-59)

`setMonth()`: 设置月(0-11)

`setSeconds()`: 设置秒(0-59)

`setTime()`: 设置时间(从 1970 年 1 月 1 日至今的毫秒数)



Math对象：

`Math.round(x)`:返回`x`四舍五入的整数值

`Math.pow(x, y)`: 返回`x`的`y`次幂

`Math.sqrt(x)`: 返回`x`的平方

`Math.abs(x)`: 返回`x`的绝对值 

`Math.ceil(x)`: 返回`x`向上取整的值

`Math.floor(x)`: 返回`x`向下取整的值

`Math.min()`: 返回参数列表中的最小值

`Math.max()`: 返回参数列表中的最大值

`Matn.random()`: 返回[0,1)的随机数



JavaScript最佳实践：

- 避免全局变量
- 始终声明局部变量
- 把所有声明放在每段脚本或函数的顶部
- 初始化变量
- 使用`===`比较
- 避免使用`eval()`
- 不要声明数值、字符串或布尔对象
- 请勿使用`new Object()`
  - 使用`{}`代替`new Objects()`
  - 使用`""`代替`new String()`
  - 使用`0`来代替`new Number()`
  - 使用`false`来代替`new Boolean()`
  - 使用`[]`来代替`new Array()`
  - 使用`/()/`来代替`new RegExp()`
  - 使用`function(){}`来代替`new Function()`