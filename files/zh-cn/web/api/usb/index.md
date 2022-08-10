---
title: USB
slug: Web/API/USB
translation_of: Web/API/USB
---
<p>{{SeeCompatTable}}{{APIRef("WebUSB API")}}</p>

<p><a href="/en-US/docs/Web/API/WebUSB_API">WebUSB API</a> 接口提供了从网页查找和连接 USB 设备的属性和方法</p>

<h2 id="属性">属性</h2>

<p>None.</p>

<h3 id="Event_handlers">Event handlers</h3>

<dl>
 <dt>{{domxref("USB.onconnect")}}</dt>
 <dd>每当连接到先前配对的设备时，调用此事件处理器。</dd>
 <dt>{{domxref("USB.ondisconnect")}}</dt>
 <dd>每当配对设备断开连接时，调用此事件处理器。</dd>
</dl>

<h2 id="方法">方法</h2>

<dl>
 <dt>{{domxref("USB.getDevices()")}}</dt>
 <dd>Returns a {{jsxref("Promise")}} that resolves with an array of {{domxref("USBDevice")}} objects for paired attached devices.</dd>
 <dt>{{domxref("USB.requestDevice()")}}</dt>
 <dd>Returns a {{jsxref("Promise")}} that resolves with an instance of {{domxref("USBDevice")}} if the specified device is found. Calling this function triggers the user agent's pairing flow.</dd>
</dl>

<h2 id="规范">规范</h2>

{{Specifications}}

<h2 id="Browser_compatibility">Browser compatibility</h2>



<p>{{Compat("api.USB")}}</p>