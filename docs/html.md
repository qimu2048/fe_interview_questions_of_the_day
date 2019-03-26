# HTML & CSS

1. p、img、ul、form，属于行内标签的是？
> 答案：img  
解析：行内标签多个元素显示在一行，不能设置宽、高、margin、padding，包括span、a、label、strong、em、br等；  
行内块标签多个元素显示在一行，可以设置元素宽高，包括img、input等；  
块级元素，每个元素占一行，可以设置宽高，包括div、h1-6、p、form、ul、li、dt、dd等。  
可以用display: inline/inline-block/block;来转换几种元素。

2. body、dlv、footer、picture，这几个标签不存在的是？
> 答案：dlv  
解析：picture标签一般使用时包含多个source标签，指定media类型和对应srcset，以及一个img标签来占位。


### CSS
1. body、div、img、form，哪几个标签默认有padding值？
> 答案：body、img、form
解析：有默认margin的元素有h1-6、dl、dd、form(IE中)、select；  
有默认margin和padding的元素有ol、ul、textarea；  
有默认padding的元素有th、td、option。

2. 哪些参数可以作为media queries的条件？
> 答案：设备像素比、设备类型、设备高度
解析：排除设备型号。

3. 浮动会导致页面非正常显示，哪些方法可以清楚浮动？
> 答案：  
1.浮动元素末尾添加空标签`<div style="clear:both"></div>`   
2.给父元素添加clearfix类   
3.设置父元素overflow: hidden

4. 什么情况下会产生reflow回流与repaint重绘？
> 答案：浏览器合并DOM和CSSOM产生RenderTree来渲染，基本遍历一次可以完成，而table可能会花费3倍以上的时间。
回流是指RenderTree中元素尺寸、结构改变时，浏览器重新渲染部分或全部文档的现象。回流的开销较高。
可能引起的操作如浏览器窗口大小改变，元素尺寸位置改变，文字大小内容改变，激活伪类，添加删除DOM等。
重绘是指元素样式改变但不影响定位时，浏览器重新绘制该元素的现象。
可能引起重绘的操作有改变color，background，visibility等。  
补充：浏览器会优化重复的回流重绘过程，维持一个队列保存需要回流重绘的操作，把多次操作简化为一次。
在取某些值时，为了保证取值精确，会清空队列。如clientWidth、offsetWidth、scrollWidth/Height/Top/Left、width/height、
getComputedStyle()、getBoundingClientRect()等。

5. 如何避免reflow回流和repaint重绘？
> 答案：CSS方面——避免table布局，避免多层内联样式，在DOM末端改变class，动画应用在position: absolute/fixed; 元素上，
避免使用CSS表达式如calc()。   
JS方面——避免频繁操作style（直接更改class或替换style属性），避免频繁操作文档流中的DOM（先新建操作完再插入or操作display:none;的元素再显示），
有复杂动画的元素设置为position: absolute/fixed;


### HTML5
1. html5新增标签有哪些？
> 答案：  
结构性标签：section,article,aside,header,hgroup,footer,nav,figure  
表单标签：（input的新增type值）email,url,number,range,search,color,date-picker一类  
媒体标签：video,audio,embed  
其他：mark,progress,time,ruby/rt/rp,wbr,canvas,command,details,datalist,keygen

*[Back to Contents](../README.md)*
