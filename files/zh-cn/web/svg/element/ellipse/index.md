---
title: ellipse
slug: Web/SVG/Element/ellipse
tags:
  - SVG
  - SVG 图形
  - 元素
  - 参考
translation_of: Web/SVG/Element/ellipse
---
<div>{{SVGRef}}</div>

<p><code>ellipse</code>元素是一个 SVG 基本形状，用来创建一个椭圆，基于一个中心坐标以及它们的<code>x</code>半径和<code>y</code>半径。</p>

<p>椭圆不能指定精确的椭圆倾向（假设，举个例子，你想画一个 45 度角倾斜的椭圆），但是可以利用{{ SVGAttr("transform") }}属性实现旋转。</p>

<h2 id="用法">用法</h2>

<p>{{svginfo}}</p>

<h2 id="示例">示例</h2>

<p>» <a href="https://developer.mozilla.org/files/3253/ellipse.svg">ellipse.svg</a></p>

<h2 id="属性">属性</h2>

<h3 id="全局属性">全局属性</h3>

<ul>
 <li><a href="/en-US/SVG/Attribute#ConditionalProccessing">条件处理属性</a> »</li>
 <li><a href="/en-US/SVG/Attribute#Core">核心属性</a> »</li>
 <li><a href="/en-US/SVG/Attribute#GraphicalEvent">图形事件属性</a> »</li>
 <li><a href="/en-US/SVG/Attribute#Presentation">外观属性</a> »</li>
 <li>{{ SVGAttr("class") }}</li>
 <li>{{ SVGAttr("style") }}</li>
 <li>{{ SVGAttr("externalResourcesRequired") }}</li>
 <li>{{ SVGAttr("transform") }}</li>
</ul>

<h3 id="专有属性">专有属性</h3>

<ul>
 <li>{{ SVGAttr("cx") }}</li>
 <li>{{ SVGAttr("cy") }}</li>
 <li>{{ SVGAttr("rx") }}</li>
 <li>{{ SVGAttr("ry") }}</li>
</ul>

<h2 id="DOM_接口">DOM 接口</h2>

<p>该元素实现了<code><a href="/en-US/DOM/SVGEllipseElement">SVGEllipseElement</a></code>接口。</p>

<h2 id="浏览器兼容性">浏览器兼容性</h2>

{{Compat("svg.elements.ellipse")}}

<h2 id="参见">参见</h2>

<ul>
 <li>{{ SVGElement("circle") }}</li>
</ul>