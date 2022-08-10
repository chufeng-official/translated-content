---
title: URL.search
slug: Web/API/URL/search
tags:
  - API
  - Property
  - Reference
  - Search
  - URL
translation_of: Web/API/URL/search
---
<div>{{ApiRef("URL API")}}</div>

<p>{{domxref("URL")}} 接口的<strong><code>search</code></strong> 属性是一个搜索字符串， 也称为查询字符串，这是一个{{domxref("USVString")}}包含一个 <code>'?'</code>后面跟着 URL 的参数</p>

<p>现代浏览器提供{{domxref("URL.searchParams")}}属性，以便轻松解析查询字符串中的参数。</p>

<p>{{AvailableInWorkers}}</p>

<h2 id="语法">语法</h2>

<pre class="syntaxbox"><em>string</em> = <em>object</em>.search;
<em>object</em>.search = <em>string</em>;
</pre>

<h3 id="值">值</h3>

<p>一个 {{domxref("USVString")}}.</p>

<h2 id="例子">例子</h2>

<pre class="brush: js">var url = new URL('https://developer.mozilla.org/en-US/docs/Web/API/URL/search?q=123');
var queryString = url.search; // Returns:"?q=123"
</pre>

<h2 id="规范">规范</h2>

{{Specifications}}

<h2 id="浏览器兼容性">浏览器兼容性</h2>



<p>{{Compat("api.URL.search")}}</p>

<h2 id="参考">参考</h2>

<ul>
 <li>它所属的{{domxref("URL")}}接口。</li>
</ul>