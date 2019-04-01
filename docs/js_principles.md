# The Major Principles of JavaScript

### 原型和原型链
1. `prototype`属性和`__proto__`属性分别指向什么？  
答案：`prototype`指向对象的原型，`__proto__`指向对象的构造函数的原型。  
解析：`prototype`指向对象继承的原型。  
`__proto__`是一个访问器属性（具有get、set特性），返回对象的构造函数的原型。具体指可以分以下几种情况：
  1. 对象/数组字面量创建的对象，该值为`Object.prototype`或`Array.prototype`;
  2. 一个函数或内建构造器new出来的对象，该值为`Function.prototype`;
  3. 其他构造器函数new出来的对象，该值为 构造器函数的`prototype`属性。  

  由于性能影响，不建议直接修改`__proto__`属性，建议使用`Object或Reflect`的  `getPrototypeOf`或`setPrototypeOf`方法。

### this的绑定


*[Back to Contents](../README.md)*
