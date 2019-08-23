# 1. HTML

## 1.1 设置整体链接的打开状态

base可以设置整体链接的打开状态

```html
<head>
		<meta charset="UTF-8">
		<title>13 base标签</title>
		<base target="_blank" />
</head>
```

## 1.2 定义选项列表

datalist 标签定义选项列表，与input标签配合使用

```html
<input type="text" list="star" value="输入明星" /> <!--input 里面用 list-->
<datalist id="star">  <!--datalist 里面用 id 来实现和 input 链接-->
	<option>刘德华</option>
	<option>刘若英</option>
	<option>刘晓庆</option>
	<option>郭富城</option>
	<option>张学友</option>
</datalist>
```

## 1.3 表单分组

fieldset 元素可将表单内的相关元素分组，打包

```html
<fieldset>
			<legend>用户登录</legend>  标题
			用户名：<input type="text" /><br /> 
			密&nbsp;码：<input type="password" />
</fieldset>
```

## 1.4 input相关

### 1.4.1 最多字符数（maxlength）

```html
<input type="password" name="pass" maxlength="6">
```



### 1.4.2 自动记录input标签输入内容（autocomplete）

- 使用要求

  - 需要提交按钮

  - 表单必须有名字

    ```html
    <form action="">
        姓名：<input type="text" autocomplete name="userName">
        <input type="submit" />
    </form>
    ```

### 1.4.3 新增的input type属性值

| 类型     | 使用示例                | 含义                 |
| -------- | ----------------------- | -------------------- |
| email    | <input type="email">    | 输入邮箱格式         |
| tel      | <input type="tel">      | 输入手机号码格式     |
| url      | <input type="url">      | 输入url格式          |
| number   | <input type="number">   | 输入数字格式         |
| search   | <input type="search">   | 搜索框（体现语义化） |
| range    | <input type="range">    | 自由拖动滑块         |
| time     | <input type="time">     | 小时分钟             |
| date     | <input type="date">     | 年月日               |
| datetime | <input type="datetime"> | 时间                 |
| month    | <input type="month">    | 年月                 |
| week     | <input tyoe="week">     | 年 星期              |
| color    | <input type="color">    | 颜色                 |

### 1.4.4 常用新属性

| 属性         | 用法                                                         | 含义                                                         |
| ------------ | ------------------------------------------------------------ | ------------------------------------------------------------ |
| placeholder  | <input type="text" placeholder="请输入用户名">               | 占位符提供可描述输入字段预期值的提示信息                     |
| autofocus    | <input type="text" autofocus>                                | 规定当页面加载时 input 元素应该自动获得焦点                  |
| multiple     | <input type="file" multiple>                                 | 多文件上传                                                   |
| accept       | <input type="file" accept=".jpg,.png" ><br /><input type="file" accept="image/*" > | 规定上传的文件类型                                           |
| autocomplete | <input type="text" autocomplete>                             | 规定表单是否应该启用自动完成功能 有两个值，一个是on，一个是off，on代表记录已经输入的值 |
| required     | <input type="text" required>                                 | 必填项                                                       |
| accesskey    | <input type="text" accesskey="s">                            | 规定激活（使元素获得焦点）元素的快捷键 采用alt+字母的形式    |

## 1.5 多媒体标签

- **embed** 可以用来插入各种多媒体，格式可以是Midi、Wav、AIFF、AU、MP3等等。

  ```html
  <embed src="http://..." allowFullscreen="true" quality="high" width="480" height="400" align></embed>
  ```

- **audio** 音频播放，autoplay自动播放；controls显示控件；loop循环播放
- **video** 视频播放

## 1.6 命名规范

|   名称   |           含义           |       名称        |   含义   |
| :------: | :----------------------: | :---------------: | :------: |
|  header  |            头            | content/container |   内容   |
|  footer  |         尾/页脚          |        nav        |   导航   |
| sidebar  |           侧栏           |      column       |   栏目   |
| wrapper  | 页面外围控制整体布局宽度 | left center right |  左中右  |
| loginbar |          登录条          |       logo        |   标志   |
|  banner  |           广告           |       main        | 页面主体 |
|   hot    |           热点           |       news        |   新闻   |
| download |           下载           |      subnav       |  子导航  |
|   menu   |           菜单           |      submenu      |  子菜单  |
|  search  |           搜索           |    friendlink     | 友情链接 |

# 2. css样式

## 2.1 字体

#### font-style:字体风格

- normal 默认值
- italic：斜体字体样式
- oblique：倾斜字体样式

#### font：综合设置字体样式

选择器{font：font-style font-weight font-size/line-height font-family}

#### letter-spacing、word-spacing字间距

- letter-spacing中英文都生效
  - 可用于消除inline-block元素间的换行符空格间隙问题。
- word-spacing只对英文单词生效

## 2.2 伪类选择器

### 2.2.1 链接伪类选择器

- :link  未访问的链接
- :visited  已访问的链接
- :hover   鼠标移动到链接
- :active   选定的链接

`被点击访问过的超链接样式不再具有hover和active了，解决方式为设置css样式时按照l-v-h-a的顺序设置。`

### 2.2.2 结构伪类选择器

- E:first-of-type与E:first-child区别

  - 匹配父元素下第一个类型为E的子元素
  - E必须是它的兄弟元素中的第一个元素

  

## 2.3 

# 3. 移动web开发

## 3.1 meta标签配置视口

- 配置方式

  ```html
  <meta name="viewport" content="width=device-width, user-scalable=no,initial-scale=1.0, maximum-scale=1.0, minimum-scale=1.0">
  ```

- 配置解析

  | 属性          | 解释说明                                             |
  | ------------- | ---------------------------------------------------- |
  | width         | 宽度设置的是viewport宽度，可以设置device-width特殊值 |
  | initial-scale | 初始缩放比，大于0的数字                              |
  | maximum-scale | 最大缩放比，大于0的数字                              |
  | minimum-scale | 最小缩放比，大于0的数字                              |
  | user-scalable | 用户是否可以缩放，yes或no（1或0）                    |

- 标准视口设置

  - 视口宽度和设备保持一致
  - 视口的默认缩放比例1.0
  - 不允许用户自行缩放
  - 最大允许的缩放比例1.0
  - 最小允许的缩放比例1.0

## 3.2 常用初始化样式

```css
* {
    margin: 0;
    padding: 0;
}
body {
    margin: 0 auto;
    max-width: 640px;
    min-width: 320px;
    background: #fff;
    font-family: -apple-system, Helvetica, sans-serif;
    line-height: 1.5;
    color: #666;
}
.clearfix::after {
    content: '';
    display: block;
    clear: both;
    height: 0;
    visibility: hidden;
    line-height: 0;
}
ul {
    list-style: none;
}
a {
    text-decoration: none;
    color: #666;
}
```

# 4. js 基础

## 4.1 JS数据类型

## 4.1.1 查看数据类型

- typeof 数据;
- typeof(数据);

## 4.1.2 数据类型转换

#### 其他类型 转数字类型

##### Number()

- 语法：把需要转的值或者变量放入括号内部；
- 结果：肯定能转成功；
  - 数字
  - NaN

##### parseInt()

- 将其他类型转为数字**整数**；
- 只能接受**字符串**，纯字符串、true、null、undefined都是NaN，字符串中的数字只能写在字符串的前面；

##### parseFloat()

- parseFloat这个方法用于转换字符串转换成小数(在编程中，小数也称浮点数)
- 非数字类型只能接受**字符串**，纯字符串、true、null、undefined都是NaN；
  - 如果**字符串前面是数字**，可以把前面的数字转化为数字类型；
  - 如果字符串中前面不是数字，转NaN；

#### 其它类型 转 字符串类型

##### String()

所有类型转换完后效果就是数据两边加单(双)引号；

##### .toString()

undefined和null不能使用这个方式变成字符串；

#### 其它类型 转 布尔类型

##### Boolean()

特点：返回一个布尔值。

- 6种情况返回值为false

  ```js
  var res1 = Boolean(0);
  console.log(res1); //输出false
  
  var res3 = Boolean(NaN);
  console.log(res3); //输出false
  
  
  var res2 = Boolean('');// 空字符，里面啥没有，空格也没有；
  console.log(res2); //输出false
  
  
  var res6 = Boolean(false);
  console.log(res6); //输出false
  
  
  var res5 = Boolean(null);
  console.log(res5); //输出false
  
  var res4 = Boolean(undefined); 
  console.log(res4); //输出false
  
  ```

## 4.2 流程控制

### 4.2.1 分支结构

- if结构
- switch-case结构
- 三元表达式

### 4.2.2 循环结构

- while结构
- for循环
- do-while循环

## 4.3 数组

## 4.4 函数

### 4.4.1 return的作用

- 修改返回值
- 终止函数执行

### 4.4.2 arguments

- 语法：可以获取所有传入函数的实参，形成一个伪数组；本质是个对象，可以循环遍历。

### 4.4.3 格式化日期的封装

```js
  function patchZero(v) {
    return v < 10 ? '0' + v : v;
  }

  function formatDate() {
    var now = new Date();
    var y = now.getFullYear();
    var m = now.getMonth() + 1;
    var d = now.getDate();
    var h = now.getHours();
    var mm = now.getMinutes();
    var s = now.getSeconds();
    return y + '-' + patchZero(m) + '-' + patchZero(d) + ' ' + patchZero(h) + ":" + patchZero(mm) + ':' + patchZero(s);
  }

```



## 4.5 对象

### 语法

#### 创建

- 构造函数：

```javascript
var obj = new Object(); // 这是一个没有属性和方法的对象
console.log(obj);

```

- 字面量：

```javascript
var obj = {}; // 这也是一个没有属性和方法对象，其本质和构造函数创建的对象是一样的
console.log(obj,typeof obj);

```

#### 添加

```javascript
var obj = {};
// 对象.属性 = 值;
obj.name = "";
// 对象.方法名 = function(){}
obj.sayName = function(){  
	
}

```

## 4.6 内置对象

### 4.6.1 Math

- Math.random(x)；这个方法的作用是生成一个 [0,1) 之间的随机浮点数

```js
var r = Math.random();
// 每次执行等到的数字都不一样
console.log(r);

```

- Math.floor(x)   把一个浮点数进行向下取整

```js
console.log(Math.floor(3.1));  // 3
console.log(Math.floor(3.9));  // 3
console.log(Math.floor(-3.1)); // -4
console.log(Math.floor(-3.9)); // -4

```

- Math.ceil(x) 把一个浮点数进行向上取整
- Math.round(x)  把一个浮点数进行四舍五入取整
- Math.abs(x)  求一个数的绝对值 正数
- Math.max(x,y...)  求多个数字中的最大值，同理 Math.min(x,y...);

### 4.6.2 Date

- 语法：

```js
var date = new Date(); // 得到的是当前时间的日期对象

```

- 获取年月日时分秒

```js
console.log(date.getFullYear());// 年份
console.log(date.getMonth()); // 月份，从0开始


console.log(date.getDate()); //日期

console.log(date.getHours()); // 小时，0-23
console.log(date.getMinutes()); // 分钟 ， 0-59
console.log(date.getSeconds()); // 秒数 ， 0-59
console.log(date.getMilliseconds()); // 毫秒 0-999 ， 1秒 = 1000毫秒

```

- 创建一个**指定日期**的对象

```js
// 给一个日期格式字符串
var date = new Date('2019-01-01');

// 分别传入年月日时分秒。注意传入的月份是从0开始算的
var date = new Date(2019,0,1,12,33,12);

```

- 获取从1970年1月1日到现在的总毫秒数，**常说的时间戳**

```js
var date = new Date();
//四种方式
console.log(date.valueOf());
console.log(date.getTime());
console.log(1*date);

console.log(Date.now());

```



### 4.6.3 array

#### 对元素操作

| 方法名  | 用法                                                         | 含义                                     | 方法返回值       |
| ------- | ------------------------------------------------------------ | ---------------------------------------- | ---------------- |
| push    | var arr = [1, 2, 3, 4, 5, 6, 7];<br />var res = arr.push(2); | 从数组后面推入一个元素或多个元素         | 数组长度         |
| pop     | var res = arr.pop();                                         | 删除数组最后一个元素                     | 被删除的元素     |
| unshift | var res = arr.unshift(20);                                   | 从数组开始位置添加元素                   | 修改后数组的长度 |
| shift   | var res = arr.shift();                                       | 用于将数组的第一个元素移除               | 被删除的元素     |
| splice  | var res = arr.splice(3,0,1,2);<br />//第一个参数是索引，第二个参数是删除数据的个数，后续参数是添加的元素 | 用于从数组的指定位置移除、添加、替换元素 | 返回被删除的数组 |

#### 与字符串互转

- join 用于将数组中的多元素以指定分隔符连接成一个字符串

```js
var arr = ['刘备','关羽','张飞'];
var str = arr.join('|'); 
console.log(str);  // 刘备|关羽|张飞

```

- split 字符串的方法：转数组，后面为分隔的字符

```js
// 这个方法用于将一个字符串以指定的符号分割成数组
var str = '刘备|关羽|张飞';
var arr = str.split('|');
console.log(arr);

```

#### 查找元素

- indexOf：根据元素查找索引，如果这个元素在数组中，返回索引，否则返回-1

```js
var arr = [10,20,30]
console.log(arr.indexOf(30));  // 2
console.log(arr.indexOf(40));  // -1

```

- findIndex方法用于查找满足条件的第一个元素的索引，如果没有，则返回-1

```js
var arr = [10, 20, 30];
var res1 = arr.findIndex(function (item) {
  return item >= 20;
});
// 返回 满足条件的第一个元素的的索引
console.log(res1);  

var res2 = arr.findIndex(function (item) {
  return item >= 50;
});
// -1
console.log(res2);

```

#### 遍历数组

- for循环

- forEach：遍历数组

  ```js
  var arr = [3, 2, 5, 7, 4, 6, 4];
  
  // item是数组中的每个元素，index是item的索引,arr表示当前数组；
  // 对本数组操作，没有返回值；
      arr.forEach(function(item, index) {
          console.log(item, index);
      })
  
  ```

  

- filter() 筛选出数组中满足条件的数组，**返回是一个新的数组**；

  ```js
  // 数组的filter方法用于将数组中满足条件的元素筛选出来
  // 筛选出数组中 小于 2000 的数据
  var arr_1 = [1500,1800,2200,300,2600,800];
  var res = arr_1.filter(function(item,index,arr){
    return item < 2000;
  });
  // fitler方法的的参数要求是一个函数，这个函数接收2个参数：item是数组中的每个元素，index是item对应的索引,arr代表当前的数组
  
  
  
  ```

- some() 

#### 拼接与截取

- concat 拼接数组，**不改变原数组，创建新数组返回**

  ```js
  // 数组的concat方法的作用是把多个数组合并成一个新的数组
  var arr1 = [1,2,3];
  var arr2 = [4,5,6];
  var arr3 = [7,8,9];
  var res = arr1.concat(arr2,arr3);
  console.log(res);
  
  ```

- slice 截取数组：**不对原数组操作，返回的是新的数组**；

  ```js
  var arr = ['a','b','c','d','e'];
  // 表示 从下标1（包括），截取到下标为4(不包括),
  var res = arr.slice(1, 4);
  
  // 如果不给第二个参数，默认就是把从start开始，到length结束的所有的元素截取
  var arr_1 = arr_2.slice(1);
  
  // 复制数组：如果省略两个参数，start默认是0，end默认是length
  var arr_1 = arr_2.slice();
  
  ```

#### 复制

- 方法一：for循环

  ```js
  var newArr_1 = [];
      for (var index = 0; index < newArr_1.length; index++) {
          newArr_1[index] = arr[index];
      }
  
  ```

  

- 方法二：forEach遍历

  ```js
  var newArr_2 = [];
      arr.forEach(function(item, index) {
          newArr_2.push(item);
      });
  
  ```

- 方法三：filter

  ```js
  var arr_1 = arr_2.filter(function(item,index,arr){
    return item;
  });
  
  ```

- 方法四：concat拼接

  ```js
  // 复制一个数组
  var arr_1 = arr.concat();
  
  ```

- 方法五：slice截取

  ```js
  var new_arr = arr.slice();
  
  ```

  

### String

#### 查找

```js
 var str = "我爱北京天安门";

//查询字符在字符串中的位置
    var index = str.indexOf("北京");
    console.log(index); //2

    index = str.indexOf("d");
    console.log(index); //-1

// 查询字符串下标位置的字符
    var char = str.charAt(2);

// var a = "a";
  // a.charCodeAt(); 返回ASCII 码
  var res = str.charCodeAt(0);
  console.log(res);

```

#### 拼接与截取

- +

- concat 拼接

  ```js
  // 这个方法用于连接多个字符串，其作用相当于 + 操作符
  var res = "abc".concat('def','ghi');
  console.log(res);
  
  ```

- substring 截取字符串，不操作原字符；返回截取出来的字符串

  ```js
  // 这个方法用于获取字符串中的部分字符
  var str = '我爱中华人民共和国';
  
  // 从索引2开始，到索引4结束，得到之间的字符，不包含索引4的字符
  var res = str.substring(2,4);
  console.log(res);
  
  ```

- slice

  ```js
  // 这个方法用于获取字符串中的部分字符
  var str = '我爱中华人民共和国';
  var res = str.slice(2,4);// 从索引2开始，到索引4结束，得到之间的字符，不包含索引4的字符
  console.log(res);
  
  // 看起来和substring 没有啥区别，
  // slice()可以设置参数为负数，slice()方法在遇到负的参数的时候，会将这个负值与字符串的长度相加。
  console.log(str.slice(-6,7));
  console.log(str.slice(2,-5));
  console.log(str.slice(-9,-7));
  
  ```

- substr

  ```js
  // 这个方法用于获取字符串中的部分字符
  var str = '我爱中华人民共和国';
  var res = str.substr(2,2);// 人索引2开始，总共获取2个字符，第二个参数为个数
  
  ```

  

# 5. Web API

## 5.1 DOM

- js组成：
  - ES：js基础知识
  - DOM：**文档对象模型**
    - DOM节点：标签本身、标签上的属性、标签内文本
  - BOM：浏览器被当作一个对象。

### 5.1.1 事件类型

#### 点击事件：click

- xx.onclick=function(){}

#### scroll事件

- 谁有滚动条注册给谁，浏览器注册给window

#### 焦点事件：focus、blur

- 注册给有光标的盒子 input、textarea；
- 事件类型：
  - 有光标时：获得焦点focus；
  - 无光标时：失去焦点 blur

```js
ipt.onfocus = function(){
  // 当你想要让鼠标光标在输入框里面的时候要做什么事，就使用这个事件即可
}

ipt.onblur =  function(){
  //当你希望处理鼠标光标失去的时候所做的事情，就在这里做
}

```

#### 键盘事件：keydown,keyup

- 按键按下：keydown
- 按键弹起：keyup
- 按下哪个键？
  - 事件对象.keyCode，这个属性被称为  键盘码 ，每个按键对应的数字是不一样 ，只需要判断数字，就知道按下的按键是哪一个； keyCode==13 回车键
  - 按下了ctrl：事件对象里面有一个属性 ctrlKey ；如果是true，按下了ctrl键

#### 鼠标移动事件：mouseover（mouseenter）、mouseout（mouseleave）、mousemove

- 鼠标移入、移出某个元素或移动的时候，触发事件
- mouseover-mouseout支持事件冒泡，mouseenter-mouseleave不支持事件冒泡

#### 动画结束事件

- transitionend：元素的过渡动画结束的时候触发；
- animationend：会在帧动画结束时触发；
  - 注意：
    - 不能使用on的方式注册，只能使用addEventListener的方式注册
    - 如果帧动画是无限次的，不会触发该事件

### 5.1.2 操作 类样式-classList

- add 添加类名：

```js
// 参数：多个类名，之间用逗号隔开
box.classList.add(类名1,类名2...)；

```

- remove 移除类名：

```js
// 参数：多个类名，可以是多个，多个之间用逗号隔开
box.classList.remove(类名1,类名2...)

```

- toggle 切换类名：

```js
// 参数： 要切换的类名
box.classList.toggle(类名)

```

### 5.1.3 案例：全选与反选

```js
var ckAll = document.getElementById("checkAll");
var cks = document.getElementsByClassName("ck");

    // 需求，点击全选按钮后，所有子按钮选中

    ckAll.onclick = function() {

        for (var index = 0; index < cks.length; index++) {
            cks[index].checked = ckAll.checked;

        }
    }

    // 子选项全选，父选项自动变为选择
    // 子项存在未选中项时，父选项未选中
    for (var i = 0; i < cks.length; i++) {

        cks[i].onclick = function() {
            // 使用反证法实现判断是否全选
      		// 1 假设全都选中了
            var flag = true;
             
            // 2 循环的去找反例，只要有一个没勾选，就推翻假设
            for (var j = 0; j < cks.length; jndex++) {
                if (cks[j].checked != true) {
                    // 至少有一个没有勾选，推翻假设
                    flag = false;
                    break;
                }
            }
            // 3 再次判断假设是否成立
            // if (flag) {
                // 如果是true，证明全都勾选，设置全选是选中的
             //   ckAll.checked = true;
            //} else {
                // 证明没有全都勾选，设置全选是取消选中的
            //    ckAll.checked = false;
           // }
            // flag ? ckAll.checked = true : ckAll.checked = false;
            ckAll.checked = flag;
        }

    }

```



### 5.1.4 获取元素对象 选择器

```js
// 作用： 根据指定的选择器获取从上到下的第一个元素，获取不到返回个null对象；
document.querySelector(css选择器);

// 作用：根据选择器获取所有满足条件的元素，这个使用的比较多；
// 参数：多个css选择器，以逗号隔开，都是字符串
// 返回值：伪数组；for，但是上面有forEach方法
document.querySelectorAll(css选择器1,css选择器2...);
// 可简单判别下和获取通过ID获取的DOM节点有什么区别

```

### 5.1.5 操作属性

- 一般情况下是操作自定义属性多一些；

```js
// 作用： 根据属性名获取属性值
// 参数： 要获取的属性名,标准属性和自定义属性都可以。而且自定义属性不再限制于 data-属性 的格式要求
// 返回值： 字符串
元素.getAttribute(属性名)

// 作用： 添加或者修改属性的值
// 参数：都是字符串；
元素.setAttribute(属性名,属性值)

// 作用：删除某个属性
元素.removeAttribute(属性名)

```

### 5.1.6 添加事件监听

addEventListener：添加事件监听，可以多次注册事件；

```js
// 参数： 事件类型 - 字符串； 事件处理程序 - function 
dom.addEventListener('click', function() {
    
})

```

### 5.1.7 事件三阶段

- 捕获、到达目标、冒泡；

- **阻止冒泡**

  ```js
  dom.addEventListener('click',function(e){
    // 调用阻止事件冒泡的方法进行阻止
    // 事件对象 e 把该次点击这个过程看成一个对象
    e.stopPropagation();//位置无所谓
    ...
  });
  
  ```

  

### 5.1.8 事件对象

```js
// 获取事件对象
事件源.on+事件类型 = function(事件对象){   }

事件源.addEventListener(事件类型,function(事件对象){});

```



- 属性：

  ```js
  // 鼠标位置
  
  // 可视区域坐标系 - 以浏览器的可视区域的左上角为原点的
  // 可视区域：就是元素用来显示内容的区域
  事件对象.clientX
  事件对象.clientY
  
  // 页面坐标系  -  以body的左上角作为原点
  事件对象.pageX
  事件对象.pageY
  
  
  // 事件的目标对象，用户点击到谁上面了；
  事件对象.target
  
  // 事件的绑定对象，就是是绑定在哪个DOM节点上 和 this一样
  // 前面说的事件源
  e.currentTarget==this -----> true
  
  ```

- 方法：

  ```js
  // 阻止冒泡
  事件对象.stopPropagation();
  
  // 阻止默认行为；
  事件对象.preventDefault();
  
  // 页面右键事件 查看右键菜单
  document.oncontextmenu = function(e){
    e.preventDefault();
  }
  
  // 阻止a标签转跳
  // 1 把a标签的href属性设置为 javascript:void(0);
  // 2 在a标签的点击事件里面，return false;
  // 3 使用事件对象.preventDefault();
  dom_a.addEventListener('click', function(e) {
      e.preventDefault();
  });
  
  ```

  

### 5.1.9 获取元素对象属性

#### 位置

```js
// 得到的是某个元素距离他的offsetParent元素的水平距离
// 元素.offsetLeft = marginLeft + left
元素.offsetLeft 

// 得到的是某个元素距离他的offsetParent元素的垂直距离
// 元素.offsetTop = marginTop + top
元素.offsetTop 

// 找到一个有定位的父亲元素，如果亲生父亲没有定位，会一直往上找，直到找打有定位的父亲，或者body；
元素的offsetParent

```

#### 元素实际宽度和高度

- 元素的实际宽高 = border+padding+content（width和height）

```js
// 返回值：数值；

// 只能进行获取；
// 元素的实际宽度
元素.offsetWidth 
// 元素的实际高度
元素.offsetHeight

// 获取和设置
dom.style.width；

```

#### 可视区域宽度、高度

```js
元素.clientWidth - 可视区域的宽度
元素.clientHeight - 可视区域的高度

```



### 5.1.10 DOM节点创建、添加、修改

#### 方法：创建节点

- innerHTML(属性)*
- document.write()：
  - 把页面已经存在的结构覆盖；
  - 可以解析HTML结构；
- document.createElement()：
  - 根据指定的标签名，创建一个新的元素

#### 方法：添加节点

- appendChild：

  - 给制定的父元素追加子元素，**作为最后一个子元素；从后添加一个子元素**

    ```js
    // 元素.appendChild(子元素);
    var li = document.createElement('li');
    ul.appendChild(li);
    
    ```

- insertBefore：

  - 在某个子元素之前，插入新的子元素

    ```js
    //父元素.insertBefore(新的子元素,插入谁之前的旧的子元素)
    var second = document.querySelector('.second');
    ul.insertBefore(li,second);
    
    ```

#### 属性：修改节点

- innerHTML：
  - 用于获取或者设置某个元素的**内部结构**(html结构)；
  - 会覆盖旧的结构；
  - 对于页面上已经存在的、或者即将新创建的节点都适用。
- innerText：
  - 用于获取或者设置某个元素里面的**文本内容**，不具备解析HTML结构；
  - 对于页面上已经存在的、或者即将新创建的节点都适用。

#### DOM节点获取方式

- 方法获取

  ```js
  var first = document.querySelector('ul > li:first-child');
  
  ```

- 根据DOM节点 获取 DOM节点（属性获取）

- 获取子元素：可以得到某个元素之下的所有的子元素的集合，一个**伪数组**

```
父元素.children

```

- 获取父元素

```js
元素.parentNode

```

- 获取兄弟元素

```js
元素.nextElementSibling  -  得到下一个兄弟元素
元素.previousElementSibling - 得到上一个兄弟元素

```

### 5.1.11 删除DOM节点

```js
// 父元素.removeChild(要删除的子元素);


```

## 5.2 BOM

### 5.2.1 onload

- 页面加载完毕的时候执行
- 页面加载完毕：页面所需的静态资源全部加载完毕
- 静态资源： **html文件、css文件、js文件、图片...**

```javascript
window.onload = function(){
    // 想要获取图片的宽高，就需要等待图片加载完成后才执行后面的函数；
}

```

### 5.2.2 定时器

- 一次性定时器
  - setTimeout
  - clearTimeout   清除定时器
- 永久性定时器
  - setInterval
  - clearInterval     清除永久定时器

#### 【案例】获取验证码-倒计时

```js
// 获取按钮
var btn = document.getElementById('getCode');
// 注册点击事件
btn.onclick = function(){
  // 禁用按钮，禁用不能点击了；
  btn.disabled = true;
    
    
  // 开始倒计时
  var time = 5;
  // 在点击的时候，先改变一次
  btn.value = '获取验证码('+ time +')';
    
  
  // 设置倒计时
  var timer = setInterval(function(){  
    // 每隔1秒钟，数字要减少1
    time--;  
    // 修改按钮的内容
    btn.value = '获取验证码('+ time +')';   
      
      
    // 当倒计时到达0的时候，停止定时器
    if(time === 0){
      // 停止的定时器
      clearInterval(timer);
      // 把按钮还原
      // 文字还原
      btn.value = '获取验证码';
      // 可以点击
      btn.disabled = false;
    }
      
  },1000);
}

```



### 5.2.3 属性对象 location

- 负责管理浏览器地址栏相关的行为和信息的对象；

### 5.2.4 localStorage 和 JSON

#### localStorage

- 实现数据的本地存储

```js
// 注意： 如果存储的是对象之类的复杂类型，需要先把复杂类型转换为JSON格式的字符串，再存进去，因为本地存储只能存储字符串
localStorage.setItem(键,值);

// 读取数据
// 返回值：就是我们存入的的数据的值
localStorage.getItem(键);

//删除数据
localStorage.removeItem(健);


//全部清空
localStorageclear();                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             

```

#### JSON

```js
// 将对象转换为json格式的字符串
// 返回值：一个满足json格式的 字符串
JSON.stringify(对象);

// 将json格式的字符串转换为对象
// 返回值：依赖于你的json格式字符串，可能返回数组，或者是对象....
JSON.parse(json格式字符串);

```

# 6. jQuery

- 入门

  - 入口函数

    ```js
    $(function(){
        ...
    })
    
    ```

## 6.1. jQuery筛选方法

- **元素.parent()**：父级
- **元素.parents()**：所有祖先，有参数时为指定
- **元素.children()**：所有子集，有参数时为指定子集
- **元素.find()**：所有后代，有参数时为指定
- **元素.siblings()**：所有兄弟，有参数时为指定
- **元素.eq(index)**：指定索引元素
- 元素.nextAll()：后面的
- 元素.prevAll()：前面的

## 6.2 jQuery 操作

### 6.2.1 样式操作

```js
//--------------行内样式------------------
//参数只写属性名时，返回属性值
元素.css("属性名")

//设置样式，参数是属性名，属性值，逗号分隔，是设置一组样式，属性必须加引号，值如果是数字可以不用
元素.css("属性名","属性值")

//对象形式设置多组样式
元素.css({"属性名":"属性值","属性名":"属性值"})


//----------------------设置类样式------------
//添加类名
元素.addClass("类名")

//移除类名
元素.removeClass("类名")

//切换类名
元素.toggle("类名")

```

### 6.2.2 属性操作

- **prop()**:设置或获取元素固有属性值
  - 设置：prop("属性")；获取：prop("属性"，"属性值")
- **attr()**:设置或获取元素自定义属性值
  - 设置：attr("属性")；获取：attr("属性"，"属性值")
- data():数据缓存
  - `data() 方法可以在指定的元素上存取数据，并不会修改 DOM 元素结构，所以元素上无法查看。一旦页面刷新，之前存放的数据都将被移除。`
  - data(''name'',''value'')   // 向被选元素附加数据   
  - date(''name'')             //   向被选元素获取数据  

### 6.2.3 元素操作

#### 遍历

- ```js
  $().each(function(index,domEle) {})
  //遍历匹配的每一个元素，主要做DOM处理
  
  ```

- ```js
  $.each(object,function(index,element){})
  //可用于遍历任何对象。主要用于数组处理，比如数组，对象
  
  ```

#### 创建

```js
$("<li></li>")

```

#### 添加

- 内部添加

  - ```js
    element.append("内容")   //把内容放入匹配元素的内部最后面
    
    ```

  - ```js
    element.prepend("内容")   //把内容放入匹配元素内部的最前面
    
    ```

- 外部添加

  - ```js
    element.after("内容")  //把内容放入目标元素后面
    
    ```

  - ```js
    element.before("内容")    //把内容放入目标元素的最前面
    
    ```

#### 删除

- ```js
  element.remove()  //是移除匹配的元素本身
  
  ```

- ```js
  element.empty()   //删除匹配的元素集合中的所有子节点`
  
  ```

- ```js
  element.html("")   //清空匹配的元素内容
  
  ```

### 6.2.4 jQuery 尺寸操作

- width()，height()
  - 只计算width和height
- innerWidth()，innerHeight()
  - 包含padding+width/height
- outerWIdth()，ouerHeight()
  - 包含padding、border、width/height
- outerWIdth(true)，outerHeight(true)
  - 包含padding、border、margin、width/height

### 6.2.5 jQuery 位置操作

- **offset()**  设置或获取元素偏移

  - 距离**文档**的距离【top，left】

  - 设置：

    ```js
    offset({top:10,left:10})
    
    ```

- **position()**  获取元素偏移

  - 返回被选元素相对于**带有定位的父级**的偏移坐标，如果父级都没有定位，则以文档为准。
  - 只读，不能设置

- **scrollTop()、scrollLeft()** 设置或获取元素被卷起的头部和左侧

## 6.3 jQuery 动画效果

### 6.3.1 显示隐藏基本效果

```
show([speed,[easing],[fn]])
hide([speed,[easing],[fn]])
toggle([speed,[easing],[fn]])


（1）参数都可以省略， 无动画直接显示。
（2）speed：三种预定速度之一的字符串(“slow”,“normal”, or “fast”)或表示动画时长的毫秒数值(如：1000)。
（3）easing：(Optional) 用来指定切换效果，默认是“swing”，可用参数“linear”。
（4）fn:  回调函数，在动画完成时执行的函数，每个元素执行一次。

```

### 6.3.2 显示隐藏上下滑动效果（slide）

```
slideDown([speed,[easing],[fn]])
slideUp([speed,[easing],[fn]])
slideToggle([speed,[easing],[fn]])


（1）参数都可以省略。
（2）speed：三种预定速度之一的字符串(“slow”,“normal”, or “fast”)或表示动画时长的毫秒数值(如：1000)。
（3）easing：(Optional) 用来指定切换效果，默认是“swing”，可用参数“linear”。
（4）fn:  回调函数，在动画完成时执行的函数，每个元素执行一次

```

### 6.3.3 显示隐藏淡入淡出效果（fade）

```
fadeIn([speed,[easing],[fn]])
fadeOut([speed,[easing],[fn]])
fadeToggle([speed,[easing],[fn]])
fadeTo([[speed],opacity,[easing],[fn]])【注意fadeTo必须写两个参数，speed和opacity】


（1）参数都可以省略。
（2）speed：三种预定速度之一的字符串(“slow”,“normal”, or “fast”)或表示动画时长的毫秒数值(如：1000)。
（3）easing：(Optional) 用来指定切换效果，默认是“swing”，可用参数“linear”。
（4）fn:  回调函数，在动画完成时执行的函数，每个元素执行一次。


```

### 6.3.4 自定义动画（anmiate）

```
语法：animate(params,[speed],[easing],[fn])

参数：
（1）params: 想要更改的样式属性，以对象形式传递，必须写。 属性名可以不用带引号， 如果是复合属性则需要采取驼峰命名法 borderLeft。其余参数都可以省略。
（2）speed：三种预定速度之一的字符串(“slow”,“normal”, or “fast”)或表示动画时长的毫秒数值(如：1000)。
（3）easing：(Optional) 用来指定切换效果，默认是“swing”，可用参数“linear”。
（4）fn:  回调函数，在动画完成时执行的函数，每个元素执行一次。

```

### 6.3.5 动画队列及其停止排队方法

```
动画或者效果一旦触发就会执行，如果多次触发，就造成多个动画或者效果排队执行。

停止排队:stop()

(1）stop() 方法用于停止动画或效果。
(2)  注意： stop() 写到动画或者效果的前面， 相当于停止结束上一次的动画


```

## 6.4 jQuery 内容文本值

- 普通元素内容 html()
  - 获取：html()
  - 设置：html("内容")
- 普通元素文本内容 text()
  - 获取：text()
  - 设置：text("内容")
- 表单的值 val()
  - 获取：val()
  - 设置：val("内容")



# 7. jS高级

## 7.1 ES6 类class

- **创建类**
  - 语法：class 类名 {}
    - 类名首字母大写
    - 类要抽取公共属性方法，定义一个类

## 函数进阶

### 递归函数

- 函数调用其本身

  ```js
  function fn() {
              var n = 3;
              var m = "a";
  
              // 自调用
              fn();
          }
          fn();
  
  ```

  

# 8 ajax

## 8.1 ajax请求方式

- GET：浏览器的目的是希望从服务器得到一些东西
- POST：浏览器希望将数据提交给服务器

## 8.2 Ajax发送GET请求

Ajax的核心是内置在浏览器中的 `XMLHttpRequest` 对象。

```js
//创建浏览器内置的对象 XMLHttpRequest，简称xhr对象
var xhr = new XMLHttpRequest();

//调用xhr对象的open方法，设置请求方式和请求的url
xhr.open('GET','http://localhost:4000/time');

//调用xhr对象的send方法，向服务器发送请求
xhr.send();

//当请求响应整个过程结束，然后接收服务器响应的结果
xhr.onload=function(){
    
    //使用xhr的response属性来接收服务器响应的结果
    console.log(xhr.response)
}



```

### GET请求传参

- 什么时候需要带请求参数
  - 请求参数又叫查询字符串
  - 一般用于告诉浏览器此次请求的目的，比如查询什么，删除哪条记录等等
- url携带查询字符串
  - 格式：http://www.baidu.com/s?q=word&sug=5017
  - 查询字符串(querystring):
    - url中==问号后面==携带的就是get请求传参的数据，叫做查询字符串
    - 格式：aa==xxx&bb=yyy
    - 查询字符串知识和传输少量数据

