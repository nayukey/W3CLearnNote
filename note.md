阅读笔记第一节-Document

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





