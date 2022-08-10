---
title: TypedArray.prototype.reverse()
slug: Web/JavaScript/Reference/Global_Objects/TypedArray/reverse
translation_of: Web/JavaScript/Reference/Global_Objects/TypedArray/reverse
---
<div>{{JSRef}}</div>

<p><code><strong>reverse()</strong></code>方法原地翻转类型化数组。类型化数组的第一个元素变为最后一个，最后一个变为第一个。这个方法的算法和{{jsxref("Array.prototype.reverse()")}}<em>相同。</em> <em>TypedArray</em> 是这里的 <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/TypedArray#TypedArray_objects">类型化数组类型</a> 之一。</p>

<h2 id="语法">语法</h2>

<pre class="syntaxbox"><code><var>typedarray</var>.reverse();</code></pre>

<h3 id="返回值">返回值</h3>

<p>翻转的数组。</p>

<h2 id="示例">示例</h2>

<pre class="brush: js">var uint8 = new Uint8Array([1, 2, 3]);
uint8.reverse();

console.log(uint8); // Uint8Array [3, 2, 1]
</pre>

<h2 id="规范">规范</h2>

{{Specifications}}

<h2 id="浏览器兼容性">浏览器兼容性</h2>

{{Compat}}

<h2 id="另见">另见</h2>

<ul>
 <li>{{jsxref("Array.prototype.reverse()")}}</li>
</ul>