# [BOM](http://w3school.com.cn/jsref/index.asp)
浏览器提供的一些方法。

## 常用对象
* navigator 有关浏览器的信息
  * userAgent 用户代理的信息
  * platform 运行浏览器的操作系统平台
* histroy 浏览历史
  * lengh 返回浏览器历史列表中的 URL 数量
  * back() 加载 history 列表中的前一个 URL
  * forward() 加载 history 列表中的下一个 URL
  * go(index) 加载 history 列表中的某个具体页面
* location 当前 URL 的信息
  * href  设置或返回完整的 URL
  * hostname  设置或返回当前 URL 的主机名
  * host  设置或返回主机名和当前 URL 的端口号
  * port  设置或返回当前 URL 的端口号
  * protocol  设置或返回当前 URL 的协议
  * search  设置或返回从问号 (?) 开始的 URL（查询部分）
  * hash  设置或返回从井号 (#) 开始的 URL（锚）
  * reload()  重新加载当前文档
  * assign(url)  加载新的文档
  * replace(url)  用新的文档替换当前文档
* window
  * alert()  显示带有一段消息和一个确认按钮的警告框
  * confirm()   显示带有一段消息以及确认按钮和取消按钮的对话框
  * open()  打开一个新的浏览器窗口或查找一个已命名的窗口
  * setTimeout()  在指定的毫秒数后调用函数或计算表达式
  * setInterval()  按照指定的周期（以毫秒计）来调用函数或计算表达式
  * console  在控制台打印出信息
    * log  
    * info
    * warn
    * error
