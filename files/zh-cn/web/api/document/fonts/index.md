---
title: fonts
slug: Web/API/Document/fonts
translation_of: Web/API/Document/fonts
---
<p>{{domxref("Document")}}的 <strong><code>fonts</code></strong> 属性接口返回文档的 {{domxref("FontFaceSet")}} 接口。</p>

<h2 id="Syntax">语法</h2>

<pre class="syntaxbox"><var>let fontFaceSet</var> = <em>document</em>.fonts;</pre>

<h3 id="值">值</h3>

<p>返回值是文档的 {{domxref("FontFaceSet")}} 接口。<code>FontFaceSet</code> 接口对 加载新字体、检查已加载字体的加载状态 来说非常有用。</p>

<h2 id="Example">例子</h2>

<h3 id="在所有字体加载完成后进行操作">在所有字体加载完成后进行操作</h3>

<pre class="brush: js">document.fonts.ready.then(function() {
  // 字体加载完成后的逻辑
});
</pre>

<h2 id="Specifications">说明</h2>

{{Specifications}}

<h2 id="See_Also">浏览器兼容性</h2>

<p>{{Compat("api.Document.fonts")}}</p>

<h2 id="See_Also">参考资料</h2>

<ul>
 <li>{{domxref("FontFaceSet")}} interface</li>
 <li>{{domxref("FontFace")}}</li>
</ul>

<div>{{APIRef("DOM")}}</div>