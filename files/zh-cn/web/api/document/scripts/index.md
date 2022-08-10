---
title: Document.scripts
slug: Web/API/Document/scripts
translation_of: Web/API/Document/scripts
---
<p>{{ ApiRef() }}</p>
<h3 id="Summary">概述</h3>
<p>返回一个{{ domxref("HTMLCollection") }}对象，包含了当前文档中所有{{ HTMLElement("script") }}元素的集合。</p>
<h3 id="Syntax">语法</h3>
<pre class="eval"><code>var <em>scriptList</em></code> = document.scripts;
</pre>
<p><code>scriptList</code> 是一个 {{ domxref("HTMLCollection") }} 对象。你可以像使用数组一样通过索引来获取其中包含的 {{ HTMLElement("script") }} 元素。</p>
<h3 id="例子">例子</h3>
<p>下例演示了如何查看当前页面是否包含有{{ HTMLElement("script") }}元素。</p>
<pre class="brush: js">var scripts = document.scripts;

if (scripts.length) {
  alert("该页面存在 script 标签！");
}
</pre>
<h3 id="Specification">浏览器兼容性</h3>
{{Compat("api.Document.scripts")}}