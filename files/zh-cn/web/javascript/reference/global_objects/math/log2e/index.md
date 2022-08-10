---
title: Math.LOG2E
slug: Web/JavaScript/Reference/Global_Objects/Math/LOG2E
translation_of: Web/JavaScript/Reference/Global_Objects/Math/LOG2E
---
<div>
 {{JSRef("Global_Objects", "Math")}}</div>
<h2 id="Summary">概述</h2>
<p><code><strong>Math.LOG2E</strong></code> 属性表示以 2 为底数，e 的对数，约为 1.442：</p>
<p><math display="block"><semantics><mrow><mstyle mathvariant="monospace"><mi>Math.LOG2E</mi></mstyle><mo>=</mo><msub><mo lspace="0em" rspace="0em">log</mo><mn>2</mn></msub><mo stretchy="false">(</mo><mi>e</mi><mo stretchy="false">)</mo><mo>≈</mo><mn>1.442</mn></mrow><annotation encoding="TeX">\mathtt{\mi{Math.LOG2E}} = \log_2(e) \approx 1.442</annotation></semantics></math></p>
<div>
 {{js_property_attributes(0,0,0)}}</div>
<h2 id="Description">描述</h2>
<p>由于 <code>LOG2E</code> 是 <code>Math</code> 的静态属性，所以应该像这样使用：<code>Math.LOG2E</code>，而不是作为你创建的 <code>Math</code> 对象的属性（<code>Math</code> 不是一个构造函数）。</p>
<h2 id="Examples">示例</h2>
<h3 id="Example:_Using_Math.LOG2E">例子：使用 <code>Math.LOG2E</code></h3>
<p>下面的函数返回以 2 为底数，E 的对数：</p>
<pre class="brush:js">function getLog2e() {
   return Math.LOG2E
}

getLog2e() // 1.4426950408889634</pre>
<h2 id="规范">规范</h2>
{{Specifications}}

<h2 id="浏览器兼容性">浏览器兼容性</h2>

{{Compat}}

<h2 id="See_also">相关链接</h2>
<ul>
 <li>The {{jsxref("Global_Objects/Math", "Math")}} object it belongs to.</li>
</ul>