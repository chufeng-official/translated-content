---
title: DataView.prototype.getFloat32()
slug: Web/JavaScript/Reference/Global_Objects/DataView/getFloat32
tags:
  - DataView
  - getFloat32
translation_of: Web/JavaScript/Reference/Global_Objects/DataView/getFloat32
---
<div>{{JSRef}}</div>

<p><strong><code>getFloat32()</code></strong>方法从相对于{{jsxref("DataView")}} 的起始位置偏移 n 个字节处获取一个 32-bit 浮点数 (单精度浮点数，4 个字节).</p>

<div>{{EmbedInteractiveExample("pages/js/dataview-getfloat32.html")}}</div>



<h2 id="语法">语法</h2>

<pre class="syntaxbox"><var>dataview</var>.getFloat32(byteOffset [, littleEndian])</pre>

<h3 id="参数">参数</h3>

<dl>
 <dt>byteOffset</dt>
 <dd>偏移量，单位为字节，为从视图的开始位置到读取数值的位置的偏移。</dd>
 <dt>littleEndian</dt>
 <dd>{{optional_inline}} 表示这个 32 位浮点数是否以 {{Glossary("Endianness", "little- or big-endian")}} 格式存储，如果设置为 false 或者不指定，将用 big-endian 格式读取数值。</dd>
</dl>

<h3 id="返回">返回</h3>

<p>一个带符号的 32 位浮点数。</p>

<h3 id="抛出错误">抛出错误</h3>

<dl>
 <dt>{{jsxref("RangeError")}}</dt>
 <dd>如果 byteOffset 设置导致读数值时超出了视图的末尾就会抛出错误。</dd>
</dl>

<h2 id="说明">说明</h2>

<p>没有对齐约束; 多字节值可以从任何偏移处获取。</p>

<h2 id="例子">例子</h2>

<pre class="brush:js">var buffer = new ArrayBuffer(8);
var dataview = new DataView(buffer);
dataview.getFloat32(1); // 0
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