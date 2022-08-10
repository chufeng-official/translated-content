---
title: Date.prototype.setTime()
slug: Web/JavaScript/Reference/Global_Objects/Date/setTime
translation_of: Web/JavaScript/Reference/Global_Objects/Date/setTime
---
<div>{{JSRef("Global_Objects", "Date")}}</div>

<p><code><strong>setTime()</strong></code> 方法以一个表示从 1970-1-1 00:00:00 UTC 计时的毫秒数为来为 <code>Date</code> 对象设置时间。</p>

<div>{{EmbedInteractiveExample("pages/js/date-settime.html")}}</div>



<h2 id="Syntax">语法</h2>

<pre class="syntaxbox"><var>dateObj</var>.setTime(<em>timeValue</em>)</pre>

<h3 id="Parameters">参数</h3>

<dl>
 <dt><code>timeValue</code></dt>
 <dd>一个整数，表示从 1970-1-1 00:00:00 UTC 开始计时的毫秒数。</dd>
</dl>

<h3 id="Parameters">返回值</h3>
<p>UTC 1970 年 1 月 1 日 00:00:00 与更新日期之间的毫秒数（实际上是自变量的值）。</p>

<h2 id="Description">描述</h2>

<p>使用 <code>setTime</code> 方法用来把一个日期时间赋值给另一个 <code>Date </code>对象。</p>

<h2 id="Examples">例子</h2>

<h3 id="Example_Using_setTime">例子：使用<code>setTime</code></h3>

<pre>theBigDay = new Date("July 1, 1999");
sameAsBigDay = new Date();
sameAsBigDay.setTime(theBigDay.getTime());
</pre>

<h2 id="规范">规范</h2>

{{Specifications}}

<h2 id="浏览器兼容性">浏览器兼容性</h2>

<p>{{Compat}}</p>

<h2 id="See_Also">相关链接</h2>

<ul>
 <li>{{jsxref("Date.prototype.getTime()")}}</li>
 <li>{{jsxref("Date.prototype.setUTCHours()")}}</li>
</ul>