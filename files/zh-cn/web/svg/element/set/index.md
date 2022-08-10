---
title: set
slug: Web/SVG/Element/set
tags:
  - SVG
  - SVG 动画
  - 元素
  - 需要兼容性表
  - 需要示例
translation_of: Web/SVG/Element/set
---
<div>{{SVGRef}}</div>

<p><code>set</code>元素可以用来设定一个属性值，并为该值赋予一个持续时间。它支持所有的属性类型， 包括那些原理上不能插值的， 例如值为字符串和布尔类型的属性。 set 元素是非叠加的。无法在其上使用 additive 属性或 accumulate 属性，即使声明了这些属性也会自动被忽略。</p>

<h2 id="用法">用法</h2>

<p>{{svginfo}}</p>

<h2 id="示例">示例</h2>

<h2 id="属性">属性</h2>

<h3 id="全局属性">全局属性</h3>

<ul>
 <li><a href="/en/SVG/Attribute#ConditionalProccessing">条件处理属性</a> »</li>
 <li><a href="/en/SVG/Attribute#Core">核心属性</a> »</li>
 <li><a href="/en/SVG/Attribute#AnimationEvent">动画事件属性</a> »</li>
 <li><a href="/en/SVG/Attribute#XLink">Xlink 属性</a> »</li>
 <li><a href="/en/SVG/Attribute#AnimationAttributeTarget">动画属性目标属性</a> »</li>
 <li><a href="/en/SVG/Attribute#AnimationTiming">动画定时属性</a> »</li>
 <li>{{ SVGAttr("externalResourcesRequired") }}</li>
</ul>

<h3 id="专有属性">专有属性</h3>

<ul>
 <li>{{ SVGAttr("to") }}</li>
</ul>

<h2 id="DOM_接口">DOM 接口</h2>

<p>该元素实现了<code><a href="/en/DOM/SVGSetElement">SVGSetElement</a></code> 接口。</p>

<h2 id="参见">参见</h2>

<ul>
 <li>{{ SVGElement("animate") }}</li>
</ul>