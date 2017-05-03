#this指向和修改this指向

标签（空格分隔）： js

---
## this指向
>**定时器调用的function (){ }里面的this就是window**

```
console.log(this);  //window

document.onclick=function(){
  console.log(this);  //document
  }
  
var a=1;
function fn(){
  console.log(this.a);  
  }
  fn();  //1
  
  var obj={
  a:2,
  fn:fn
  };
  obj.fn();  //2
  
  var f=obj.fn;
  fn();  //1
  
  var obj2={
  a:2,
  css:function(){alert('css')},
  animate:function (){
  console.log(this.css);
  function inner(){
   console.log(this.a);
   }
   inner();
   }
   }
   obj2.animate();  //function(){alert('css')}   1
```
## 修改this指向

### fn.call(obj,arg1,arg2...)

 - 第一个参数obj：用来修改函数的this指向
 - 后面的参数arg1,arg2...:代表当前函数的参数
```
var obj1={a:1};
var obj2={a:2};

var a='abc';
function fn(b){
  console.log(this.a);
 // console.log(b);
 //   var _this=this;
    (function(){
      console.log(this.a);
      })();
}

var obj={a:3,fn:fn};
obj.fn();  //3 'abc'

var f=obj.fn;
f();  //'abc' 'abc'

obj.fn.call(null);  //'abc' 'abc'
obj.fn.call(obj1);  //1 'abc'

function fn(b){
  console.log(this.a);
  console.log(b);
 //   var _this=this;
    (function(){
      console.log(this.a);
      })();
}
obj.fn.call(obj2,'参数');  //2 '参数' 'abc'

fn.call(obj,'参数obj');  /3 '参数obj' 'abc'
  
```
 
