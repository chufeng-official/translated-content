---
title: GlobalEventHandlers.ontouchmove
slug: Web/API/Element/touchmove_event
translation_of: Web/API/GlobalEventHandlers/ontouchmove
original_slug: Web/API/GlobalEventHandlers/ontouchmove
---
<div>{{ApiRef("HTML DOM")}}</div>

<p>A {{domxref("GlobalEventHandlers","global event handler")}} for the {{event("touchmove")}} event.</p>

<h2 id="Syntax">语法</h2>

<pre class="eval">var moveHandler = someElement.ontouchmove;
</pre>

<h3 id="Return_Value">Return value</h3>

<dl>
 <dt><code>moveHandler</code></dt>
 <dd><code>someElement</code>元素的 <em>touchmove 事件处理句柄/函数。</em></dd>
</dl>

<h2 id="例子">例子</h2>

<p>这个例子展示了两种通过 <em>ontouchmove </em>设置元素的 <em>touchmove 事件处理句柄/函数的方式。</em></p>

<pre class="brush: js">&lt;html&gt;
&lt;script&gt;

function moveTouch(ev) {
 // 处理事件
}

function init() {
 var el=document.getElementById("target1");
 el.ontouchmove = moveTouch;
}

&lt;body onload="init();"&gt;
&lt;div id="target1"&gt; Touch me ... &lt;/div&gt;
&lt;div id="target2" ontouchmove="moveTouch(event)"&gt; Touch me ... &lt;/div&gt;
&lt;/body&gt;
&lt;/html&gt;
</pre>

<h2 id="Specifications">Specifications</h2>

{{Specifications}}

<h2 id="Browser_compatibility">Browser compatibility</h2>

{{Compat}}

<h2 id="See_also">See also</h2>

<ul>
 <li>{{ event("touchmove") }}</li>
</ul>