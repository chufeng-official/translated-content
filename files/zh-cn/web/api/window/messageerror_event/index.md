---
title: WindowEventHandlers.onmessageerror
slug: Web/API/Window/messageerror_event
translation_of: Web/API/WindowEventHandlers/onmessageerror
original_slug: Web/API/WindowEventHandlers/onmessageerror
---
<div>{{APIRef("HTML DOM")}}</div>

<p> </p>

<p>{{domxref("WindowEventHandlers")}}接口的 onmessageerror 事件处理器是一个 {{domxref("EventListener")}}，每当一个类型为 <code>messageerror</code> 的 {{domxref("EventListener")}} 事件在一个窗口被触发 --也就是说，当它收到的消息不能是{{glossary("Deserialization", "deserialized")}} 。</p>

<p>{{AvailableInWorkers}}</p>

<h2 id="语法">语法</h2>

<pre class="syntaxbox"><em>window</em>.onmessageerror = function() { ... };</pre>

<h2 id="规范">规范</h2>

{{Specifications}}

<h2 id="浏览器兼容性">浏览器兼容性</h2>

{{Compat("api.WindowEventHandlers.onmessageerror")}}

<h2 id="See_also">See also</h2>

<ul>
 <li><a href="/en-US/docs/Web/API/Channel_Messaging_API/Using_channel_messaging">Using channel messaging</a></li>
</ul>