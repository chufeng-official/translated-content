---
title: HTMLHyperlinkElementUtils.hash
slug: Web/API/HTMLAnchorElement/hash
tags:
  - HTMLHyperlinkElementUtils.hash
translation_of: Web/API/HTMLHyperlinkElementUtils/hash
original_slug: Web/API/HTMLHyperlinkElementUtils/hash
---
<p>{{ APIRef("URLUtils") }}</p>

<p><strong><code>HTMLHyperlinkElementUtils.hash</code></strong> 属性返回一个包含“＃”的 {{domxref("DOMString")}} , 后跟URL的片段标识符。</p>

<p>片段没有<a href="/zh-CN/docs/Glossary/percent-encoding">百分比解码</a>。如果URL没有包含片段标识符，这个属性为一个空的字符串, <code>""</code>.</p>

<h2 id="Syntax">Syntax</h2>

<pre class="syntaxbox"><em>string</em> = <em>object</em>.hash;
<em>object</em>.hash = <em>string</em>;
</pre>

<h2 id="Examples">Examples</h2>

<pre class="brush: js">// Let's an &lt;a id="myAnchor" href="https://developer.mozilla.org/en-US/docs/HTMLHyperlinkElementUtils.href#youhou"&gt; element be in the document
var anchor = document.getElementById("myAnchor");
var result = anchor.hash; // Returns:'#youhou'</pre>

<h2 id="Specifications">Specifications</h2>

{{Specifications}}

<h2 id="Browser_compatibility">Browser compatibility</h2>

{{Compat("api.HTMLAnchorElement.hash")}}

<h2 id="See_also">See also</h2>

<ul>
 <li>The {{domxref("HTMLHyperlinkElementUtils")}} interface it belongs to.</li>
</ul>