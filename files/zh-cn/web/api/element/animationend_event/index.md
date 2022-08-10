---
title: GlobalEventHandler.onanimationend
slug: Web/API/Element/animationend_event
translation_of: Web/API/GlobalEventHandlers/onanimationend
original_slug: Web/API/GlobalEventHandlers/onanimationend
---
<h2 id="概述">概述</h2>

<p>事件处理程序。 当 CSS 动画到达其活动期的结束时发送此事件</p>

<h2 id="语法">语法</h2>

<pre class="syntaxbox">var <em>animEndHandler</em> = <em>target</em>.onanimationend;

<em>target</em>.onanimationend = <em>事件处理函数</em>
</pre>

<h3 id="值">值</h3>

<p>当<em><code>target</code></em>(HTML 元素， document 或者 window) 的 CSS 动画已经开始，{{event("animationend")}}事件会触发同时<code>事件处理函数</code>会被调用。<code>事件处理函数</code>会接收到唯一的参数：{{domxref("AnimationEvent")}} 描述发生的事件。</p>

<h2 id="例子">例子</h2>

<p>{{Page("/en-US/docs/Web/API/GlobalEventHandlers/onanimationstart", "Example")}}</p>

<h2 id="规范">规范</h2>

{{Specifications}}

<h2 id="浏览器兼容性">浏览器兼容性</h2>

{{Compat}}

<h2 id="参考">参考</h2>

<ul>
 <li>The {{event("animationend")}} event this event handler is triggered by</li>
 <li>{{domxref("AnimationEvent")}}</li>
 <li>The {{event("animationstart")}} event</li>
</ul>