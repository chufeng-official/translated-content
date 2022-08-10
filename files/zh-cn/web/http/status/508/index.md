---
title: 508 Loop Detected
slug: Web/HTTP/Status/508
tags:
  - '508'
  - HTTP
  - 服务器错误
  - 状态码
translation_of: Web/HTTP/Status/508
---
<div>{{HTTPSidebar}}</div>

<p>HTTP 协议的 <code><strong>508 Loop Detected</strong></code> 状态码可以在 WebDAV 协议（基于 Web 的分布式创作和版本控制）中给出。</p>

<p>508 码表示服务器中断一个操作，因为它在处理具有“Depth: infinity”的请求时遇到了一个无限循环。508 码表示整个操作失败。</p>

<h2 id="Status">Status</h2>

<pre class="syntaxbox">508 Loop Detected</pre>

<h2 id="Specifications">Specifications</h2>

{{Specifications}}