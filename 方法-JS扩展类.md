### 网络操作

1. **`ajax(url: Any): String?`**
   - **参数**: `url` - 目标请求的URL，可以是单个字符串或列表。
   - **功能**: 发送网络请求并返回响应的字符串内容。

2. **`ajaxAll(urlList: Array<String>): Array<StrResponse?>`**
   - **参数**: `urlList` - URL数组。
   - **功能**: 并发发送多个网络请求，并返回响应数组。

3. **`connect(urlStr: String): StrResponse`**
   - **参数**: `urlStr` - 请求的URL。
   - **功能**: 发送网络请求，并返回包含响应的对象。

4. **`connect(urlStr: String, header: String?): StrResponse`**
   - **参数**: 
     - `urlStr` - 请求的URL。
     - `header` - 请求头信息的JSON字符串。
   - **功能**: 带请求头发送网络请求，并返回响应对象。

5. **`get(urlStr: String, headers: Map<String, String>): Connection.Response`**
   - **参数**: 
     - `urlStr` - 请求的URL。
     - `headers` - 请求头信息。
   - **功能**: 执行GET请求，并返回响应对象。

6. **`head(urlStr: String, headers: Map<String, String>): Connection.Response`**
   - **参数**: 
     - `urlStr` - 请求的URL。
     - `headers` - 请求头信息。
   - **功能**: 执行HEAD请求，不返回响应体，节省流量。

7. **`post(urlStr: String, body: String, headers: Map<String, String>): Connection.Response`**
   - **参数**: 
     - `urlStr` - 请求的URL。
     - `body` - 请求体内容。
     - `headers` - 请求头信息。
   - **功能**: 执行POST请求，并返回响应对象。

### WebView交互

8. **`webView(html: String?, url: String?, js: String?): String?`**
   - **参数**: 
     - `html` - 直接加载的HTML内容。
     - `url` - URL地址。
     - `js` - 要执行的JavaScript。
   - **功能**: 使用WebView加载内容并返回JavaScript执行结果。

9. **`webViewGetSource(html: String?, url: String?, js: String?, sourceRegex: String): String?`**
   - **参数**: 
     - `html` - HTML内容。
     - `url` - URL地址。
     - `js` - JavaScript代码。
     - `sourceRegex` - 用于匹配资源的正则表达式。
   - **功能**: 使用WebView获取资源的URL。

10. **`webViewGetOverrideUrl(html: String?, url: String?, js: String?, overrideUrlRegex: String): String?`**
    - **参数**: 
      - `html` - HTML内容。
      - `url` - URL地址。
      - `js` - JavaScript代码。
      - `overrideUrlRegex` - 用于匹配重定向URL的正则表达式。
    - **功能**: 使用WebView获取重定向的URL。

### 浏览器操作

11. **`startBrowser(url: String, title: String)`**
    - **参数**: 
      - `url` - 要打开的链接。
      - `title` - 浏览器页面的标题。
    - **功能**: 使用内置浏览器打开链接。

12. **`startBrowserAwait(url: String, title: String): StrResponse`**
    - **参数**: 
      - `url` - 要打开的链接。
      - `title` - 浏览器页面的标题。
    - **功能**: 打开链接并等待网页结果。

### 文件操作

13. **`importScript(path: String): String`**
    - **参数**: `path` - 脚本的路径，可以是网络路径或本地路径。
    - **功能**: 导入JavaScript脚本内容。

14. **`cacheFile(urlStr: String): String`**
    - **参数**: `urlStr` - 网络文件的URL。
    - **功能**: 缓存以文本方式保存的文件，并返回其内容。

15. **`cacheFile(urlStr: String, saveTime: Int): String`**
    - **参数**: 
      - `urlStr` - 网络文件的URL。
      - `saveTime` - 缓存时间（秒）。
    - **功能**: 缓存文件并指定缓存时间。

16. **`downloadFile(url: String): String`**
    - **参数**: `url` - 下载地址。
    - **功能**: 下载文件并返回其相对路径。

17. **`deleteFile(path: String): Boolean`**
    - **参数**: `path` - 文件的相对路径。
    - **功能**: 删除本地文件。

18. **`unzipFile(zipPath: String): String`**
    - **参数**: `zipPath` - ZIP文件的相对路径。
    - **功能**: 解压ZIP文件。

19. **`un7zFile(zipPath: String): String`**
    - **参数**: `zipPath` - 7z文件的相对路径。
    - **功能**: 解压7z文件。

20. **`unrarFile(zipPath: String): String`**
    - **参数**: `zipPath` - RAR文件的相对路径。
    - **功能**: 解压RAR文件。

21. **`unArchiveFile(zipPath: String): String`**
    - **参数**: `zipPath` - 压缩文件的相对路径。
    - **功能**: 解压压缩文件。

22. **`getTxtInFolder(path: String): String`**
    - **参数**: `path` - 文件夹的相对路径。
    - **功能**: 读取文件夹内所有文本文件内容。

23. **`getZipStringContent(url: String, path: String): String`**
    - **参数**: 
      - `url` - ZIP文件的链接或十六进制字符串。
      - `path` - ZIP内文件的路径。
    - **功能**: 获取ZIP文件中指定文件的字符串内容。

24. **`getRarStringContent(url: String, path: String): String`**
    - **参数**: 
      - `url` - RAR文件的链接或十六进制字符串。
      - `path` - RAR内文件的路径。
    - **功能**: 获取RAR文件中指定文件的字符串内容。

25. **`get7zStringContent(url: String, path: String): String`**
    - **参数**: 
      - `url` - 7z文件的链接或十六进制字符串。
      - `path` - 7z内文件的路径。
    - **功能**: 获取7z文件中指定文件的字符串内容。

26. **`getZipByteArrayContent(url: String, path: String): ByteArray?`**
    - **参数**: 
      - `url` - ZIP文件的链接或十六进制字符串。
      - `path` - ZIP内文件的路径。
    - **功能**: 获取ZIP文件中指定文件的字节数组。

27. **`getRarByteArrayContent(url: String, path: String): ByteArray?`**
    - **参数**: 
      - `url` - RAR文件的链接或十六进制字符串。
      - `path` - RAR内文件的路径。
    - **功能**: 获取RAR文件中指定文件的字节数组。

28. **`get7zByteArrayContent(url: String, path: String): ByteArray?`**
    - **参数**: 
      - `url` - 7z文件的链接或十六进制字符串。
      - `path` - 7z内文件的路径。
    - **功能**: 获取7z文件中指定文件的字节数组。

### 编码与解码

29. **`strToBytes(str: String): ByteArray`**
    - **参数**: `str` - 输入字符串。
    - **功能**: 将字符串转换为UTF-8字节数组。

30. **`strToBytes(str: String, charset: String): ByteArray`**
    - **参数**: 
      - `str` - 输入字符串。
      - `charset` - 字符集名称。
    - **功能**: 按指定字符集将字符串转换为字节数组。

31. **`bytesToStr(bytes: ByteArray): String`**
    - **参数**: `bytes` - 输入字节数组。
    - **功能**: 将UTF-8字节数组转换为字符串。

32. **`bytesToStr(bytes: ByteArray, charset: String): String`**
    - **参数**: 
      - `bytes` - 输入字节数组。
      - `charset` - 字符集名称。
    - **功能**: 按指定字符集将字节数组转换为字符串。

33. **`base64Decode(str: String?): String`**
    - **参数**: `str` - Base64编码的字符串。
    - **功能**: 解码Base64字符串。

34. **`base64Decode(str: String?, charset: String): String`**
    - **参数**: 
      - `str` - Base64编码的字符串。
      - `charset` - 字符集名称。
    - **功能**: 按指定字符集解码Base64字符串。

35. **`base64Decode(str: String, flags: Int): String`**
    - **参数**: 
      - `str` - Base64编码的字符串。
      - `flags` - 解码标志。
    - **功能**: 带标志解码Base64字符串。

36. **`base64DecodeToByteArray(str: String?): ByteArray?`**
    - **参数**: `str` - Base64编码的字符串。
    - **功能**: 解码Base64字符串为字节数组。

37. **`base64DecodeToByteArray(str: String?, flags: Int): ByteArray?`**
    - **参数**: 
      - `str` - Base64编码的字符串。
      - `flags` - 解码标志。
    - **功能**: 带标志解码Base64字符串为字节数组。

38. **`base64Encode(str: String): String?`**
    - **参数**: `str` - 输入字符串。
    - **功能**: 编码字符串为Base64。

39. **`base64Encode(str: String, flags: Int): String?`**
    - **参数**: 
      - `str` - 输入字符串。
      - `flags` - 编码标志。
    - **功能**: 带标志编码字符串为Base64。

40. **`hexDecodeToByteArray(hex: String): ByteArray?`**
    - **参数**: `hex` - 十六进制字符串。
    - **功能**: 解码十六进制字符串为字节数组。

41. **`hexDecodeToString(hex: String): String?`**
    - **参数**: `hex` - 十六进制字符串。
    - **功能**: 解码十六进制字符串为UTF-8字符串。

42. **`hexEncodeToString(utf8: String): String?`**
    - **参数**: `utf8` - UTF-8字符串。
    - **功能**: 编码UTF-8字符串为十六进制字符串。

### 时间与格式化

43. **`timeFormatUTC(time: Long, format: String, sh: Int): String?`**
    - **参数**: 
      - `time` - 时间戳。
      - `format` - 时间格式。
      - `sh` - 时区偏移量。
    - **功能**: 格式化时间为UTC格式。

44. **`timeFormat(time: Long): String`**
    - **参数**: `time` - 时间戳。
    - **功能**: 格式化时间。

### 字符编码转换

45. **`utf8ToGbk(str: String): String`**
    - **参数**: `str` - UTF-8编码的字符串。
    - **功能**: 将UTF-8字符串转换为GBK编码。

46. **`encodeURI(str: String): String`**
    - **参数**: `str` - 输入字符串。
    - **功能**: 使用UTF-8编码对字符串进行URI编码。

47. **`encodeURI(str: String, enc: String): String`**
    - **参数**: 
      - `str` - 输入字符串。
      - `enc` - 编码字符集。
    - **功能**: 使用指定字符集对字符串进行URI编码。

48. **`htmlFormat(str: String): String`**
    - **参数**: `str` - HTML字符串。
    - **功能**: 格式化HTML字符串。

### 字体操作

49. **`queryBase64TTF(data: String?): QueryTTF?`**
    - **参数**: `data` - Base64编码的字体数据。
    - **功能**: 解析字体Base64数据，返回字体解析类。

50. **`queryTTF(data: Any?, useCache: Boolean): QueryTTF?`**
    - **参数**: 
      - `data` - 支持URL、本地文件、Base64、ByteArray。
      - `useCache` - 是否使用缓存。
    - **功能**: 返回字体解析类。

51. **`queryTTF(data: Any?): QueryTTF?`**
    - **参数**: `data` - 支持URL、本地文件、Base64、ByteArray。
    - **功能**: 返回字体解析类（默认使用缓存）。

52. **`replaceFont(text: String, errorQueryTTF: QueryTTF?, correctQueryTTF: QueryTTF?, filter: Boolean): String`**
    - **参数**: 
      - `text` - 包含错误字体的内容。
      - `errorQueryTTF` - 错误的字体解析类。
      - `correctQueryTTF` - 正确的字体解析类。
      - `filter` - 是否删除错误字体中不存在的字符。
    - **功能**: 替换字体。

53. **`replaceFont(text: String, errorQueryTTF: QueryTTF?, correctQueryTTF: QueryTTF?): String`**
    - **参数**: 
      - `text` - 包含错误字体的内容。
      - `errorQueryTTF` - 错误的字体解析类。
      - `correctQueryTTF` - 正确的字体解析类。
    - **功能**: 替换字体。

### 其他实用功能

54. **`t2s(text: String): String`**
    - **参数**: `text` - 繁体中文文本。
    - **功能**: 将繁体中文转换为简体中文。

55. **`s2t(text: String): String`**
    - **参数**: `text` - 简体中文文本。
    - **功能**: 将简体中文转换为繁体中文。

56. **`getWebViewUA(): String`**
    - **功能**: 获取WebView的默认用户代理字符串。

57. **`getCookie(tag: String): String`**
    - **参数**: `tag` - Cookie的标识。
    - **功能**: 获取Cookie。

58. **`getCookie(tag: String, key: String?): String`**
    - **参数**: 
      - `tag` - Cookie的标识。
      - `key` - Cookie的键。
    - **功能**: 获取指定键的Cookie。

59. **`toNumChapter(s: String?): String?`**
    - **参数**: `s` - 包含章节数字的字符串。
    - **功能**: 将章节数转换为数字。

60. **`toURL(urlStr: String): JsURL`**
    - **参数**: `urlStr` - URL字符串。
    - **功能**: 转换字符串为`JsURL`对象。

61. **`toURL(url: String, baseUrl: String? = null): JsURL`**
    - **参数**: 
      - `url` - URL字符串。
      - `baseUrl` - 可选的基URL。
    - **功能**: 转换字符串为`JsURL`对象。

62. **`toast(msg: Any?)`**
    - **参数**: `msg` - 要显示的消息。
    - **功能**: 显示短时间的Toast消息。

63. **`longToast(msg: Any?)`**
    - **参数**: `msg` - 要显示的消息。
    - **功能**: 显示长时间的Toast消息。

64. **`log(msg: Any?): Any?`**
    - **参数**: `msg` - 要记录的消息。
    - **功能**: 输出调试日志。

65. **`logType(any: Any?)`**
    - **参数**: `any` - 要检查类型的对象。
    - **功能**: 输出对象的类型。

66. **`randomUUID(): String`**
    - **功能**: 生成一个随机的UUID。

67. **`androidId(): String`**
    - **功能**: 获取Android设备的ID。
