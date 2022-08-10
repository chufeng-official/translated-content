---
title: column-count
slug: Web/CSS/column-count
tags:
  - CSS3 Multiple column layout
  - CSS3 多列布局
translation_of: Web/CSS/column-count
---
<div>{{CSSRef}}</div>

<div> </div>

<p><strong>column-count </strong>CSS 属性，描述元素的列数。</p>

<pre><code>column-count: 3;
column-count: auto;

column-count: inherit;
column-count: initial;
column-count: unset;</code></pre>

<h2 id="Syntax">语法</h2>

<p>{{cssinfo}}</p>

<h3 id="取值">取值</h3>

<dl>
 <dt><code>auto</code></dt>
 <dd>用来表示列的数量由其他 CSS 属性指定，例如 {{cssxref("column-width")}}.</dd>
 <dt><code>&lt;number&gt;</code></dt>
 <dd>是个严格的正数 {{cssxref("&lt;integer&gt;")}} ，用来描述元素内容被划分的理想列数。假如 {{cssxref("column-width")}}也被设置为非零值，此参数仅表示所允许的最大列数. </dd>
</dl>

<h2 id="Examples">例子</h2>

<pre class="brush: css">.content-box {
  border: 10px solid #000000;
  column-count:3;
}
</pre>

<h2 id="Specifications">规范</h2>

{{Specifications}}

<h2 id="Browser_compatibility">浏览器兼容性</h2>

{{Compat("css.properties.column-count")}}