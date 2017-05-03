# for...in循环

标签（空格分隔）： js

---
>**语法：for(var key in obj){ };**

 - key:obj这个对象的每一个key
 - obj[key]就代表每一个value值
```
var obj={'a':1,'matrix':2,'x':'abc',fn:function(){console.log(1);}};
for(var key in obj){
console.log(`${key}:${obj[key]}`)
};
```

