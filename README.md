# 前端学习知识点和常见问题
主要包括前端常见问题和解决方案，以及必备知识点
1xx --- 信息提示（临时响应）
2xx --- 成功（服务器成功接收客户端请求）
3xx --- 重定向（客户端需要采取更多操作来请求）
4xx --- 客户端错误（客户端问题）
5xx --- 服务器问题（服务器出错不能完成该请求）

常见状态码及解决方法
304 缓存Not Modified
解决方法:
IE下ajax请求是按照ip地址和请求路由进行缓存的。
① 直接请求加时间戳
② 取消缓存 前端页面禁止缓存 <META HTTP-EQUIV="pragma" CONTENT="no-cache">前端ajax禁止缓存,ajax请求的cache参数设置为false
400 Bad Request请求出现语法错误
Invalid argument privided提供了无效参数,表明header或者parameter里有无效参数
①对照字段名称，类型保证一致性
②使用stringify将前端传递的对象转化为字符串，data:JSON.stringify(param)
403 Forbidden 资源不可用（服务器理解客户端请求，但拒绝处理）
通常由于服务器上文件或目录的权限设置导致
404 Not Found 无法找到指定位置的资源（很有可能url出现了问题）
405 Method Not Allowed 请求方法(GET,POST,HEAD,Delete,PUT,TRACE等)
500 Internal Server Error 服务器遇到了意料不到的情况，不能完成客户端请求
503 Service Unavailable服务不可用
504 Gateway Timeout 网关超时
