---
title: URL.密码
slug: Web/API/URL/password
translation_of: Web/API/URL/password
original_slug: Web/API/URL/密码
---
<div>{{ApiRef("URL API")}}</div>

<p> {{domxref("URL")}}接口的<strong><code>password</code></strong>属性为{{domxref("USVString")}}，其中包含在域名之前指定的密码。</p>

<p>如果在未设置<a href="/zh-CN/docs/Web/API/URL/username">username</a>属性的情况下进行调用，默认失败。</p>

<p>{{AvailableInWorkers}}</p>

<h2 id="语法">语法</h2>

<pre class="syntaxbox"><em>string</em> = <em>object</em>.password;
<em>object</em>.password = <em>string</em>;
</pre>

<h3 id="值">值</h3>

<p>A {{domxref("USVString")}}.</p>

<h2 id="Examples">Examples</h2>

<pre class="brush: js">var url = new URL('https://anonymous:flabada@developer.mozilla.org/en-US/docs/Web/API/URL/password');
var result = url.password; // Returns:"flabada"
</pre>

<h2 id="规范">规范</h2>

{{Specifications}}

<h2 id="浏览器兼容性">浏览器兼容性</h2>



<p>{{Compat("api.URL.password")}}</p>

<h2 id="参见">参见</h2>

<ul>
 <li>The {{domxref("URL")}} interface it belongs to.</li>
</ul>