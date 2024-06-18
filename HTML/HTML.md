# HTML

## HTML基础知识

### 第一部分 基础知识

#### 1.1 标签的分类

1. 按照标签的结构分类
   - 围堵标签：`<标签>内容</标签>`
   - 自闭合标签：`<标签>`

2. 按照标签效果分类
   - 行内标签：标签不会独占一行，会和其他标签共享一行。
   - 块级标签：标签会独占一行，不会和其他标签共享一行。

#### 1.2 标签嵌套规则

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


#### 1.3 基础标签

1. HTML注释
```html
<!--注释内容 -->
```
> VsCode快捷键 ctrl+/

2. P标签
```html
<p>My cat is very grumpy</p>
```
>- 使用p标签将这行文字封装成一个段落元素来使其在单独一行呈现。
>- 标签可以使大写也可以是小写。

3. em标签  `~语义化`
```html
<em>Camellia·XIAOHUA</em>
```
   - 可以被网络检索到
   - 阅读器看到em标签会改变读音。
   - i标签只有一个斜体的效果

> em元素将文本标记为强调（emphasis）格式。em元素可以嵌套，嵌套层次越深，则强调的程度越深。


4. a标签
   - herf：跳转链接
   - title：鼠标悬停，提示文字内容
   - target属性用于指定链接如何变成页面。
```html
<a href="https://camelliaxiaohua.online" title="Camellia·XIAOHUA的个人学习记录网站" target="_blank">Camellia·XIAOHUA</a>
```

5. HTML空格
 - `&nbsp;`

6. strong标签 `~语义化`
```html
<strong>Camellia.xiaohua</strong>
```
> `<b>`只有加粗效果，没有语义化

                 
#### 1.4 标签的属性
 
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
| <         | &lt;            |
| >         | &gt;            |
| “         | &quot;          |
| ‘         | &apos;          |
| &         | &amp;           |




### 第二部分 HTML基础结构

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

### 2.1 head标签

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

### 2.2 body标签

1. 标题标签：
`<h1></h1>`、`<h2></h2>`、`<h3></h3>`、`<h4></h4>`、`<h5></h5>`、`<h6></h6>`

2. 段落标签：
`<p></p>`

3. 无序列表
```html
<ul type="circle">
   <li>豆浆</li>
   <li>油条</li>
   <li>豆汁</li>
   <li>焦圈</li>
</ul>
```
<blockquote style="border-left: 4px solid #e74c3c; background-color: #f8d7da; padding: 10px;">
    <p><strong>⚠️ 警告：</strong>不要使用type属性，它已经被弃用了。请使用 CSS list-style-type 属性作为代替。</p>
</blockquote>

> <a href="https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/ul">点击查看详情</a>

4. 有序列表
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


## 2.3 超链接标签

1. 块级链接
任何内容，甚至块级内容都可以作为显示链接。如果想让标题内容变为链接，就把它包裹在锚点内容（<a>）内，像这个代码段一样：
```html
<a href="https://developer.mozilla.org/zh-CN/">
  <h1>MDN Web 文档</h1>
</a>
<p>自从 2005 年起，就开始记载包括 CSS、HTML、JavaScript 等网络技术。</p>
```

2. 图片链接
如果需要链接的图片，使用<a>全文来概括要链接的<img>。
```html
<a href="https://developer.mozilla.org/zh-CN/">
  <img src="mdn_logo.svg" alt="MDN Web 文档主页" />
</a>
```
3. title：鼠标悬停，提示文字内容

4. target属性用于指定链接如何变成页面。