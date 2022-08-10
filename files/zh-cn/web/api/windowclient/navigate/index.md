---
title: WindowClient.navigate()
slug: Web/API/WindowClient/navigate
translation_of: Web/API/WindowClient/navigate
---
<p>{{SeeCompatTable}}{{APIRef("Service Workers API")}}</p>

<p>{{domxref("WindowClient")}} 接口的<strong><code> navigate() </code></strong>方法加载特定的 URL 地址到一个被控制的浏览器页面，并返回一个当前 {{domxref("WindowClient")}} 议的 {{jsxref("Promise")}} 对象。</p>

<h2 id="语法">语法</h2>

<pre class="syntaxbox"><em>WindowClient</em>.navigate(<em>url</em>).then(function(<em>WindowClient</em>) {
  // do something with your WindowClient after navigation
});</pre>

<h3 id="参数">参数</h3>

<dl>
 <dt><code>url</code></dt>
 <dd>跳转地址</dd>
</dl>

<h3 id="返回值">返回值</h3>

<p>一个 {{domxref("WindowClient")}}决议的{{jsxref("Promise")}}对象。</p>

<h2 id="Specifications">Specifications</h2>

{{Specifications}}

<h2 id="浏览器兼容性">浏览器兼容性</h2>

{{Compat("api.WindowClient.navigate")}}