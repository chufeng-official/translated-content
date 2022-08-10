---
title: VRDisplay.requestAnimationFrame()
slug: Web/API/VRDisplay/requestAnimationFrame
translation_of: Web/API/VRDisplay/requestAnimationFrame
---
<div>{{APIRef("WebVR API")}}{{SeeCompatTable}}</div>

<p>The <code><strong>requestAnimationFrame()</strong></code> method of the {{domxref("VRDisplay")}} interface is a special implementation of {{domxref("Window.requestAnimationFrame")}} containing a callback function that will be called every time a new frame of the <code>VRDisplay</code> presentation is rendered:</p>

<ul>
 <li>When the <code>VRDisplay</code> is not presenting a scene, this is functionally equivalent to {{domxref("Window.requestAnimationFrame")}}.</li>
 <li>When the VRDisplay is presenting, the callback is called at the native refresh rate of the <code>VRDisplay</code>.</li>
</ul>

<h2 id="Syntax">Syntax</h2>

<pre class="brush: js">var handle = vrDisplayInstance.requestAnimationFrame(<em>callback</em>);
</pre>

<h3 id="Parameters">Parameters</h3>

<dl>
 <dt>callback</dt>
 <dd>A callback function that will be called every time a new frame of the <code>VRDisplay</code> presentation is rendered.</dd>
</dl>

<h3 id="Return_value">Return value</h3>

<p>A long representing the handle of the <code>requestAnimationFrame()</code> call. This can then be passed to a {{domxref("VRDisplay.cancelAnimationFrame()")}} call to unregister the callback.</p>

<h2 id="Examples">Examples</h2>

<pre>TBD.</pre>

<h2 id="Specifications">Specifications</h2>

<p>该 API 在旧的 <a href="https://immersive-web.github.io/webvr/spec/1.1/">WebVR API</a>（已被 <a href="https://immersive-web.github.io/webxr/">WebXR Device API</a> 取代）中定义。它不再有望成为标准。</p>

<p>在所有浏览器都实现新的 <a href="/zh-CN/docs/Web/API/WebXR_Device_API/Fundamentals">WebXR API</a> 之前，建议使用框架（如：<a href="https://aframe.io/">A-Frame</a>、<a href="https://www.babylonjs.com/">Babylon.js</a> 或 <a href="https://threejs.org/">Three.js</a>）或 <a href="https://github.com/immersive-web/webxr-polyfill">polyfill</a> 来开发适用于所有浏览器的 WebXR 应用程序。<a href="https://developer.oculus.com/documentation/web/port-vr-xr/">[1]</a></p>

<h2 id="Browser_compatibility">Browser compatibility</h2>

{{Compat("api.VRDisplay.requestAnimationFrame")}}

<h2 id="See_also">See also</h2>

<ul>
 <li><a href="/en-US/docs/Web/API/WebVR_API">WebVR API homepage</a>.</li>
 <li><a href="http://mozvr.com/">MozVr.com</a> — demos, downloads, and other resources from the Mozilla VR team.</li>
</ul>