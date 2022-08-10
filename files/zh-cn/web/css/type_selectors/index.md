---
title: 元素选择器
slug: Web/CSS/Type_selectors
tags:
  - CSS
  - Selectors
translation_of: Web/CSS/Type_selectors
---
<div>{{ CSSRef }}</div>

<h2 id="Summary">概述</h2>

<p>CSS 元素选择器 (也称为类型选择器) 通过 node 节点名称匹配元素。因此，在单独使用时，寻找特定类型的元素时，元素选择器都会匹配该文档中所有此类型的元素。</p>

<h2 id="Syntax">语法</h2>

<pre class="syntaxbox">元素 {<em>样式声明</em> }
</pre>

<h2 id="Examples">示例</h2>

<h3 id="CSS">CSS</h3>

<pre class="brush: css">span {
  background-color: DodgerBlue;
  color: #ffffff;
}
</pre>

<h3 id="HTML">HTML</h3>

<pre class="brush: html">  &lt;span&gt;这里是由 span 包裹的一些文字.&lt;/span&gt;
  &lt;p&gt;这里是由 p 包裹的一些文字.&lt;/p&gt;
</pre>

<h3 id="效果">效果</h3>

<p>这里是由 span 包裹的一些文字。<br>
 这里是由 p 包裹的一些文字。</p>

<h2 id="Specifications">规范</h2>

{{Specifications}}

<h2 id="浏览器兼容性">浏览器兼容性</h2>

{{Compat("css.selectors.type")}}

<h2 id="See_also">See also</h2>