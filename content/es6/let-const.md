在老 JS 语法中，也就是 ES5 中，声明变量使用 var 。但是 ES6 中推荐使用 let 和 const 。

# var 的缺陷

var 总体来说，就是很烂。毛病有：

作用域不清晰，造成各种尴尬使用情形，具体见下面参考链接
可以重复声明，代码有错误，不容易报错出来
对应 let 和 const 就是避免这些问题。

多说一句：TS（ typeScript ）现在这么火，就是因为强类型，报错多。

# let 和 const 的区别

let 用来声明变量 。const 用来声明常量 。let 定义的变量，后续允许修改。const 定义一个变量后，一旦修改就会报错（当然，const 也不是绝对不能改的，详情见参考链接）。

# 参考

http://es6.ruanyifeng.com/#docs/let
