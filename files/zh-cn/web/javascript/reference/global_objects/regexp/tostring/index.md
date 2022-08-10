---
title: RegExp.prototype.toString()
slug: Web/JavaScript/Reference/Global_Objects/RegExp/toString
tags:
  - JavaScript
  - Method
  - Prototype
  - RegExp
translation_of: Web/JavaScript/Reference/Global_Objects/RegExp/toString
---
<div>
 {{JSRef("Global_Objects", "RegExp")}}</div>
<h2 id="Summary">概述</h2>
<p><code><strong>toString()</strong></code> 返回一个表示该正则表达式的字符串。</p>
<h2 id="Syntax">语法</h2>
<pre class="syntaxbox"><var>regexObj</var>.toString()</pre>
<h3 id="Parameters">参数</h3>
<p>无</p>
<h2 id="Description">描述</h2>
<p>{{jsxref("Global_Objects/RegExp", "RegExp")}} 对象覆盖了 {{jsxref("Global_Objects/Object", "Object")}} 对象的 <code>toString()</code> 方法，并没有继承 {{jsxref("Object.prototype.toString()")}}。对于 <code>RegExp</code> 对象，<code>toString</code> 方法返回一个该正则表达式的字符串形式。</p>
<h2 id="Examples">示例</h2>
<h3 id="Example:_Using_toString">例子：使用 <code>toString</code></h3>
<p>下例输出 <code>RegExp</code> 对象的字符串值：</p>
<pre>myExp = new RegExp("a+b+c");
alert(myExp.toString());       // 显示 "/a+b+c/"

foo = new RegExp("bar", "g");
alert(foo.toString());         // 显示 "/bar/g"
</pre>
<h2 id="规范">规范</h2>
{{Specifications}}

<h2 id="浏览器兼容性">浏览器兼容性</h2>

{{Compat}}

<h2 id="See_Also">相关链接</h2>
<ul>
 <li>{{jsxref("Object.prototype.toString()")}}</li>
</ul>