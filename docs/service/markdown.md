# markdown语法

!> 基础语法 详见表格：

|语法|含义|效果|
|-|-|-|
|# h1<br>## h2<br>### h3<br>...<br>###### h6|h1~h6标题| |
|>>> 请问 Markdwon 怎么用？<br>>> 自己看教程！<br>> 教程在哪？|文字引用-blockquote| <blockquote><blockquote><blockquote>请问 Markdwon 怎么用？</blockquote></blockquote></blockquote><blockquote><blockquote>自己看教程！</blockquote></blockquote><blockquote> 教程在哪？</blockquote>|
| * 无序列表项 一<br>+ 无序列表项 二<br>- 无序列表项 三|无序列表-ul li| <ul><li>天气非常不错</li><li>无聊的人聊天气</li></ul> |
|1. 有序列表项 一<br>2. 有序列表项 二<br>3. 有序列表项 三|有序列表-ol li| <ol><li>这是什么？</li><li>有序列表呀</li></ol> |
|\`code\`|行内代码块|`.code`|
| `![alt](url "title")`|插入图片|<div style="width:50px;height:50px">![图片演示](../idea.svg "我是标题")</div>|
|`[name](url "title")`|插入链接|[我的博客](http://lee.cm "jim")|
|`[name][var]`<br>`[var]:url "title"` |插入链接 (变量调用)|[我的博客](http://lee.cm "jim")|
|`<url>`|插入链接 (自动)|<http://lee.cm>|
| \ | 防止代码被转义 |\`我没有被解析\`|
| * * * <br> &#42;&#42;&#42; <br> &#42;&#42;&#42;&#42;&#42; <br>- - -<br>-----------|分割线-hr|<hr>|
|文本末尾两个空格或另起空行|换行||
|`:emoji:`|emoji表情，也可以直接插入可视表情<br>[查看emoji表情码](https://www.webfx.com/tools/emoji-cheat-sheet/)|🏖 ✔️ 💯 🍿 🍩 🧚‍♂️|
|`*斜体*`<br>`_斜体_`|斜体字|_我是斜体字_|
|`**粗体**`<br>`__粗体__`|粗体字|__我是粗体字__|
|`***粗斜体***`<br>`___粗斜体___`|粗斜体字|***我是粗斜体***|
|`~~删除线~~`|删除体字|~~我是删除体~~|
|&#124;标题1&#124;标题2&#124;标题3&#124;<br>&#124;:--&#124;:--:&#124;--:&#124;<br>&#124;左对齐&#124;居中&#124;右对齐&#124;|表格<br>[表格生成器](https://www.tablesgenerator.com/markdown_tables)|<table><thead><tr><th align="left">th1</th><th align="center">th2</th><th align="right">th3</th></tr></thead><tbody><tr><td align="left">左对齐</td><td align="center">居中</td><td align="right">右对齐</td></tr></tbody></table>|










