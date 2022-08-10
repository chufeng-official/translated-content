---
title: DataView.prototype.getInt8()
slug: Web/JavaScript/Reference/Global_Objects/DataView/getInt8
tags:
  - 类型化
  - 类型化数组
translation_of: Web/JavaScript/Reference/Global_Objects/DataView/getInt8
---
<div>{{JSRef}}</div>

<p><strong><code>getInt8()</code></strong> 方法从 {{jsxref("DataView")}} 相对于起始位置偏移 n 个字节处开始，获取一个有符号的 8-bit 整数 (一个字节)。</p>

<div>{{EmbedInteractiveExample("pages/js/dataview-getint8.html")}}</div>



<h2 id="语法">语法</h2>

<pre class="syntaxbox"><var>dataview</var>.getInt8(byteOffset)</pre>

<h2 id="参数">参数</h2>

<dl>
 <dt>byteOffset</dt>
 <dd>偏移量，单位为字节，从起始位置开始计算。</dd>
</dl>

<h3 id="抛出错误">抛出错误</h3>

<dl>
 <dt>{{jsxref("RangeError")}}</dt>
 <dd>如果 byteOffset 超出了视图能储存的值，就会抛出错误。</dd>
</dl>

<h2 id="描述">描述</h2>

<p> 没有对齐约束; 多字节值可以从任何偏移量获取。</p>

<h2 id="例子">例子</h2>

<pre class="brush:js">var buffer = new ArrayBuffer(8);
var dataview = new DataView(buffer);
dataview.getInt8(1); // 0
</pre>

<h2 id="规范">规范</h2>

{{Specifications}}

<h2 id="浏览器兼容性">浏览器兼容性</h2>



<p>{{Compat}}</p>

<h2 id="相关内容">相关内容</h2>

<ul>
 <li>{{jsxref("DataView")}}</li>
 <li>{{jsxref("ArrayBuffer")}}</li>
</ul>