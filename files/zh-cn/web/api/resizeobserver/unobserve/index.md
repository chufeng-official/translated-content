---
title: ResizeObserver.unobserve()
slug: Web/API/ResizeObserver/unobserve
translation_of: Web/API/ResizeObserver/unobserve
---
<div>{{APIRef("Resize Observer API")}}{{SeeCompatTable}}</div>

<p>The <strong><code>unobserve()</code></strong> method of the {{domxref("ResizeObserver")}} interface ends the observing of a specified {{domxref('Element')}} or {{domxref('SVGElement')}}.<br>
 {{domxref("ResizeObserver")}} 接口的 <strong><code>unobserve()</code></strong>  方法用于结束一个指定的 {{domxref('Element')}} 或 {{domxref('SVGElement')}} 的观察。</p>

<h2 id="语法">语法</h2>

<pre class="syntaxbox">void unobserve(target);</pre>

<h3 id="参数">参数</h3>

<dl>
 <dt>target</dt>
 <dd>取消监听的{{domxref('Element')}} 或 {{domxref('SVGElement')}} 的引用。</dd>
</dl>

<h3 id="返回值">返回值</h3>

<p>{{jsxref('undefined')}}</p>

<h3 id="异常">异常</h3>

<p>无。</p>

<h2 id="规范">规范</h2>

{{Specifications}}

<h2 id="浏览器兼容性">浏览器兼容性</h2>



<p>{{Compat("api.ResizeObserver.unobserve")}}</p>