# 通用约定

#### 标签
* 自闭合（self-closing）标签，无需闭合 ( 例如： `img` `input` `br` `hr` 等 )；
* 可选的闭合标签（closing tag），需闭合 ( 例如：`</li>` 或 `</body>` )；
* 尽量减少标签数量；

```html
<img src="images/google.png" alt="Google">
<input type="text" name="title">

<ul>
  <li>Style</li>
  <li>Guide</li>
</ul>

<!-- Not recommended -->
<span class="avatar">
  <img src="...">
</span>

<!-- Recommended -->
<img class="avatar" src="...">
```

#### Class 与 ID
* class 应以功能或内容命名，不以表现形式命名；
* class 与 id 单词字母小写，多个单词组成时，采用中划线`-`分隔；
* 使用唯一的 id 作为 Javascript hook, 同时避免创建无样式信息的 class；

```html
<!-- Not recommended -->
<div class="j-hook left contentWrapper"></div>

<!-- Recommended -->
<div id="j-hook" class="sidebar content-wrapper"></div>
```

#### 属性顺序
HTML 属性应该按照特定的顺序出现以保证易读性。
* id
* class
* name
* data-xxx
* src, for, type, href
* title, alt
* aria-xxx, role

```html
<a id="..." class="..." data-modal="toggle" href="###"></a>

<input class="form-control" type="text">

<img src="..." alt="...">
```

#### id和class命名约定

>* id 和 class 的命名基本原则: 内容优先，表现为辅。首先根据内容来命名，如:#header,#footer,.main-nav.如根据内容无法找到合适的命名，可以再结合表现进行命名，如：col-main, col-sub, col-extra,blue-box
* id 和 class 的名称一律小写，多个单词以连字符连接，如： main-wrap
* id 和 class 的名称只能出现，小写字母，数字和连字符( - )(js钩子除外)
* id 和 class 的名称尽量使用英文单词命名,如确实找不到合适的单词，可以使用拼音，如：zhidao-com
* 在不影响语意的情况下，id 和 class 的名称 可以适当使用缩写，如: col, nav, hd, bd, fd( 缩写只用来表示结构，不允许写任何样式)。不要自造缩写。
* class 对于选中命名.selected;对于hover，支持伪类使用:hover，不支持的使用 .hover，隐藏使用.hide 。
* id 和 class 的选择，如果只使用一次，使用id,如果使用多次使用class，如果需要和js交互，使用id,如果需要交互并且页面中有大量重复，请参见下一条。
* 对于作为js钩子的 id 和 class 命名规则为以”J_“开头(J,象形钩子的形状)，后面加上原应有的命名，在使用class的时候需要放在最前面。如:class="J_tab-content some-mod-content"。（注意：钩子，不允许在css中定义任何的样式效果）
* 很多浏览器会将含有这些词的作为广告拦截： ad、ads、adv、banner、sponsor、gg、guangg、guanggao等 页面中尽量避免采用以上词汇来命名。
#### 引号
属性的定义，统一使用双引号。

```html
<!-- Not recommended -->
<span id='j-hook' class=text>Google</span>

<!-- Recommended -->
<span id="j-hook" class="text">Google</span>
```

#### 嵌套
`a 不允许嵌套 div`这种约束属于语义嵌套约束，与之区别的约束还有严格嵌套约束，比如`a 不允许嵌套 a`。

严格嵌套约束在所有的浏览器下都不被允许；而语义嵌套约束，浏览器大多会容错处理，生成的文档树可能相互不太一样。

**语义嵌套约束**
* `<li>` 用于 `<ul>` 或 `<ol>` 下；
* `<dd>`, `<dt>` 用于 `<dl>` 下；
* `<thead>`, `<tbody>`, `<tfoot>`, `<tr>`, `<td>` 用于 `<table>` 下；

**严格嵌套约束**
* inline-Level 元素，仅可以包含文本或其它 inline-Level 元素;
* `<a>`里不可以嵌套交互式元素`<a>`、`<button>`、`<select>`等;
* `<p>`里不可以嵌套块级元素`<div>`、`<h1>~<h6>`、`<p>`、`<ul>/<ol>/<li>`、`<dl>/<dt>/<dd>`、`<form>`等。

更多详情，参考[WEB标准系列-HTML元素嵌套](http://www.smallni.com/element-nesting/)

#### 布尔值属性
HTML5 规范中 `disabled`、`checked`、`selected` 等属性不用设置值。
```html
<input type="text" disabled>

<input type="checkbox" value="1" checked>

<select>
  <option value="1" selected>1</option>
</select>
```

### 图片规范

1. 图片格式仅限于gif || png || jpg;
2. 命名全部用小写英文字母 || 数字 || _ 的组合，其中不得包含汉字 || 空格 || 特殊字符；尽量用易懂的词汇, 便于团队其他成员理 解; 另, 命名分头尾两部分, 用下划线隔开, 比如ad_left01.gif || btn_submit.gif;
3. 在保证视觉效果的情况下选择最小的图片格式与图片质量, 以减少加载时间;
4. 尽量避免使用半透明的png图片(若使用, 请参考css规范相关说明);
5. 运用css sprite技术集中小的背景图或图标, 减小页面http请求, 但注意, 请务必在对应的sprite psd源图中划参考线, 并保存至img目录下.注释规范

### 注释规范

html注释: 注释格式 , 只能在注释的始末位置,不可置入注释文字区域;
<!-- 头部 -->  <!-- //头部 -->包围，请务必要分开注释的文字（即注释文字中加空格
