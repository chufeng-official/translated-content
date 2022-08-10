---
title: HTMLHyperlinkElementUtils.origin
slug: Web/API/HTMLAnchorElement/origin
tags:
  - HTMLHyperlinkElementUtils.origin
translation_of: Web/API/HTMLHyperlinkElementUtils/origin
original_slug: Web/API/HTMLHyperlinkElementUtils/origin
---
<p>{{APIRef("URL API")}}</p>

<p><strong><code>HTMLHyperlinkElementUtils.origin</code></strong> 只读属性是一个 {{domxref("USVString")}} ，其中包含代表URL的原始码的Unicode序列化，即：</p>

<ul>
 <li>for URL using the <code>http</code> or <code>https</code>, the scheme followed by <code>'://'</code>, followed by the domain, followed by <code>':'</code>, followed by the port (the default port, <code>80</code> and <code>443</code> respectively, if explicitely specified);</li>
 <li>for URL using <code>file:</code> scheme, the value is browser dependant;</li>
 <li>for URL using the <code>blob:</code> scheme, the origin of the URL following <code>blob:</code>. E.g <code>"blob:https://mozilla.org"</code> will have <code>"https://mozilla.org".</code></li>
</ul>

<p>{{AvailableInWorkers}}</p>

<h2 id="Syntax">Syntax</h2>

<pre class="syntaxbox"><em>string</em> = <em>object</em>.origin;
</pre>

<h2 id="Examples">Examples</h2>

<pre class="brush: js">// On this page, returns the origin
var result = window.location.origin; // Returns:'https://developer.mozilla.org'
</pre>

<h2 id="Specifications">Specifications</h2>

{{Specifications}}

<h2 id="Browser_compatibility">Browser compatibility</h2>

{{Compat("api.HTMLAnchorElement.origin")}}

<h2 id="See_also">See also</h2>

<ul>
 <li>The {{domxref("HTMLHyperlinkElementUtils")}} mixin it belongs to.</li>
</ul>