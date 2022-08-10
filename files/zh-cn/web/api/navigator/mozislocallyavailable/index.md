---
title: Navigator.mozIsLocallyAvailable()
slug: Web/API/Navigator/mozIsLocallyAvailable
translation_of: Web/API/Navigator/mozIsLocallyAvailable
---
<p>{{APIRef("HTML DOM")}}{{Non-standard_header}}</p>

<h3 id="Summary">概述</h3>

<p>查询某个 URI 上的资源是否是本地可用的。</p>

<h3 id="Syntax">语法</h3>

<pre class="eval">window.navigator.mozIsLocallyAvailable(<em>uri</em>, <em>ifOffline</em>);
</pre>

<ul>
 <li><code>uri</code> 将要查询本地可用性的的资源的 URI，</li>
 <li><code>ifOffline</code> 是否检查离线资源缓存。</li>
</ul>

<h3 id="Example">例子</h3>

<pre class="eval">var available = navigator.mozIsLocallyAvailable("http:www.example.com/my-image-file.png", true);
if (available) {
  /* 该离线资源可用 */
} else {
  alert("离线资源不可用，必须联网。");
}
</pre>

<h3 id="Notes">备注</h3>

<div class="note">
 <p><strong>备注：</strong>查询的 URI 和当前页面的 URI 不同域的话，会抛出安全异常。</p>
</div>

<h3 id="Specification">规范</h3>

<p>无规范；这里有一些可用信息：<a href="http://www.campd.org/stuff/Offline%20Cache.html">将资源标记为离线可用</a>。</p>