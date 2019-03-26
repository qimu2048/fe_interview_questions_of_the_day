# Short Program Test

1. 一个无限长的数字序列 1,  2，3，3，4，4，4,  5，5，5，5，5 ...,(已知此数列有一定规律，现将这些数字按不同数值堆叠，相同值的数字在同一层)。  
这个数字序列的第n个数所在的那一层之前的所有层里共有多少个数?
> 答案：  
```javascript
function arrSum(n) {
  var arr = new Array();
  arr[0] = 1;
  arr[1] = 1;
  var sum = arr[0] + arr[1];
  for (var i=2;;i++) {
    arr[i] = arr[i-1] + arr[i-2];
    sum += arr[i];
    if(sum >= n) {
      return sum - arr[i];
    }
  }
}
console.log(arrSum(6)); //输出4
```

*[Back to Contents](../README.md)*
