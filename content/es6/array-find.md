ES6 对数组的扩展中，有 find() 这个方法。用于找出第一个符合条件的数组成员。

find() 中传入的参数是什么呢？是一个函数，当一个函数被作为其他函数的参数的时候，这个函数就叫做一个回调函数 （ callback function )。
```js
let data = [1, 5, 10, 15].find(value => value > 9) // 10

console.log(data)
```
上面，回调函数发挥的作用是判断条件。
