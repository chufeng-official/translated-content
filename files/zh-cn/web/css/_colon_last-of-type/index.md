---
title: ':last-of-type'
slug: 'Web/CSS/:last-of-type'
translation_of: 'Web/CSS/:last-of-type'
---
<p>{{ CSSRef() }}</p>

<h2 id="概述">概述</h2>

<p><code>:last-of-type</code> <a href="/zh-CN/CSS/Pseudo-classes">CSS 伪类</a> 表示了在（它父元素的）子元素列表中，最后一个给定类型的元素。当代码类似 Parent tagName:last-of-type 的作用区域包含父元素的所有子元素中的最后一个选定元素，也包括子元素的最后一个子元素并以此类推。</p>

<h2 id="语法">语法</h2>

<pre class="eval">element:last-of-type { <em>style properties</em> }
</pre>

<h2 id="示例">示例</h2>

<pre class="brush: css">p em:last-of-type {
  color: lime;
}
</pre>

<pre class="brush: html">&lt;p&gt;
  &lt;em&gt;我没有颜色 :(&lt;/em&gt;&lt;br&gt;
  &lt;strong&gt;我没有颜色 :(&lt;/strong&gt;&lt;br&gt;
  &lt;em&gt;我有颜色 :D&lt;/em&gt;&lt;br&gt;
  &lt;strong&gt;我也没有颜色 :(&lt;/strong&gt;&lt;br&gt;
&lt;/p&gt;

&lt;p&gt;
  &lt;em&gt;我没有颜色 :(&lt;/em&gt;&lt;br&gt;
  &lt;span&gt;&lt;em&gt;我有颜色！&lt;/em&gt;&lt;/span&gt;&lt;br&gt;
  &lt;strong&gt;我没有颜色 :(&lt;/strong&gt;&lt;br&gt;
  &lt;em&gt;我有颜色 :D&lt;/em&gt;&lt;br&gt;
  &lt;span&gt;
    &lt;em&gt;我在子元素里，但没有颜色！&lt;/em&gt;&lt;br&gt;
    &lt;span style="text-decoration:line-through;"&gt; 我没有颜色 &lt;/span&gt;&lt;br&gt;
    &lt;em&gt;我却有颜色！&lt;/em&gt;&lt;br&gt;
  &lt;/span&gt;&lt;br&gt;
  &lt;strong&gt;我也没有颜色 :(&lt;/strong&gt;
&lt;/p&gt;</pre>

<p>结果如下：</p>

<div>{{EmbedLiveSample('示例','100%','330')}}</div>

<h2 id="规范">规范</h2>

{{Specifications}}

<h2 id="浏览器兼容性">浏览器兼容性</h2>
<div>


<p>{{Compat("css.selectors.last-of-type")}}</p>
</div>

<h2 id="参见">参见</h2>

<ul>
 <li>{{ Cssxref(":nth-last-of-type") }}</li>
 <li>{{ Cssxref(":first-of-type") }}</li>
 <li>{{ Cssxref(":nth-of-type") }}</li>
</ul>