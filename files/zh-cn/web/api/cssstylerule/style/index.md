---
title: style
slug: Web/API/CSSStyleRule/style
translation_of: Web/API/CSSStyleRule/style
---
<p>{{ ApiRef() }}</p>

<h3 id="Summary">概述</h3>

<p>返回 一个 {{ domxref("CSSStyleDeclaration") }}接口对象，它代表了{{ DOMXref("CSSRule") }}的 <a href="http://www.w3.org/TR/1998/REC-CSS2-19980512/syndata.html#block">declaration block</a>。</p>

<h3 id="Syntax">语法</h3>

<pre class="eval notranslate"><em>styleObj</em> = <em>cssRule</em>.style
</pre>

<h3 id="Example">例子</h3>

<pre class="brush: js notranslate">function stilo() {
  alert(document.styleSheets[0].cssRules[0].style.cssText);
}
// 弹出 "background-color: gray;"
</pre>

<h3 id="Notes">备注</h3>

<p>declaration block 是样式规则中花括号内的部分（选择器就在花括号的外部）</p>

<h3 id="相关链接">相关链接</h3>

<ul>
 <li><a href="/zh-cn/CSS/CSS_Reference">DOM CSS Properties</a></li>
</ul>

<h3 id="Specification">规范</h3>

<p><a href="http://www.w3.org/TR/DOM-Level-2-Style/css.html#CSS-CSSStyleRule-style">DOM Level 2 CSS: style</a></p>

<h3 id="Specification">浏览器兼容性</h3>

<p>{{Compat("api.CSSStyleRule.style")}}</p>