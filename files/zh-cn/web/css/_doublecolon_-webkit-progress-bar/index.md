---
title: '::-webkit-progress-bar'
slug: 'Web/CSS/::-webkit-progress-bar'
tags:
  - CSS
  - 非标准特性
translation_of: 'Web/CSS/::-webkit-progress-bar'
---
<div>{{CSSRef}}{{Non-standard_header}}</div>

<h2 id="概述">概述</h2>

<p><strong><code>::-webkit-progress-bar</code></strong> <a href="/en-US/docs/Web/CSS">CSS</a> <a href="/en-US/docs/Web/CSS/Pseudo-elements">伪元素</a> 选择 {{HTMLElement("progress")}} 元素的未完成部分。 {{ cssxref("::-webkit-progress-value") }} 选择完成的部分。<strong><code>::-webkit-progress-bar</code></strong> 是{{cssxref("::-webkit-progress-inner-element")}} 伪元素的子元素，同时是 {{cssxref("::-webkit-progress-value")}} 伪元素的父元素。</p>

<div class="note">
<p><strong>Note:</strong> 为了能让<code>::-webkit-progress-value</code>起作用，需要添加 CSS {{cssxref("-webkit-appearance")}} 至 <code>&lt;progress&gt;</code> 元素。</p>
</div>

<h2 id="规范">规范</h2>

<p>没有规范。这是一个 WebKit/Blink 独有的规范。</p>

<h2 id="例子">例子</h2>

<h3 id="CSS_content">CSS content</h3>

<pre class="brush: css notranslate">progress {
  -webkit-appearance: none;
}

::-webkit-progress-bar {
   background-color: orange;
}
</pre>

<h3 id="HTML_content">HTML content</h3>

<pre class="brush: html notranslate">&lt;progress value="10" max="50"&gt;
</pre>

<h3 id="Output">Output</h3>

<p>{{EmbedLiveSample("Example", 200, 50)}}</p>

<p>应用了上述样式的进度条样式如下：</p>

<p><img src="progress-bar.png"></p>

<h2 id="浏览器兼容性">浏览器兼容性</h2>

{{Compat("css.selectors.-webkit-progress-bar")}}

<h2 id="参见">参见</h2>

<ul>
 <li>The pseudo-elements used by WebKit/Blink to style other parts of a {{HTMLElement("progress")}} element:
  <ul>
   <li>{{ cssxref("::-webkit-progress-value") }}</li>
   <li>{{ cssxref("::-webkit-progress-inner-element") }}</li>
  </ul>
 </li>
 <li>{{ cssxref("::-moz-progress-bar") }}</li>
 <li>{{ cssxref("::-ms-fill") }}</li>
</ul>