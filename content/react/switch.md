有了 exact 有些情况还是应付不来

<Route path="/about" component={About}/>
<Route path="/:user" component={User}/>
<Route component={NoMatch}/>
所以需要 switch 。

### switch 的作用

一旦上面的 Route 匹配成功，那么之后的 Route 就直接忽略。
