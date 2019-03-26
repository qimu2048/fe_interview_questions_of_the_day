# The Basic Usage of JavaScript

1. 这段代码的输出结果是什么？
```javascript
var val = 12;
function func1() {
  console.log(val);
  var val = 20;
  console.log(val);
  )
}
func1();
```
> 答案：undefined 20   
解析：变量声明提升到func1作用域最开始，第一个console时变量未赋值。

2. 触摸事件包括哪几种？
> 答案：touchstart, touchend, touchmove, touchcancel

3. 结果不为真的表达式？  
A. null == undefined;   
B. [1,2,3].splice(1,1,1) == [2];   
C. let Mi = new Function(); Mi._proto_._proto_ == Object.prototype;   
D. "1" === true;
> 答案：BD   
解析：AD选项比较明显。B选项中，splice三个参数分别是start, deleteCount, insertElement；
以数组的形式返回被剪切掉的元素，此例中是[2]。但是数组是引用类型，[2] == [2]是false。  
C选项中，`Mi.__proto__`指向Mi的原型`Function.prototype`，
`Mi.__proto__.__proto__`指向`Function.prototype`的原型`Object.prototype`;
在js中几乎所有对象原型链的末尾都是`Object.prototype`。

4. 不属于document对象方法的是？  
A. onload  
B. querySelectorAll  
C. children  
D. ajax  
> 答案：AD  
解析：window.onload

5. 哪些功能默认支持跨域？
> 答案：image、iframe

6. 哪些事件不支持冒泡？
> 答案：scroll, blur, mouseleave

7. 关于web表单登录中图形验证码的实现，以下做法正确的是？  
A. 返回给浏览器的html代码中包含图形验证码和文本字符串,登录前客户端判断输入内容和页面中保存的内容是否一致  
B. 服务器端在返回的图片和cookie中同时包含图形验证码,登录前客户端判断输入内容和cookie保存的内容是否一致  
C. 服务器端生成验证码后一方面通过图片将验证码返回给客户端,同时在服务器端保存文本的验证码,由服务器端验证输入内容是否正确  
D. 浏览器通过识别图形验证码中的内容和用户输入的内容判断是否一致
> 答案： C  
解析：

*[Back to Contents](../README.md)*
