- - 以下是对你的HTML笔记内容进行优化后的版本，使其结构更清晰，避免了重复信息：

    # HTML

    ## HTML基础知识

    ### 第一部分 基础知识

    #### 1.1 标签的分类

    - **标签的结构分类**：
      - **围堵标签**：`<标签>内容</标签>`
      - **自闭合标签**：`<标签 />`

    - **标签效果分类**：
      - **行内标签**：不会独占一行，与其他标签共享一行。
      - **块级标签**：会独占一行，不与其他标签共享一行。

    #### 1.2 标签嵌套规则

    - **嵌套示例**：
      - 块级标签可以嵌套其他块级标签：
        ```html
        <p>
           <hr>
           Camellia
           <hr>
        </p>
        ```
      - 块级标签可以嵌套行内标签：
        ```html
        <p>
           <em>Camellia</em><em>·XIAOHUA</em>
        </p>
        ```
      - 行内标签可以嵌套行内标签：
        ```html
        <p>
          <em><strong>Camellia·XIAOHUA</strong></em>
        </p>
        ```
      - 行内标签不能嵌套块级标签。

    > 注意：嵌套时要确保标签正确闭合。

    #### 1.3 基础标签

    - **HTML注释**：
      ```html
      <!--注释内容 -->
      ```

    - **`<p>`标签**：
      ```html
      <p>My cat is very grumpy</p>
      ```
      - 用于定义段落。

    - **`<em>`标签**（语义化）：
      ```html
      <em>Camellia·XIAOHUA</em>
      ```
      - 用于强调文本。

    - **`<a>`标签**：
      - `href`：指定链接地址。
      - `title`：鼠标悬停时显示提示文本。
      - `target`：指定链接打开方式。
      ```html
      <a href="https://camelliaxiaohua.online" title="Camellia·XIAOHUA的个人学习记录网站" target="_blank">Camellia·XIAOHUA</a>
      ```

    - **HTML空格**：
      - 使用`&nbsp;`实现非断行空格。

    - **`<strong>`标签**（语义化）：
      ```html
      <strong>Camellia.xiaohua</strong>
      ```

    > `<b>`标签仅用于视觉上的加粗，没有语义意义。

    #### 1.4 标签的属性

    - **属性格式**：
      - 属性名称后应包含等号和引号，例如：`属性="值"`。
      - 推荐使用双引号。

    - **布尔属性**：
      ```html
      <input type="text" disabled="disabled">请输入验证码
      ```
      - 省略布尔属性时应小心使用。

    - **实体引用**：
      - `<`：`&lt;`
      - `>`：`&gt;`
      - `"`：`&quot;`
      - `'`：`&apos;`
      - `&`：`&amp;`

    ### 第二部分 HTML基础结构

    ```html
    <!DOCTYPE html>
    <html>
        <head>
            <title></title>
        </head>
        <body>
        </body>
    </html>
    ```

    #### 2.1 head标签

    - **`<title>`标签**：
      - 定义网页标题。

    - **`<meta>`标签**：
      - 设置编码集：
        ```html
        <meta charset="utf-8" />
        ```
      - 设置作者信息：
        ```html
        <meta name="author" content="Camellia·XIAOHUA" />
        ```
      - 设置关键词：
        ```html
        <meta name="keywords" content="Camellia, Java, 前端, 后端" />
        ```
      - 设置描述：
        ```html
        <meta name="description" content="一个前端学习仓库" />
        ```

    #### 2.2 body标签

    - **标题标签**：
      - 使用`<h1>`到`<h6>`定义标题。

    - **段落标签**：
      - 使用`<p>`定义段落。

    - **无序列表**：
      ```html
      <ul type="circle">
         <li>豆浆</li>
         <li>油条</li>
         <li>豆汁</li>
         <li>焦圈</li>
      </ul>
      ```
      > 警告：`type`属性已弃用，建议使用CSS的`list-style-type`。

    - **有序列表**：
      ```html
      <ol type="A">
         <li>沿这条路走到头</li>
         <li>右转</li>
         <li>直行穿过第一个十字路口</li>
         <li>在第三个十字路口处左转</li>
         <li>继续走 300 米，学校就在你的右手边</li>
      </ol>
      ```

    #### 2.3 超链接标签

    - **块级链接**：
      ```html
      <a href="https://developer.mozilla.org/zh-CN/">
        <h1>MDN Web 文档</h1>
      </a>
      ```

    - **图片链接**：
      ```html
      <a href="https://developer.mozilla.org/zh-CN/">
        <img src="mdn_logo.svg" alt="MDN Web 文档主页" />
      </a>
      ```

    - **`title`和`target`属性**：
      - `title`用于鼠标悬停时显示提示文本。
      - `target`指定链接打开方式。

#### 2.4 插入图片

- **插入本地图片**：
```html
<img src="images/dinosaur.jpg" alt="恐龙" />
```

- **插入网络图片**：
```html
<img src="images/dinosaur.jpg" alt="恐龙" />
```
>不建议使用绝对 URL 进行链接。你需要托管你想要在网站上使用的图像，在比较简单的情况下，通常我们会把网站的图像保存在与 HTML 相同的服务器上。此外，从维护的角度来说，使用相对 URL 比绝对 URL 更有效率（当你将网站迁移到不同的域名时，你不需要更新所有 URL，使其包含新域名）。在更高级的设置中，你可能会使用内容分发网络（CDN）来传递图像。

- **img标签属性**：
   1. alt：它的值应该是图片的文本描述，用于在图片无法显示或者因为网速慢而加载缓慢的情况下使用。
   2. title: 鼠标悬停展示提示。
   3. width：宽度
   4. height：高度
```html
<img
  src="dinosaur.jpg"
  alt="The head and torso of a dinosaur skeleton; it has a large head with long sharp teeth"
  title="A T-Rex on display in the Manchester University Museum" />
```