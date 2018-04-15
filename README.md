# Getting-to-know-front-end
## 前端开发：HTML+CSS+JavaScript

### 什么是HTML

- HTML文件就是浏览器显示的文件，html语言就是超文本标记语言。
- 包括各类标签，负责页面布局，就是为整个页面搭架子，骨架。
- 类比于iOS开发中的各种控件：<div> ->UIView ; <button> ->UIButton

### 什么是CSS

- CSS负责页面样式，比如HTML标签显示的宽、高、位置等等。
- CSS包括各类属性，用于调节标签的样式。
- 类比与iOS开发中各控件的attribute属性。

### 什么是JavaScript

- JavaScript为网页添加一些交互和动态功能，比如处理各类用户事件，与服务端交互，动态改变样式等，让网页动起来。
- JavaScript组成：
- ECMAScript：翻译解释器；
- DOM：操作HTML
- BOM：操作浏览器

## VUE技术框架实践

### 环境配置
首先是决定了用Windows作为开发环境，先配置一下vue开发环境和Atom。

在下载安装完nodejs之后，需要在node的主文件夹下建立两个文件夹：node_global和node_catch，这俩一个是用于存储nodejs的全局模块，另一个我还不太清楚，大概还没用到

建立两个文件夹之后，需要使用cmd命令框，输入如下两个命令，用于修改node的一些配置：

npm config set prefix "C:\Program Files\nodejs\node_global"

npm config set cache "C:\Program Files\nodejs\node_cache"

然后还需要修改两次环境变量中的路径，一个是在Path中添加： 
C:\Program Files\nodejs\node_global 

无论是系统的Path还是用户的Path都可以，然后再在系统环境变量列表中个，新建一个叫做NODE_PATH的环境变量，内容是： 

C:\Program Files\nodejs\node_global\node_modules

### 实践
#### Vue组件

main.js入口文件 内容为：import Vue from ‘vue’  //es6的写法类似于require（）

##### 组件树：
![image](https://github.com/lqAsuna/Getting-to-know-front-end/blob/master/image/image1.png)

#### 文本渲染

v-once 执行一次性地插值，当数据改变时，插值处的内容不会更新。

<span v-once>这个将不会改变: {{ msg }}</span>

*{{  }}在2.0中已经不能使用到属性里  例如 <div title={{xxx}}> 是被禁止的 

{{}}中可以这么写{{num + 1}}  甚至三目运算符等一些简单表达式

<!-- 这是语句，不是表达式 -->
{{ var a = 1 }}
<!-- 流控制也不会生效，请使用三元表达式 -->
{{ if (ok) { return message } }}

##### v-html和v-text
![image](https://github.com/lqAsuna/Getting-to-know-front-end/blob/master/image/image2.png)

##### 结果
![image](https://github.com/lqAsuna/Getting-to-know-front-end/blob/master/image/image3.png)

#### 列表渲染
##### v-for
![image](https://github.com/lqAsuna/Getting-to-know-front-end/blob/master/image/image4.png)

在需要循环的项添加v-for 而不是在父级添加
##### 结果
![image](https://github.com/lqAsuna/Getting-to-know-front-end/blob/master/image/image5.png)
