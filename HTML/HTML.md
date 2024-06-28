# HTML


## 1. **HTML基础**

### 1.1 **简介与历史**

  - 什么是HTML？
  - HTML的发展历史
  - HTML版本概述

### 1.2 **基本结构**


#### HTML文档结构：`<html>`, `<head>`, `<body>`

```html
  <!DOCTYPE html>
<html>
    <head>
        <title> </title>
    </head>
    <body>
        
    </body>
</html>
```



#### **标签的分类**

1. 按照标签的结构分类
   - 围堵标签：`<标签>内容</标签>`
   - 自闭合标签：`<标签>`

2. 按照标签效果分类
   - 行内标签：标签不会独占一行，会和其他标签共享一行。
   - 块级标签：标签会独占一行，不会和其他标签共享一行。



#### **标签嵌套规则**

- 嵌套:一个标签（围堵）中可以写另一个标签

1. 块级标签可以嵌套块级
```html
<p>
   <hr>
   Camellia
   <hr>
</p>
```

2. 块级标签可以嵌套行内
```html
<p>
   <em>Camellia</em><em>·XIAOHUA</em>
</p>
```

3. 行内标签可以嵌套行内
```html
<p>
<em><strong>Camellia·XIAOHUA</strong></em>
</p>
```
>注意：要嵌套闭合

4. 行内标签不能嵌套块级
> 行内嵌套块级，行内会失效。


#### **标签的属性**

1. 属性必须包含
   - 一个空格，它在属性和元素名称之间。如果一个元素具有多个属性，则每个属性之间必须由空格分隔。
   - 属性名称，后面跟着一个等于号。
   - 一个属性值，由一对引号（""）引起来。

2. 布尔属性

   ```html
   <input type="text" disabled="disabled">请输入验证码
   <!-- 可以直接将disabled的值省略。 -->
   <input type="text" disabled>请输入验证码
   ```
   > 建议不要省略

3. 省略属性值引号用法

   ```html
   <a href=https://camelliaxiaohua.online>Camellia·XIAOHUA</a>
   ```

   > 不要省略，因为在判断多个属性用空格隔开的时候会判断混乱。
   > <a href=https://camelliaxiaohua.online title=camellia xiao hua>Camellia·XIAOHUA</a>

4. 属性的单引号与双引号
   - 单引号和双引号均可，但应该注意单引号和双引号不能在一个属性值里面混用。
   
     ```html
     <a href="https://camelliaxiaohua.online'>Camellia·XIAOHUA</a>
     ```
   - 不同引号可以嵌套，相同的不可以嵌套。
   
   
   
5. 实体引用：在HTML中包含特殊字符

| 原义字符 | 等价字符引用 |
|-----------|-----------------|
| <         | `&lt;`            |
| >         | `&gt;`            |
| “         | `&quot;`          |
| ‘         | `&apos;`          |
| &         | `&amp;`           |



#### 元数据：`<meta>`, `<title>`, `<link>`

1. title标签：展示网页标题内容

2. meta标签：

   - 设置编码集：

     - ascii、gbk、**utf-8**

     ```html
     <meta charset="utf-8" />
     ```

   - 作者信息设置：

     - name属性：作者
     - content属性：作者信息

     ```html
     <meta name="Camellia·XIAOHUA" content="camelliaxiaohua.online"/>
     ```

   - meta标签关键词(keywords)设置

     - name属性：keywords
     - content属性：关键字、关键字...

     ```html
     <meta name="keywords" content="Camellia,Java,前端,后端"/>
     ```

   - meta标签的描述(description)设置

     - name属性：description
     - content属性：描述信息

     ```html
     <meta name="description" content="一个前端学习仓库" />
     ```

#### **文本内容**

1. 标题标签：`<h1>` 到 `<h6>`

   ```html
   <h1></h1> <h2></h2> <h3></h3> <h4></h4> <h5></h5> <h6></h6> 
   ```

2. 段落标签：`<p></p>`

   ```html
   <p>My cat is very grumpy</p>
   ```
   >- 使用p标签将这行文字封装成一个段落元素来使其在单独一行呈现。
   >- 标签可以使大写也可以是小写。

3. 换行标签：`<br>`

4. 水平线标签：`<hr>`

5. 字体样式：`<strong>`, `<em>`, `<b>`, `<i>`

6. HTML注释

   ```html
   <!--注释内容 -->
   ```
   > VsCode快捷键 ctrl+/

7. em标签  `~语义化`

   ```html
   <em>Camellia·XIAOHUA</em>
   ```
   - 可以被网络检索到
   - 阅读器看到em标签会改变读音。
   - i标签只有一个斜体的效果

   > em元素将文本标记为强调（emphasis）格式。em元素可以嵌套，嵌套层次越深，则强调的程度越深。

8. a标签

- herf：跳转链接
- title：鼠标悬停，提示文字内容
- target属性用于指定链接如何变成页面。

   ```html
   <a href="https://camelliaxiaohua.online" title="Camellia·XIAOHUA的个人学习记录网站" target="_blank">Camellia·XIAOHUA</a>
   ```

9. HTML空格

- `&nbsp;`

10. strong标签 `~语义化`

    ```html
    <strong>Camellia.xiaohua</strong>
    ```
    > `<b>`只有加粗效果，没有语义化

#### **HTML元素**

1. **列表**
  
  - 无序列表：`<ul>`, `<li>`
    ```html
    <ul type="circle">
       <li>豆浆</li>
       <li>油条</li>
       <li>豆汁</li>
       <li>焦圈</li>
    </ul>
    ```
    > [!WARNING]
    >
    > 警告：不要使用type属性，它已经被弃用了。请使用 CSS list-style-type 属性作为代替。
    > <a href="https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/ul">点击查看详情</a>
  

  - 有序列表：`<ol>`, `<li>`
    - type:
          - a 表示小写英文字母编号
          - A 表示大写英文字母编号
          - i 表示小写罗马数字编号
          - I 表示大写罗马数字编号
          - 1 表示数字编号（默认）编号类型适用于整个列表，除非在 <ol> 元素的 <li> 元素中使用不同的 type 属性。
    ```html
    <ol type="A">
       <li>沿这条路走到头</li>
       <li>右转</li>
       <li>直行穿过第一个十字路口</li>
       <li>在第三个十字路口处左转</li>
       <li>继续走 300 米，学校就在你的右手边</li>
    </ol>
    ```
    > <a href="https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/ol">点击查看详情</a>
  - 描述列表：`<dl>`, `<dt>`, `<dd>`
  

2. **链接**
  
  - 超链接：`<a>`
    任何内容，甚至块级内容都可以作为显示链接。如果想让标题内容变为链接，就把它包裹在锚点内容（<a>）内：

   ```html
   <a href="https://developer.mozilla.org/zh-CN/">
   <h1>MDN Web 文档</h1>
   </a>
   <p>自从 2005 年起，就开始记载包括 CSS、HTML、JavaScript 等网络技术。</p>
   ```
  - 锚点：内部链接与外部链接
  
3. **图像**

  - 插入图像：`<img>`
  - 如果需要链接的图片，使用<a>全文来概括要链接的<img>。
   ```html
    <a href="https://developer.mozilla.org/zh-CN/">
      <img src="mdn_logo.svg" alt="MDN Web 文档主页" />
     </a>
   ```
   - 图像属性：
     - title：鼠标悬停，提示文字内容
     - target属性用于指定链接如何变成页面
     - width：宽度
     - height：高度
   - **插入本地图片**：
   ```html
    <img src="images/dinosaur.jpg" alt="恐龙" />
   ```
  
   - **插入网络图片**：
   ```html
   <img src="images/dinosaur.jpg" alt="恐龙" />
   ```
>不建议使用绝对 URL 进行链接。你需要托管你想要在网站上使用的图像，在比较简单的情况下，通常我们会把网站的图像保存在与 HTML 相同的服务器上。此外，从维护的角度来说，使用相对 URL 比绝对 URL 更有效率（当你将网站迁移到不同的域名时，你不需要更新所有 URL，使其包含新域名）。在更高级的设置中，你可能会使用内容分发网络（CDN）来传递图像。

#### 相对路径和绝对路径

1. 相对路径引用
   - `./`表示当前目录（默认，可以省略）
      1. 页面引用平级目录下的图片
      2. 页面引用平级目录文件夹下的图片
   - `../`页面引用上一级目录文件夹下的图片

2. 绝对路径引用

#### **表格**

1. 表格基础标签
   - `<table>`：定义表格的开始和结束。
   - `<tr>（table row）`：定义表格中的一行。
   - `<th>（table header）`：定义表头单元格，通常显示为加粗居中的文本。
   - `<td>（table data）`：定义表格中的标准单元格。
   - `<caption>`：标签为表格添加标题。

2. 表格的样式标签
   - border：设置表格的边框。
   - cellspacing：设置表格之间边框的距离。
   - cellpadding：指定表格单元格内容与单元格边框之间的空白（内边距）。
   - align：用于设置表格内容的对齐方式，包括水平对齐和垂直对齐。
   - bgcolor：设置表格的背景颜色。

   ```html
   <table border="1px" cellspacing="0" cellpadding="20px" align="center">
        <caption>User Information Table</caption>
        <tr bgcolor="pink" align="center">
            <th>name</th>
            <th>age</th>
            <th>city</th>
            <th>job</th>
        </tr>
        <tr align="center">
            <td>Camellia</td>
            <td>23</td>
            <td>杭州</td>
            <td>Java工程师</td>
        </tr>
        <tr align="center">
            <td>XIAOHUA</td>
            <td>22</td>
            <td>南京</td>
            <td>PHP工程师</td>
        </tr>
        <tr align="center">
            <td>HAHA</td>
            <td>27</td>
            <td>上海</td>
            <td>算法工程师</td>
        </tr>
    </table>
   ```
3. 表格的跨行/跨列合并

   - 跨列操作：保留左边的td,删掉右边的td,让左边的td合并右边的td colspan="2"

   - ```html
     <table border="1px" cellspacing="0" cellpadding="10px" align="center">
             <tr>
                 <th>姓名</th>
                 <th colspan="2">手机号</th>
             </tr>
     
             <tr>
                 <td>张三</td>
                 <td>135xxx</td>
                 <td>138xxx</td>
             </tr>
     
             <tr>
                 <td>李四</td>
                 <td>131xxx</td>
                 <td>199xxx</td>
             </tr>
         </table>
     ```

   - 跨行操作：保留上面的td,删掉下面的td,让上面的td合并下面的td rowspan="2"

   - ```html
     <table border="1px" cellspacing="0" cellpadding="10px" align="center">
             <tr>
                 <th>姓名</th>
                 <td>Camellia</td>
                 <td>XIAOHUA</td>
             </tr>
             <tr>
                 <th rowspan="2">手机号</th>
                 <td>132xxx</td>
                 <td>3214xxx</td>
             </tr>
             <tr>
                 <td>136xxx</td>
                 <td>167xxx</td>
             </tr>
         </table>
     ```

#### **表单与输入**

##### 表单的基本结构

<form action="URL" method="post">
    <input type="text" name="username">
    <input type="submit" value="提交">
</form>


##### 表单的主要属性

1. **action**：
   - 描述：定义表单提交的目标URL，通常是一个服务器端脚本或程序（如Servlet、PHP、ASP等）。
   - 示例：`action="/submit"`

2. **method**：
   - 描述：指定表单数据的提交方式，有两种常用的方式：
     - `GET`：通过URL参数传递数据，适合提交非敏感数据，数据长度有限制。
     - `POST`：通过HTTP请求体传递数据，适合提交敏感数据和大数据量。
   - 示例：`method="post"`

##### 表单验证

为了确保用户输入的有效性，可以使用HTML5的内置验证功能或JavaScript进行表单验证。HTML5提供了一些内置的验证属性，如`required`、`pattern`、`min`、`max`等，可以帮助开发者进行简单的表单验证。

##### 输入控件

1. **文本框 (Text Field)**：
   - **描述**：文本框是一个单行输入框，用户可以在其中输入文本。常用于获取简单的输入，如用户名、电子邮件地址等。
   - **HTML标签**：`<input type="text">`
   - **示例**：
     ```html
     <label for="username">用户名:</label>
     <input type="text" id="username" name="username">
     ```

2. **密码框 (Password Field)**：
   - **描述**：密码框也是一个单行输入框，但与文本框不同的是，用户输入的内容会被隐藏（通常显示为点或星号），用于输入密码。
   - **HTML标签**：`<input type="password">`
   - **示例**：
     ```html
     <label for="password">密码:</label>
     <input type="password" id="password" name="password">
     ```

3. **文本域 (Text Area)**：
   - **描述**：文本域是一个多行输入框，用户可以在其中输入较长的文本内容。常用于获取用户的评论、反馈或描述等。
   - **HTML标签**：`<textarea>`
   - **示例**：
     ```html
     <label for="comments">评论:</label>
     <textarea id="comments" name="comments" rows="4" cols="50"></textarea>
     ```

##### 单选择控件


HTML 中的单选控件是通过 <input> 元素的 type="radio" 属性实现的。单选控件允许用户从一组互斥的选项中选择一个。
1. **HTML 结构**：
   ```html
   <form action="#" method="get">
      男 <input type="radio" name="sex" value="1" checked="checked">
      女 <input type="radio" name="sex" value="2">
      <input type="submit" value="提交数据">
   </form>
   ```

   - `<input type="radio">` 定义了单选按钮。
   - `name` 属性用于将单选按钮分组，确保它们互斥地工作。
   - `value` 属性定义了每个选项的值。
   - `checked="checked"`属性表示默认选中。

2. **特点和行为**：
   - 用户只能选择单选按钮组中的一个选项。
   - 单选按钮组中的每个选项都应该具有相同的 `name` 属性值，以确保它们是互斥的。

##### 复选控件

HTML 中的复选控件通过 `<input>` 元素的 `type="checkbox"` 属性实现，允许用户从多个选项中选择多个或全部选项。
1. **HTML 结构**：
   ```html
    <form action="#" method="get">
        爱好：听歌<input type="checkbox" name="hobby" value="1" checked>
        水博客<input type="checkbox" name="hobby" value="2">
        追剧 <input type="checkbox" name="hobby" value="3">

        <br>阅读并同意规范<input type="checkbox" name="isAgree" value="1">
        <br> <input type="submit" value="提价数据">
    </form>
   ```

   - `<input type="checkbox">` 定义了复选框。
   - `name` 属性用于将复选框分组，以便在表单提交时能够收集选中的值。
   - `value` 属性定义了每个选项的值。

2. **特点和行为**：
   - 用户可以从多个复选框中选择一个或多个选项。
   - 复选框之间的选择是独立的，即用户可以同时选择多个选项。


#### 4. **HTML5新特性**
- **语义化标签**
  - 结构标签：`<header>`, `<nav>`, `<section>`, `<article>`, `<footer>`, `<aside>`, `<main>`
- **多媒体标签**
  - 音频：`<audio>`
  - 视频：`<video>`
  - 嵌入：`<embed>`, `<object>`, `<iframe>`
- **图形与绘图**
  - 画布：`<canvas>`
  - 矢量图形：`<svg>`
- **其他新特性**
  - 数据存储：`localStorage`, `sessionStorage`
  - 离线支持：`<application>`, `cache manifest`
  - 拖放API：Drag and Drop

#### 5. **高级主题**
- **响应式设计**
  - 响应式布局概念
  - 媒体查询：`@media`
  - 流式布局与栅格系统
- **HTML与CSS的结合**
  - 内联样式与嵌入样式
  - 外部样式表的链接：`<link>`
  - 常用CSS属性：颜色，背景，边框，文本，布局
- **HTML与JavaScript的结合**
  - 在HTML中嵌入JavaScript：`<script>`
  - 事件处理：`onclick`, `onchange`, `onsubmit`, 等
  - DOM操作：获取元素，修改内容，样式

#### 6. **实践与项目**
- **创建简单的静态网页**
  - 个人简历页面
  - 产品展示页面
  - 博客模板
- **综合项目**
  - 完整的网站项目
  - 使用HTML、CSS和JavaScript实现交互式网页
  - 响应式设计项目

### 学习资源
- **在线教程**
  - W3Schools
  - MDN Web Docs
  - freeCodeCamp
- **书籍**
  - 《HTML and CSS: Design and Build Websites》 by Jon Duckett
  - 《Learning Web Design》 by Jennifer Robbins
- **视频课程**
  - Coursera, edX, Udemy, YouTube
- **开发工具**
  - 浏览器开发者工具
  - 代码编辑器：Visual Studio Code, Sublime Text, Atom

通过上述学习结构，你可以系统地掌握HTML的基础知识和高级应用，逐步提升自己的网页开发技能。

