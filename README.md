# issues
# cookies介绍

> Cookie（复数形态Cookies），类型为「小型文本文件」，指某些网站为了辨别用户身份而储存在用户本地终端上的数据。

cookie一般不超过4kb，由一个名称、一个值和其他几个用于控制Cookie有效期、安全性、适用范围的可选属性组成。

# 设置Cookie

  服务端：给响应头添加 "Set-Cookie" 字段，当浏览器接收到响应的时候会自动保存下该字段中的内容。
  客户端：浏览器可以通过document.cookie = "example=1; expires=Mon, 11 Nov 2026 07:34:46 GMT; domain=mnnuu.cn;path=/"的格式来设置cookie
  
# Cookie的属性

我们打开谷歌浏览器 开发者工具(F12) > Application > Cookies > 当前url 可以看到，cookie的属性有
| Name
| Value
| Domain
| Path
| Expires/Max-Age
| Size
| HttpOnly
| Secure
| SameSite
