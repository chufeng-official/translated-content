---
title: DataView.prototype.getUint16()
slug: Web/JavaScript/Reference/Global_Objects/DataView/getUint16
tags:
  - 类型化
  - 类型化数组
translation_of: Web/JavaScript/Reference/Global_Objects/DataView/getUint16
---
<div>{{JSRef}}</div>

<p><strong><code>getUint16()</code></strong> 方法从 <a href="/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/DataView"><code>DataView</code></a> 相对于起始位置偏移 n 个字节处开始，获取一个 16-bit 数 (无符号短整型，2 个字节)。</p>

<div>{{EmbedInteractiveExample("pages/js/dataview-getuint16.html")}}</div>



<h2 id="语法">语法</h2>

<pre class="syntaxbox"><var>dataview</var>.getUint16(byteOffset [, littleEndian])</pre>

<h3 id="参数">参数</h3>

<dl>
 <dt>byteOffset</dt>
 <dd>偏移量，单位为字节，从头开始计算。</dd>
 <dt>littleEndian</dt>
 <dd>{{optional_inline}} Indicates whether the 16-bit int is stored in {{Glossary("Endianness", "little- or big-endian")}} format. If false or undefined, a big-endian value is read.</dd>
</dl>

<h3 id="返回">返回</h3>

<p>一个无符号短整型 16 位数。</p>

<h3 id="抛出错误">抛出错误</h3>

<dl>
 <dt>{{jsxref("RangeError")}}</dt>
 <dd>如果 byteOffset 超出了视图能储存的值，就会抛出错误。</dd>
</dl>

<h2 id="描述">描述</h2>

<p>没有对齐约束; 多字节值可以从任何偏移量获取。</p>

<h2 id="例子">例子</h2>

<pre class="brush:js">var buffer = new ArrayBuffer(8);
var dataview = new DataView(buffer);
dataview.getUint16(1); // 0
</pre>

<h2 id="规范">规范</h2>

{{Specifications}}

<h2 id="浏览器兼容性">浏览器兼容性</h2>

<p>{{Compat}}</p>

<h2 id="另见">另见</h2>

<ul>
 <li>{{jsxref("DataView")}}</li>
 <li>{{jsxref("ArrayBuffer")}}</li>
</ul>