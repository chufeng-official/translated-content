---
title: XMLHttpRequest.responseURL
slug: Web/API/XMLHttpRequest/responseURL
tags:
  - XMLHttpRequest.responseURL
translation_of: Web/API/XMLHttpRequest/responseURL
---
<p>{{APIRef('XMLHttpRequest')}}</p>

<p>只读属性<code><strong>XMLHttpRequest.responseURL</strong></code>返回响应的序列化 URL，如果 URL 为空则返回空字符串。如果 URL 有锚点，则位于 URL # 后面的内容会被删除。如果 URL 有重定向，<code>responseURL</code> 的值会是经过多次重定向后的最终 URL。</p>

<h2 id="实例">实例</h2>

<pre class="brush: js">var xhr = new XMLHttpRequest();
xhr.open('GET', 'http://example.com/test', true);
xhr.onload = function () {
  console.log(xhr.responseURL); // http://example.com/test
};
xhr.send(null);</pre>

<h2 id="规范">规范</h2>

{{Specifications}}

<h2 id="浏览器兼容性">浏览器兼容性</h2>

{{Compat("api.XMLHttpRequest.responseURL")}}