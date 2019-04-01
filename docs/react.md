# React

1. 列举React的生命周期，什么阶段可以使用setState ？  
答案：  
在客户端被实例化时
  * getDefaultProps，对于组建类只调用一次
  2. getInitialState，每个组件只调用一次
  3. ComponentWillMount
  4. render
  5. componentDidMount，在服务端被实例化时不会调用  

  存在期，交互时发生状态改变
  * componentWillRecieveProps
  2. shouldComponentUpdate
  3. componentWillUpdate，不能更新props或state
  4. render
  5. componentDidUpdate 
 
  销毁时
  * componentWillUnmount

*[Back to Contents](../README.md)*
