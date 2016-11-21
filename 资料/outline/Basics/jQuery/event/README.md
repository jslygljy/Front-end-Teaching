# 事件
## 绑定事件处理函数
### 通用写法
```
$elem.on(事件名称, 事件处理函数)
```

### 常见事件
* ready : DOM树构建完成。`$(document).ready(callback)`
* load: 页面加载完毕。 `$(document).load(callback)`
* click
* dblclick 双击
* mouseenter
* mouseleave
* mousemove
* mouseout 移出。移入子元素也会触发。
* hover 移动到元素上和移出。 等效与 mouseenter 和 mouseleave
* change 表单元素的值发生变化
* keyup
* keydown
* keypress
* focus
* blur
* ...

### 事件委托
给动态生成的元素绑定事件，需要
```
$par.on(事件名称, 委托元素, 事件处理函数)
```


## 解绑事件
### 解除某类型事件的所有事件处理函数
```
$elem.off(事件名称)
```

### 解除某类型事件的某个事件处理函数
```
$elem.off(事件名称, 要解除的事件处理函数)
```

## 脚本触发事件
```
$elem.trigger(事件名称)
```

## [事件上的常用属性](https://api.jquery.com/category/events/event-object/)
* target
* currentTarget
* relatedTarget
* pageX
* pageY
* which 按下的键值
* metaKey meta键是否被按下，在 Window 指 Windows key，在 Mac 上指 Command Key


## 阻止事件冒泡
```
event.stopPropagation();
```

## 阻止元素的默认行为
```
event.preventDefault();
```

元素的默认行为，如

* 点击a元素跳转页面
* 右击元素出现上下文菜单
* 点击表单的提交按钮会提交表单

## return false
在 jQuery 中，若在事件处理函数中 `return false`，则会阻止事件冒泡和阻止默认行为。    

注:如果不用 jQuery，在事件处理函数中 `return false` 与写法有关。如
```
elem.onclick = function(event){
    return false;// 相当与 event.preventDefault()
};

elem.addEventListener(
    'click',
    function(event){
        return false;// 什么都不做。
    },
    false
);
```

### 总结
考虑到可读性以及歧义性。尽量不要用 `return false`。

### 鼠标右击事件
方法1:
```
$elem.bind("contextmenu",function(evt){// 事件处理函数});
```

方法2:
```
$elem.mousedown(function(event) {
  switch (event.which) {
    case 1: /* 左击 */; break;
    case 2: /* 点滑轮 */; break;
    case 3: /* 右击 */; break;
  }
});
```

### 图片加载失败
```
$( "img" )
  .error(function() {
    $( this ).attr( "src", "replacement.png" );
  })
```


