---
title: Document.links
slug: Web/API/Document/links
tags:
  - API
  - Document
  - 属性
translation_of: Web/API/Document/links
---
<p>{{APIRef("DOM")}}</p>

<p><code>links</code> 属性返回一个文档中所有具有 href 属性值的 {{HTMLElement("area")}} 元素与 {{HTMLElement("a")}} 元素的集合。</p>

<h3 id="语法">语法</h3>

<pre class="syntaxbox"><em>nodeList</em> = document.links </pre>


<h3 id="返回值">返回值</h3>

<p>一个 {{domxref("HTMLCollection")}}。</p>

<h3 id="示例">示例</h3>

<pre class="brush: js">var links = document.links;
for(var i = 0; i &lt; links.length; i++) {
  var linkHref = document.createTextNode(links[i].href);
  var lineBreak = document.createElement("br");
  document.body.appendChild(linkHref);
  document.body.appendChild(lineBreak);
}
</pre>

<h3 id="规范">规范</h3>

{{Specifications}}

<h2 id="浏览器兼容性">浏览器兼容性</h2>



<p>{{Compat("api.Document.links")}}</p>