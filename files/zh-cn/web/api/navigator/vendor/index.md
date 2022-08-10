---
title: Navigator.vendor
slug: Web/API/Navigator/vendor
translation_of: Web/API/Navigator/vendor
---
<p>{{ ApiRef() }}</p>

<h3 id="Summary">概述</h3>

<p>返回当前所使用浏览器的浏览器供应商的名称。</p>

<h3 id="Syntax">语法</h3>

<pre class="eval"><em>venString</em> = window.navigator.vendor
</pre>

<h3 id="Parameters">参数</h3>

<ul>
 <li><code>venString</code> 浏览器供应商。</li>
</ul>

<h3 id="Example">例子</h3>

<pre>window.navigator.vendor
// 返回 "Netscape6"
</pre>

<h3 id="Notes">备注</h3>

<p>vendor 属性值也是组成 userAgent 字符串的一部分 .product 属性值和 vendor 属性值可以是不同的，比如在 Firefox 中，两者的值表示：Netscape 6.1 使用 Gecko 来渲染网页。想了解更多，请查看 <a href="/zh-cn/DOM/window.navigator.product">navigator.product</a>，<a href="/zh-cn/DOM/window.navigator.userAgent">navigator.userAgent</a></p>

<h2 id="规范">规范</h2>

{{Specifications}}

<h2 id="浏览器兼容性">浏览器兼容性</h2>

{{Compat}}