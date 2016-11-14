# 使用 HTML DOM 来分配事件
* onmousedown 元素被点击时
* onmouseup 元素点击松开时
* onclick  点击完成事件
* onload 用户进入页面执行事件
* onchange 改变输入字段的内容
* onmouseover 移动元素发生的事件
* onmouseout 移动元素发生的事件


# 如何使用

* js中绑定事件
  <script>
  document.getElementById("myBtn").onclick=function(){displayDate()};
  </script>
* html中绑定事件

  onclick="displayDate()"
  onclick="this.innerHTML='hello!'"
  changetext(this)
  function changetext(id)
  {
    id.innerHTML="hello!";
  }
