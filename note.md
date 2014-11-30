阅读笔记第一节-Document
-------------------------------------------------------------------------------------------------------
document.referrer 获取网页的来源页面的地址，NGINX与APACHE等服务器access.log中会记录此信息，注意若link类型设置了noreferrer属性，HTTP请求中就不会记录referrer属性，另外若从一个HTTPS的应用中跳到HTTP，也不会记录referrer属性。

document.cookie 注意若内容在sandboxed into unique origin中，cookie是不能get也不能set的。

document.lastModified 获取网页的最后修改时间，这个时间从服务端获取，若这个时间是未知的，那么将返回当前时间。

document.readyState "loading"说明内容正在加载，"complete"说明文章加载完毕，"interactive"文章已经完成解析，但是依旧在加载子资源

document.head 返回head元素

document.title 返回文章标题，有些未读的消息提醒，是通过此设置将内容展示出来，如果没有head元素，那么这个属性会被忽略

document.body 返回body元素，这里可以被set，但是这里插入的不是body或者frameset元素，就会报错

document.images 返回内容中img元素列表

document.embed/document.plugins 返回html文档中embed元素列表

document.links 返回内容中"a"和"area"元素列表

document.forms 返回内容中form元素列表

document.script 返回内容中script元素列表

document.getElementsByName(name) 返回name属性为某值的NodeList

元素，属性，属性值在HTML中都会被定义成具体的意义，这些定义会让WEB搜索引擎，展示，使用文档和应用等一大堆的用途。开发者不能使用元素，属性，属性值去做这个元素本身不存在的用户当中。

-------------------------------------------------------------------------------------------
内容的种类：Metadata content、Flow content、Sectioning content、Heading content、Phrasing content、Embedded content、Interactive content
Metadata content: 用于指定剩余其他内容的展现形式，或者创建与其他文档之间的联系
eg: base link meta noscript script style template title

Flow content: 使用在body元素中的大部分文档与应用集合在一起当为flow content
eg:a abbr address area (当是map元素的子元素时) article aside audio b bdi bdo blockquote br button canvas cite code data datalist del dfn div dl em embed fieldset figure footer form h1 h2 h3 h4 h5 h6 header hr i iframe img input ins kbd keygen label main map mark math meter nav noscript object ol output p pre progress q ruby s samp script section select small span strong sub sup svg table template textarea time u ul var video wbr text

Sectioning content: 使用在顶部或者底部的定义块，每一个sectionoing content元素潜在含有一个heading与一个outline
eg:article aside nav section

Heading content: 定义了一个部分的核心内容
eg:h1 h2 h3 h4 h5 h6

Phrasing content: 文档中的文字部分的内容
eg：a abbr area (当是map元素的子元素时) audio b bdi bdo br button canvas cite code data datalist del dfn em embed i iframe img input ins kbd keygen label map mark math meter noscript object output progress q ruby s samp script select small span strong sub sup svg template textarea time u var video wbr text

Embedded content： 是从其他的资源导入进去文档中的内容部分
eg: audio canvas embed iframe img math object svg video
------------------------------------------------------------------------------------------------------

HTML元素全局共同属性
accesskey、class、contenteditable、dir、hidden、id、lang、spellcheck、style、tabindex、title、translate

HTML元素事件处理
onabort、onblur*、oncancel、oncanplay、oncanplaythrough、onchange、onclick、oncuechange、ondblclick、ondurationchange、onemptied、onended、onerror*、onfocus*、oninput、oninvalid、onkeydown、onkeypress、onkeyup、onload*、onloadeddata、onloadedmetadata、onloadstart、onmousedown、onmouseenter、onmouseleave、onmousemove、onmouseout、onmouseover、onmouseup、onmousewheel、onpause、onplay、onplaying、onprogress、onratechange、onreset、onresize*、onscroll*、onseeked、onseeking、onselect、onshow、onstalled、onsubmit、onsuspend、ontimeupdate、ontoggle、onvolumechange、onwaiting
注意：加星号的处理，在window与htmlelements中存在不同的意义，是两种概念

id属性：id属性在文档中必须是唯一的，且至少使用一个字符来表示，这里的属性值内不能存在任何空格属性

title属性：title属性用来展示元素的介绍信息，就像一个适当的提示。在一个link上设置时，就会展示这个资源的描述信息，在一个image元素上时，就会展示这个image的说明，在一个段落中，它将表示一个脚注或者评论，在一个交互元素上，它将做为一个标签展示这个元素的用法。注意：title元素现在在很多设备的网页上不建议使用，触发提示的时候很多时候需要一个鼠标，而现在的多点触控，是不会展示这些信息的。

