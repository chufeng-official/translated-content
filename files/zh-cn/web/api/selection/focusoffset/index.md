---
title: Selection.focusOffset
slug: Web/API/Selection/focusOffset
tags:
  - HTML 编辑
  - 只读
  - 属性
  - 选区
translation_of: Web/API/Selection/focusOffset
---
<div>
<div>
<div>{{ ApiRef("DOM") }}{{SeeCompatTable}}</div>
</div>
</div>

<p>只读属性 <strong><code>Selection.focusOffset</code></strong> 返回选区终点（鼠标松开瞬间所记录的那个点）在焦点（{{domxref("Selection.focusNode")}}）中的偏移量。返回值从零开始计数，如果选区（{{domxref("Selection")}}）在焦点（{{domxref("Selection.focusNode")}}）的第一个字符前结束，返回值为 0。</p>

<h2 id="Syntax">语法</h2>

<pre class="syntaxbox"><em>offset</em> =<em> sel</em>.focusOffset
</pre>

<h2 id="规范">规范</h2>

{{Specifications}}

<h2 id="Browser_compatibility">浏览器兼容性</h2>

{{Compat("api.Selection.focusOffset")}}

<h2 id="See_also">相关链接</h2>

<ul>
 <li>{{domxref("Selection")}}, 这个属性所属的接口。</li>
</ul>