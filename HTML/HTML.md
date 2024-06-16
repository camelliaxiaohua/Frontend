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

3. em标签
```html
<em>Camellia·XIAOHUA</em>
```
> em元素将文本标记为强调（emphasis）格式。em元素可以嵌套，嵌套层次越深，则强调的程度越深。

4. a标签
   - herf：跳转链接
   - title：鼠标悬停，提示文字内容
   - target属性用于指定链接如何变成页面。
```html
```

5. HTML空格
 - `&nbsp;`


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


