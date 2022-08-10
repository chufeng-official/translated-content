---
title: window.mozAnimationStartTime
slug: Web/API/Animation/startTime
translation_of: Web/API/Window/mozAnimationStartTime
original_slug: Web/API/Window/mozAnimationStartTIme
---
<p>{{ ApiRef() }}</p>
<p>{{ non-standard_header() }}</p>
<h3 id="Summary">概述</h3>
<p>Returns the time, in milliseconds since the epoch, at which animations started now should be considered to have started. This value should be used instead of, for example, <code><a href="/zh-cn/JavaScript/Reference/Global_Objects/Date/now">Date.now()</a></code>, because this value will be the same for all animations started in this window during this refresh interval, allowing them to remain in sync with one another.</p>
<p>This also allows JavaScript-based animations to remain synchronized with CSS transitions and SMIL animations triggered during the same refresh interval.</p>
<h3 id="Syntax">语法</h3>
<pre class="eval"><em>time</em> = window.mozAnimationStartTime;
</pre>
<h3 id="Specification">规范</h3>
<p>不属于任何规范。</p>
<h3 id="相关链接">相关链接</h3>
<ul>
 <li>{{ domxref("window.requestAnimationFrame()") }}</li>
 <li>{{ domxref("window.onmozbeforepaint") }}</li>
</ul>