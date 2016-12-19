## 对象基本操作
  * 键名
  * delete
  * 生成方法
  * 属性
  * 对象的引用
  * in运算符
  * for…in循环
参考资料：http://javascript.ruanyifeng.com/grammar/object.html#toc1

## 面向对象

```
  面向对象

  (function(){


  }())
```

```
function people(name){
  this._name = name;
}
people.prototype.say = function(){
  alert("peo-Hello" + this._name)
}

function student(){

}
student.prototype = new people();

var fathersay = people.prototype.say;

student.prototype.say = function(){
  fathersay.call(this);
  alert('stu-hello'+this._name);
}
var s = new fathersay("ljy");
s.say();
```

```
  (function(){
      var n = 'ljy';
      function Person(name){
        var _this = {};
          _this._name = name;
          _this.sayHello = function(){
            alert("Phello")+_this._name+n
          }
          return _this;
      }
      window.Person = Person
  }())

  (function(){
      function Teacher(name){
        var _this = Person(name);
        var superSay = _this.sayHello;
        _this.sayHello = function(){
          superSay.call(_this);
          alert("Thello"+_this._name)
        }
        return _this;
      }
  }())

  var t = Teacher("ljy")
  t.sayHello();
```
