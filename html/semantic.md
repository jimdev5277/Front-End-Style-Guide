# 语义化
没有 `CSS` 的 `HTML` 是一个语义系统而不是 UI 系统。

通常情况下，每个标签都是有语义的，所谓语义就是你的衣服分为外套， 裤子，裙子，内裤等，各自有对应的功能和含义。所以你总不能把内裤套在脖子上吧。-- 一丝

此外语义化的 `HTML` 结构，有助于机器（搜索引擎）理解，另一方面多人协作时，能迅速了解开发者意图。

#### 常见标签语义

| 标签 | 语义 |
| -- | -- |
| `<p>` | 段落 |
| `<h1> <h2> <h3> ...` | 标题 |
| `<ul>` | 无序列表 |
| `<ol>` | 有序列表 |
| `<blockquote>` | 大段引用 |
| `<cite>` | 一般引用 |
| `<b>` | 为样式加粗而加粗 |
| `<strong>` | 为强调内容而加粗 |
| `<i>` | 为样式倾斜而倾斜 |
| `<em>` | 为强调内容而倾斜 |
| `code` | 代码标识 |
| `abbr` | 缩写 |
**html5元素**

>* section 表示文档中的节、区段，可以和h1-h6一起来显示文档结构
* article 表示一块比较独立的内容或者主题内容，块级元素，比如blog的内容，报纸的文章
* aside 表示article以外的内容，而且应该和article有一定的关系，块级元素
* hgroup 表示一个文档、区段(section)的标题组合
* header 表示页眉,页头
* footer 表示页脚
* nav 表示导航内容
* figure 表示以相对独立的或外引的元素，如img video
* figcaption 表示 figure内容的标题
```
  :::html
  <!-- hgroup 示例 -->
  <hgroup>
  <h1>文档主标题</h1>
  <h2>文档副标题</h2>
  </hgroup>
  <!-- figure 示例 -->
  <figure>
   <video src="ogg"></video>
   <figcaption>Example</figcaption>
  </figure>
  <figure>
   <img src="img" alt="Example image" />
   <figcaption>Example image</figcaption>
  </figure>
  ```

**结构性元素**

>* p 表示段落。只能包含内联元素，不能包含块级元素;
* div 本身无特殊含义，可用于布局。几乎可以包含任何元素;
* br 表示换行符;
* hr 表示水平分割线;
* h1-h6 表示标题。其中 h1 用于表示当前页面最重要的内容的标题;
* blockquote 表示引用，可以包含多个段落。请勿纯粹为了缩进而使用 blockquote，大部分浏览器默认将 blockquote 渲染为带有左右缩进;
* pre 表示一段格式化好的文本;

**头部元素**

>* title 每个页面必须有且仅有一个 title 元素;
* base 可用场景：首页、频道等大部分链接都为新窗口打开的页面;
* link link 用于引入 css 资源时，可省去 media(默认为all) 和  
type(默认为text/css) 属性;
* style type 默认为 text/css，可以省去;
* script type 属性可以省去; 不赞成使用lang属性; 不要使用古老的<!– //–>这种hack脚本, 它用于阻止第一代浏览器（Netscape 1和Mosaic）将脚本显示成文字;
* noscript 在用户代理不支持 JavaScript 的情况下提供说明;

**文本元素**

>* a a 存在 href 属性时表示链接，无 href 属性但有 name 属性表示锚点;
* em,strong em 表示句意强调，加与不加会引起语义变化，可用于表示不同的心情或语调; strong 表示重要性强调，可用于局部或全局，strong强调的是重要性，不会改变句意;
* abbr 表示缩写;
* sub,sup 主要用于数学和化学公式，sup还可用于脚注;
* span 本身无特殊含义;
* ins,del 分别表示从文档中增加(插入)和删除

**媒体元素**

>* img 请勿将img元素作为定位布局的工具，不要用他显示空白图片; 必要时给img元素增加alt属性;
* object 可以用来插入Flash;
**列表元素**

>* dl 表示关联列表，dd是对dt的解释; dt和dd的对应关系比较随意：一个dt对应多个dd、多个dt对应一个dd、多个dt对应多个dd，都合法; 可用于名词/单词解释、日程列表、站点目录;
* ul 表示无序列表;
* ol 表示有序列表, 可用于排行榜等;
* li 表示列表项，必须是ul/ol的子元素;
**表单元素**

>* 推荐使用 button 代替 input，但必须声明 type;
* 表单元素的 name 不能设定为 action, enctype, method, novalidate, target, submit 会导致表单提交混乱

### 示例
将你构建的页面当作一本书，将标签的语义对应的其功能和含义；
* 书的名称：`<h1>`
* 书的每个章节标题: `<h2>`
* 章节内的文章标题: `<h3>`
* 小标题/副标题: `<h4> <h5> <h6>`
* 章节的段落: `<p>`

更多语义化的内容，参考 sofish 写的文章 [这样去写你的 HTML](http://wenku.baidu.com/view/0a8d3774f242336c1eb95ea9.html)。
