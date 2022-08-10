---
title: History.length
slug: Web/API/History/length
translation_of: Web/API/History/length
---
<div>{{ APIRef("HTML DOM") }}</div>

<p>History.length 是一个只读属性，返回当前 session 中的 history 个数，包含当前页面在内。举个例子，对于新开一个 tab 加载的页面当前属性返回值 1。</p>

<p> </p>

<h2 id="语法">语法</h2>

<p> </p>

<pre class="syntaxbox"><em>length</em> = <em>history</em>.length;
</pre>

<h2 id="例子">例子</h2>

<pre class="brush: js">var result = window.history.length; // 返回当前 session 中的 history 个数</pre>

<h2 id="规范">规范</h2>

{{Specifications}}

<h2 id="浏览器兼容性">浏览器兼容性</h2>



<p>{{Compat("api.History.length")}}</p>

<h2 id="参考">参考</h2>

<ul>
 <li>The {{domxref("History")}} interface it belongs to.</li>
</ul>