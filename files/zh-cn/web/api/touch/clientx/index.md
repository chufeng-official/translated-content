---
title: Touch.clientX
slug: Web/API/Touch/clientX
tags:
  - touch
translation_of: Web/API/Touch/clientX
---
<p>{{ ApiRef() }}</p>
<h3 id="Summary">概述</h3>
<p>返回触点相对于可见视区 (<a href="http://www.quirksmode.org/mobile/viewports2.html">visual viewport</a>) 左边沿的的 X 坐标。不包括任何滚动偏移.这个值会根据用户对可见视区的缩放行为而发生变化。</p>
<h3 id="Syntax">语法</h3>
<pre class="eval">var <em>x</em> = <em>touchItem</em>.clientX;
</pre>
<h3 id="Return_Value">返回值</h3>
<dl>
 <dt>
  <code>x</code></dt>
 <dd>
  触点相对于可见视区 (<a href="http://www.quirksmode.org/mobile/viewports2.html">visual viewport</a>) 左边沿的的 X 坐标。不包括任何滚动偏移。</dd>
</dl>
<h3 id="Specification">标准定义</h3>
<p><a href="http://www.w3.org/TR/touch-events/">Touch Events Specification</a></p>
<h3 id="相关链接">相关链接</h3>
<ul>
 <li>{{ domxref("Touch.clientY") }}</li>
 <li>{{ domxref("Touch.screenX") }}</li>
 <li>{{ domxref("Touch.pageX") }}</li>
</ul>