---
title: window.frameElement
slug: Web/API/Window/frameElement
translation_of: Web/API/Window/frameElement
---
<p>{{ ApiRef() }}</p>
<h3 id="Summary">概述</h3>
<p>返回嵌入当前<code>window</code>对象的元素 (比如 <code>&lt;iframe&gt;</code> 或者 <code>&lt;object&gt;</code>),如果当前<code>window</code>对象已经是顶层窗口，则返回<code>null</code>.</p>
<h3 id="Syntax">语法</h3>
<pre class="eval">var <em>frameEl</em> = window.frameElement;
</pre>
<h3 id="Example">例子</h3>
<pre class="eval">var frameEl = window.frameElement;
// 如果当前窗口被包含在一个框架里面，则将该框架的地址跳到'http://mozilla.org/'
if (frameEl)
  frameEl.src = 'http://mozilla.org/';
</pre>
<h3 id="Notes">备注</h3>
<p>虽然该属性名为<code>frameElement</code>,但该属性也会返回其他类型比如 <code>&lt;object&gt;</code> 或者其他可嵌入窗口的元素。</p>
<h3 id="See_also">相关链接</h3>
<ul>
 <li><code><a href="/zh-cn/DOM/window.frames">window.frames</a></code> 返回一个类数组对象，返回当前窗口的所有子框架元素。</li>
 <li><code><a href="/zh-cn/DOM/window.parent">window.parent</a></code> 返回当前窗口的父窗口，也就是说，包含当前窗口所在的<code>frameElement</code>元素的窗口。</li>
</ul>
<h3 id="Specification">规范</h3>
<p><a href="http://www.whatwg.org/specs/web-apps/current-work/#dom-frameelement">WHATWG</a></p>
<h3 id="浏览器兼容性">浏览器兼容性</h3>
{{Compat("api.Window.frameElement")}}