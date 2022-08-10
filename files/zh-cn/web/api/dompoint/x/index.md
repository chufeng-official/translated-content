---
title: DOMPoint.x
slug: Web/API/DOMPoint/x
translation_of: Web/API/DOMPoint/x
---
<div>{{APIRef("DOM")}}</div>

<p><code><strong>DOMPoint</strong></code> 的 x 属性表示该点的水平坐标。 通常， <code>x</code> 的正值表示右边，负值表示左边，除非改变了默认的轴方向。</p>

<h2 id="语法">语法</h2>

<pre class="syntaxbox">var <em>xPos</em> = <em>DOMPoint</em>.x;</pre>

<h3 id="值">值</h3>

<p>双精度浮点值，表示该点的 x 坐标值。这个值的类型并没有严格限制，意味着它可以是 {{jsxref("NaN")}} 或 {{jsxref("Infinity", "±Infinity")}}。</p>

<h2 id="规范">规范</h2>

{{Specifications}}

<h2 id="浏览器兼容性">浏览器兼容性</h2>



<p>{{Compat("api.DOMPointReadOnly.x")}}</p>

<h2 id="相关链接">相关链接</h2>

<ul>
 <li>其他坐标属性：{{domxref("DOMPoint.y", "y")}}，{{domxref("DOMPoint.z", "z")}}，透视值 {{domxref("DOMPoint.w", "w")}}.</li>
</ul>