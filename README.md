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

**Name/Value** —— 顾名思义就是一个键值对的概念，可以通过Name来得到cookie的value值。

**Expires** —— 用于设置Cookie的过期时间，比如：
Set-Cookie: id=a3fWa; Expires=Wed, 21 Oct 2015 07:28:00 GMT;
当Expires属性缺省时会默认为session，表示这是会话性cookie，值保存在客户端内存中，当浏览器关闭的时候会失效。

Max-Age —— 用于设置在Cookie失效之前需要经过的秒数，比如：
Set-Cookie: id=a3fWa; Max-Age=10; // 该cookie将在10s后失效

Max-Age的值可以为正数、负数、0。

如果为正数，浏览器会将其保存到cookie中。如果为负数，则表示该Cookie只是一各会话性Cookie，当浏览器关闭后会失效。如果为0，则会立即删除这个Cookie。

Max-Age优先级高于Expires

**Domain**

Domain指定Cookie可以送达的主机名，默认值是当前url中的主机名，如果有一个域名m.com，如果在a.m.com域名下设置一个cookie，tooken=123；如果不设值domain属性值，该Cookie是只能送达到当前主机名，如果将domain设置为m.com
