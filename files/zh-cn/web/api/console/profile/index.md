---
title: Console.profile()
slug: Web/API/Console/profile
tags:
  - API
  - DOM
  - Web 开发
  - web 控制台
  - 参考
  - 描述信息
  - 方法
  - 调试
  - 非标准
translation_of: Web/API/Console/profile
---
<p>{{APIRef("Console API")}}{{Non-standard_header}}</p>

<p>开始记录性能描述信息 (例如， <a href="/en-US/docs/Tools/Performance">Firefox performance tool</a>)。</p>

<p>你可以选择提供一个参数来命名描述信息，这将允许你在有多个描述信息被记录时来选择只停止那个描述信息（被你命名的那个）。请查阅{{domxref("Console.profileEnd()")}}来确认这个参数是如何被解释的。</p>

<p>要停止记录，请调用{{domxref("Console.profileEnd()")}}。</p>

<p>{{AvailableInWorkers}}</p>

<h2 id="Syntax">Syntax</h2>

<pre class="syntaxbox">console.profile(<em>profileName</em>);
</pre>

<h2 id="Parameters">Parameters</h2>

<dl>
 <dt><code>profileName</code></dt>
 <dd>描述信息的名字。可选。</dd>
</dl>

<h2 id="浏览器兼容性">浏览器兼容性</h2>

{{Compat("api.console.profile")}}

<h2 id="参见">参见</h2>

<ul>
 <li>{{domxref("Console.profileEnd()")}}</li>
</ul>