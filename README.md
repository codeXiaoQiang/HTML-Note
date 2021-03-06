   * [精华笔记](#精华笔记)
       * [基础知识储备](#基础知识储备)
           * [软件架构](#软件架构)
               * [c/s(客户端与服务器)](#cs客户端与服务器)
               * [b/s(浏览器与服务器)](#bs浏览器与服务器)
         * [进制](#进制)
            * [二进制](#二进制)
            * [十进制](#十进制)
            * [十六进制](#十六进制)
            * [八进制](#八进制)
         * [乱码](#乱码)
            * [乱码的原因](#乱码的原因)
            * [编码](#编码)
            * [解码](#解码)
            * [字符集](#字符集)
      * [HTML](#html)
         * [概念](#概念)
         * [网页的结构](#网页的结构)
         * [文档声明](#文档声明)
         * [标签](#标签)
         * [常用标签](#常用标签)
         * [文本标签](#文本标签)
         * [图片标签](#图片标签)
         * [列表](#列表)
         * [属性](#属性)
         * [实体](#实体)
         * [相对路径](#相对路径)
         * [注释](#注释)
         * [xHtml语法规范](#xhtml语法规范)

# 精华笔记
## 基础知识储备
#### 软件架构
##### c/s(客户端与服务器)
* 概念
    * 一般我们使用的软件都是C/S架构
    * 比如系统的中的软件QQ、360、office、XMind
    * C表示客户端，用户通过客户端来使用软件
    * S表示服务器，服务器负责处理软件的业务逻辑
* 特点
    * 1.软件使用前必须得安装
    * 2.软件更新时，服务器和客户端得同时更新
    * 3.C/S架构的软件不能跨平台使用
    * 4.C/S架构的软件客户端和服务器通信采用的是自有协议，相对来说比较安全
##### b/s(浏览器与服务器)
* 概念
    * 1.B/S本质上也是C/S，只不过B/S架构的软件，使用浏览器作为软件的客户端
    * 2.B/S架构软件通过使用浏览器访问网页的形式，来使用软件
    * 3.比如：京东 淘宝 12306 知乎 新浪微博
* 特点
    * 1.软件不需要安装，直接使用浏览器访问指定的网址即可
    * 2.软件更新时，客户端不需要更新
    * 3.软件可以跨平台，只要系统中有浏览器，就可以使用
    * 4.B/S架构的软件，客户端和服务器之间通信采用的是通用的HTTP协议，相对来说不安全
### 进制
#### 二进制
* 0 1
* 10 11 100 101 110 111
#### 十进制
* 0 1 2 3 4 5 6 7 8 9
* 10 11 12 13 14 。。。
#### 十六进制
* 满十六进1
* 0 1 2 3 4 5 6 。。。 9 a b c d e f
* 10 11 12 ... 19 1a 1b 1c 1d 1e 1f
* 16进制由于是满16进1，所以必须设置几个特殊的字符来表示10 11 12 13 14 15
* 使用a b c d e f分别表示10 11 12 13 14 15
#### 八进制
* 满8进1
* 0 1 2 3 4 5 6 7
* 10 11 12 13 14 15 16 17 20 21 22
### 乱码
#### 乱码的原因
* 计算机是一个非常笨的机器，它只认识两个东西 0 1
* 在计算机中保存的任何内容，最终都需要转换为0 1这种二进制编码来保存，包括网页中的内容
* 比如：中国，在计算机底层，可以能需要转换为 1010001001010101011010
* 在读取内容时，需要将二进制编码，在转换为正确的内容
* 产生乱码的根本原因是，编码和解码采用的字符集不同
#### 编码
* 依据一定的规则，将字符转换为二进制编码的过程
#### 解码
* 依据一定的规则，将二进制编码转换为字符的过程
#### 字符集
编码和解码所采用的规则，我们称为字符集
* 常见的字符集
    * ASCII
    * ISO-8859-1
    * GBK
    * 中文系统的默认编码GB2312
    * 万国码，支持地球上所有的文字UTF-8
    * 自动以系统的默认编码来保存文件ANSI
    * 在中文系统的浏览器中，默认都是使用GB2312进行解码的
## HTML
### 概念
* Hypertext markup language HTML，超文本标记语言
* 负责页面中的结构，定义出页面中的各个组成部分
* HTML是采用纯文本的形式的编写，采用HTML标签来标识出页面中的不同部分
### 网页的结构
```
<!doctype html>
<html>
	<head>
		<meta charset="utf-8" />
		<title></title>
	</head>
	<body>
		<!-- 网页的主体内容 -->
	</body>
</html>
```
### 文档声明
`
<!doctype html>
`
* 用来标识当前页面的html的版本
* 该声明用来告诉浏览器，当前的页面是使用HTML5的标准编写的
### 标签
* <标签名></标签名> 双标签
* <标签名 /> 单标签
### 常用标签
* html
    * 网页的根标签
    * 一个页面中有且只有一个根标签
    * 网页中的所有内容都需要写在html标签的内部
* head
    * 网页的头部
    * 该标签中的内容不会在网页中直接显示
    * 该标签用于帮助浏览器解析页面
    * 子标签
      *  title
        索引擎检索网页时，会主要检索title中的内容，它会影响到页面在搜索引擎中的排名
      *  meta
      	*  用来设置网页的元数据，比如网页使用的字符集
		```
		<meta charset="utf-8" />
		```
	* 设置网页的关键字
		```
		<meta name="keywords" content="关键字,关键字,关键字,关键字"/>
		```
	* 设置网页的描述
		```
		<meta name="description" content="网页的描述"/>
		```
	* 请求的重定向
		```
		<meta http-equiv="refresh" content="秒数;url=地址"  />
		```
* body
    * 网页的主体
    * 网页中所有的可见部分都需要在body中编写
* h1 ~ h6
    * 标题标签
    * 在html中一共有六级标题
    * 六级标题中，h1最重要，h6最不重要，一般页面中只会使用h1~h3
    * h1的重要性仅次于title，浏览器也会主要检索h1中的内容，以判断页面的主要内容
    * 一般一个页面中只能写一个h1
* p
    * 段落标签
* br
    * 换行标签
* hr
    * 水平线标签
* 内联框架
    ```
    <iframe></iframe>
    ```
    1.可以向一个页面中引入其他的外部页面
    2.内联框架中的内容不会被搜索引擎所检索，所以开发中尽量不要使用内联框架
    3.属性
    * src 
        * 外部页面的地址，可以使用相对路径
    * width和height 
        * 可以设置框架的宽度和高度
    * name
        * 可以为内联框架指定一个名字
        * 可以将该属性值设置为超链接的target属性的值
        * 这样当点击超链接时，页面将会在相应的内联框架中打开

* 超链接
```
<a>链接的文字</a>
```
1.可以使当前页面跳转到其他的页面
2.属性:
  * href
    * 指向链接跳转的目标地址，可以是一个相对路径
    * 还可以是#id属性值，这样当点击超链接以后，将会跳转到当前页面的指定位置
    * 可以使用mailto:来创建一个发送电子邮件的超链接
   * target
        * 指定在哪个窗口中打开链接
        * 可选值
          * 默认值，默认在当前窗口打开链接 self
          * 在新窗口中打开链接 blank
          * 内联框架的name属性值 在指定的内联框架中打开链接

### 文本标签
`
<em> 表示语气上的强调
`

`
<strong> 表示内容的重要性
`

`
<i> 表示单纯的斜体
`

`
<b> 表示单纯的加粗
`

`
<small> 表示细则一类的内容
`

`
<cite> 表示参考的内容，凡是加书名号的都可以使用cite
`

`
<q> 短引用，行内引用
`

`
<sup> 上标
`

`
<sub> 下标
`

`
<del> 删除的内容
`

`
<ins> 插入的内容
`
### 图片标签
* img
* 使用图片标签可以向页面中引入一个外部图片
* 属性
    * src 指向一个外部图片的路径，可以使用相对路径
    * alt
        * 指定一个在图片无法加载时对图片的描述
        * 搜索引擎主要通过该属性来识别图片的内容
        * 如果不写该属性则搜索引擎会对图片进行收录
     * width 设置图片的宽度
     * height 设置图片的高度
 * 图片的格式
    * JPEG 颜色丰富的图片，如，照片
    * GIF 颜色单一，简单透明的图片，动态图
    * PNG 颜色丰富，复杂透明的图片
    * 图片选择的原则
        * 效果一致，用小的
        * 效果不一致，用效果好的
### 列表
* 无序列表
    * 使用ul来创建一个无序列表，在列表中使用li来表示一个列表项
    * 无序列表使用符号作为项目符号
* 有序列表
    * 使用ol来创建一个无序列表，在列表中使用li来表示一个列表项
    * 使用有序的序号作为项目符号
* 定义列表
* 使用dl来创建一个定义列表
    * dt 表示标题
    * dd 表示描述
* 列表相关的元素都是块元素，他们之间可以互相嵌套
* 去除项目符号 list-style:none
### 属性
* 通过属性可以设置标签的效果
* 属性需要定义在开始标签中或这自结束标签中
* 属性实际上是一组一组名值对结构
* 例子：
    * <标签名 属性名="属性值" 属性名="属性值"></标签名>
    * <标签名 属性名="属性值" 属性名="属性值" />
### 实体
* 在HTML页面中一些特殊符号是不能直接使用，需要使用实体来代替这些特殊符号
* 实体也可以称为转义字符
* 实体的语法 &实体名;
* 常用的实体
    * 空格 &nbsp;
    * < &lt;
    * > &gt;
    * 版权符号 &copy;
### 相对路径
* 相对于当前资源所在的目录的路径
* 可以使用../返回一级目录，返回几级使用几个../
### 注释
* 语法 <!-- 注释内容 -->
* 注释中的内容不会在页面中显示，但是会在源码中显示，我们可以通过注释来说明网页的代码
* 也可以通过注释隐藏一些页面中不想显示的内容
### xHtml语法规范
* 1.HTML中不区分大小写，但是尽量使用小写
* 2.HTML的注释不能嵌套
* 3.标签必须结构完整
  * 要么成对出现
  * 要么自结束标签
* 4.标签可以嵌套但是不能交叉嵌套
* 5.属性必须有值，且值必须加引号，单引号双引号都可以
