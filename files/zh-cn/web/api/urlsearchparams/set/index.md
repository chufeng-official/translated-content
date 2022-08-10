---
title: URLSearchParams.set()
slug: Web/API/URLSearchParams/set
translation_of: Web/API/URLSearchParams/set
---
<p>{{ApiRef("URL API")}}{{SeeCompatTable}} </p>

<p>{{domxref("URLSearchParams")}}接口的 set() 方法用于设置和搜索参数相关联的值。如果设置前已经存在匹配的值，该方法会删除多余的，如果将要设置的值不存在，则创建它</p>

<h2 id="语法">语法</h2>

<pre class="syntaxbox">URLSearchParams.set(name, value)</pre>

<h3 id="参数">参数</h3>

<dl>
 <dt>键名</dt>
 <dd>将要设置的参数的健值名。</dd>
 <dt>参数值</dt>
 <dd>所要设置的参数值。</dd>
</dl>

<h3 id="返回值">返回值</h3>

<p>Void</p>

<h2 id="例子">例子</h2>

<pre class="brush: js">let url = new URL('https://example.com?foo=1&amp;bar=2');
let params = new URLSearchParams(url.search.slice(1));

//Add a third parameter.
params.set('baz', 3);
</pre>

<h2 id="Specifications">Specifications</h2>

{{Specifications}}

<h2 id="Browser_compatibility">Browser compatibility</h2>

{{Compat("api.URLSearchParams.set")}}