---
title: Window.onappinstalled
slug: Web/API/Window/appinstalled_event
translation_of: Web/API/Window/onappinstalled
original_slug: Web/API/Window/onappinstalled
---
<div>{{APIRef}}</div>

<p>{{domxref("Window")}} 对象的 <code><strong>onappinstalled</strong></code> 属性用于处理 {{Event("appinstalled")}}  事件，该事件是一个实现了 {{domxref("Event")}}接口的简单事件，会在网页应用成功安装为<a href="https://developer.mozilla.org/en-US/Apps/Progressive">渐进式网页应用</a>时立即触发。</p>

<h2 id="Syntax">语法</h2>

<pre class="syntaxbox">window.onappinstalled = function(event) { ... };
</pre>

<h2 id="示例">示例</h2>

<pre class="brush: js">window.onappinstalled = function(ev) {
  console.log('The application was installed.');
};</pre>

<h2 id="浏览器兼容性">浏览器兼容性</h2>

{{Compat}}

<h2 id="See_also">相关文章</h2>

<ul>
 <li>{{domxref("Event")}}</li>
</ul>