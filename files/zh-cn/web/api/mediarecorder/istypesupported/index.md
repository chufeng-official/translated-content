---
title: MediaRecorder.isTypeSupported
slug: Web/API/MediaRecorder/isTypeSupported
tags:
  - API
  - Audio
  - Media
  - Method
  - Reference
  - Video
translation_of: Web/API/MediaRecorder/isTypeSupported
---
<p>{{APIRef("MediaStream Recording")}}</p>

<p> <strong><code>MediaRecorder.isTypeSupported()</code></strong>方法会判断其 MIME 格式能否被客户端录制。</p>

<h2 id="语法">语法</h2>

<pre class="syntaxbox">var canRecord = <em>MediaRecorder</em>.<strong><code>isTypeSupported</code></strong>(<em>mimeType</em>)</pre>

<h3 id="参数">参数</h3>

<dl>
 <dt><code>mimeType</code></dt>
 <dd>需要检查的 MIME 格式</dd>
</dl>

<h3 id="返回值">返回值</h3>

<p>如果 {{domxref("MediaRecorder")}} 在浏览器上的具体实现能够支持指定 MIME 类型的 {{domxref("Blob")}} 对象就返回 true. 如果没有足够的资源来支持录制和编码任务，最终录制依然会失败。如果返回结果是 false，用户的浏览器就无法录制指定的格式。</p>

<h2 id="Example">Example</h2>

<pre class="brush: js">var types = ["video/webm",
             "audio/webm",
             "video/webm\;codecs=vp8",
             "video/webm\;codecs=daala",
             "video/webm\;codecs=h264",
             "audio/webm\;codecs=opus",
             "video/mpeg"];

for (var i in types) {
  console.log( "Is " + types[i] + " supported? " + (MediaRecorder.isTypeSupported(types[i]) ? "Maybe!" : "Nope :("));
}
</pre>

<h2 id="规范">规范</h2>

{{Specifications}}

<h2 id="浏览器兼容性">浏览器兼容性</h2>

{{Compat("api.MediaRecorder.isTypeSupported")}}

<h2 id="看过这个的用户还浏览了以下内容：">看过这个的用户还浏览了以下内容：</h2>

<ul>
 <li><a href="https://developer.mozilla.org/en-US/docs/Web/API/ServiceWorker_API/Using_Service_Workers">Using Service Workers</a></li>
 <li>{{domxref("MediaStreamTrack")}}</li>
 <li>{{domxref("MediaStream")}}</li>
</ul>