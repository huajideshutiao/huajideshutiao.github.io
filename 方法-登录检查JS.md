1. **initUrl()**
   - **功能**: 初始化并处理 URL，通过调用 `analyzeJs()` 和 `replaceKeyPageJs()` 方法来执行 JavaScript 代码和替换关键字。

2. **analyzeJs()**
   - **功能**: 执行嵌入的 JavaScript 代码，并替换结果到 `ruleUrl` 中。
   - **参数**: 无。

3. **replaceKeyPageJs()**
   - **功能**: 替换 URL 中的关键字、页码和 JavaScript 代码。
   - **参数**: 无。

4. **analyzeUrl()**
   - **功能**: 解析 URL，处理可能存在的 URL 参数。
   - **参数**: 无。

5. **evalJS(jsStr: String, result: Any? = null): Any?**
   - **功能**: 使用 Rhino 引擎执行 JavaScript 代码。
   - **参数**:
     - `jsStr`: 要执行的 JavaScript 代码字符串。
     - `result`: 可选的初始结果参数，默认为 `null`。

6. **put(key: String, value: String): String**
   - **功能**: 存储一个键值对。
   - **参数**:
     - `key`: 键。
     - `value`: 值。

7. **get(key: String): String**
   - **功能**: 获取存储在 `chapter` 或 `ruleData` 中的变量。
   - **参数**:
     - `key`: 要获取的键。

8. **fetchStart(): ConcurrentRecord?**
   - **功能**: 开始访问并进行并发判断。
   - **参数**: 无。
   - **返回**: `ConcurrentRecord` 对象或 `null`。

9. **fetchEnd(concurrentRecord: ConcurrentRecord?)**
   - **功能**: 访问结束时的并发控制。
   - **参数**:
     - `concurrentRecord`: 并发记录对象。

10. **getConcurrentRecord(): ConcurrentRecord?**
    - **功能**: 获取并发记录，若处于并发限制状态下则会等待。
    - **参数**: 无。

11. **getStrResponseAwait(jsStr: String? = null, sourceRegex: String? = null, useWebView: Boolean = true): StrResponse**
    - **功能**: 异步访问网站并返回字符串响应。
    - **参数**:
      - `jsStr`: 可选的 JavaScript 字符串。
      - `sourceRegex`: 可选的正则表达式。
      - `useWebView`: 是否使用 WebView。

12. **getStrResponse(jsStr: String? = null, sourceRegex: String? = null, useWebView: Boolean = true): StrResponse**
    - **功能**: 同步访问网站并返回字符串响应。
    - **参数**:
      - `jsStr`: 可选的 JavaScript 字符串。
      - `sourceRegex`: 可选的正则表达式。
      - `useWebView`: 是否使用 WebView。

13. **getResponseAwait(): Response**
    - **功能**: 异步访问网站并返回响应对象。
    - **参数**: 无。

14. **getResponse(): Response**
    - **功能**: 同步访问网站并返回响应对象。
    - **参数**: 无。

15. **getByteArrayIfDataUri(): ByteArray?**
    - **功能**: 如果 URL 是数据 URI，则返回其字节数组。
    - **参数**: 无。

16. **getByteArrayAwait(): ByteArray**
    - **功能**: 异步访问网站并返回字节数组。
    - **参数**: 无。

17. **getByteArray(): ByteArray**
    - **功能**: 同步访问网站并返回字节数组。
    - **参数**: 无。

18. **getInputStreamAwait(): InputStream**
    - **功能**: 异步访问网站并返回输入流。
    - **参数**: 无。

19. **getInputStream(): InputStream**
    - **功能**: 同步访问网站并返回输入流。
    - **参数**: 无。

20. **upload(fileName: String, file: Any, contentType: String): StrResponse**
    - **功能**: 上传文件。
    - **参数**:
      - `fileName`: 文件名。
      - `file`: 文件对象。
      - `contentType`: 文件的内容类型。

21. **setCookie()**
    - **功能**: 设置 Cookie。
    - **参数**: 无。

22. **saveCookie()**
    - **功能**: 保存 Cookie。
    - **参数**: 无。

23. **getGlideUrl(): GlideUrl**
    - **功能**: 获取处理过的 `GlideUrl` 对象，用于图片加载。
    - **参数**: 无。

24. **getMediaItem(): MediaItem**
    - **功能**: 获取 `MediaItem` 对象，用于媒体播放。
    - **参数**: 无。

25. **getUserAgent(): String**
    - **功能**: 获取用户代理字符串。
    - **参数**: 无。

26. **isPost(): Boolean**
    - **功能**: 判断请求方法是否为 POST。
    - **参数**: 无。

27. **getSource(): BaseSource?**
    - **功能**: 获取数据源。
    - **参数**: 无。