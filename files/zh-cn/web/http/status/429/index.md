---
title: 429 Too Many Requests
slug: Web/HTTP/Status/429
tags:
  - HTTP 协议
  - 客户端错误
  - 状态码
translation_of: Web/HTTP/Status/429
---
<div>{{HTTPSidebar}}</div>

<p>在 HTTP 协议中，响应状态码 <code><strong>429 Too Many Requests</strong></code> 表示在一定的时间内用户发送了太多的请求，即超出了“频次限制”。</p>

<p>在响应中，可以提供一个  {{HTTPHeader("Retry-After")}} 首部来提示用户需要等待多长时间之后再发送新的请求。</p>

<h2 id="状态">状态</h2>

<pre class="syntaxbox">429 Too Many Requests</pre>

<h2 id="示例">示例</h2>

<pre>HTTP/1.1 429 Too Many Requests
Content-Type: text/html
Retry-After: 3600</pre>

<h2 id="规范">规范</h2>

{{Specifications}}

<h2 id="相关内容">相关内容</h2>

<ul>
 <li>{{HTTPHeader("Retry-After")}}</li>
</ul>