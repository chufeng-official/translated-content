---
title: 511 Network Authentication Required
slug: Web/HTTP/Status/511
tags:
  - 响应状态码
  - 响应码
  - 服务器端错误
  - 状态码
translation_of: Web/HTTP/Status/511
---
<div>{{HTTPSidebar}}</div>

<p><code><strong>511 Network Authentication Required</strong></code> 是一种 HTTP 协议的错误状态代码，表示客户端需要通过验证才能使用该网络。</p>

<p>该状态码不是由源头服务器生成的，而是由控制网络访问的拦截代理服务器生成的。</p>

<p>网络运营商们有时候会在准许使用网络之前要求用户进行身份验证、接受某些条款，或者进行其他形式的与用户之间的互动（例如在网络咖啡厅或者机场）。他们通常用用户设备的  {{Glossary("MAC")}} 地址来进行识别。</p>

<h2 id="状态">状态</h2>

<pre class="syntaxbox">511 Network Authentication Required</pre>

<h2 id="规范">规范</h2>

{{Specifications}}

<h2 id="相关内容">相关内容</h2>

<ul>
 <li>{{Glossary("Proxy server")}}</li>
</ul>