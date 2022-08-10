---
title: WebGLUniformLocation
slug: Web/API/WebGLUniformLocation
tags:
  - API
  - WebGL
  - WebGLUniformLocation
translation_of: Web/API/WebGLUniformLocation
---
<div>{{APIRef("WebGL")}}</div>

<p><strong>WebGLUniformLocation</strong> 接口是 <a href="/en-US/docs/Web/API/WebGL_API">WebGL API</a> 的一部分，在一个着色器程序中表示一个统一变量的位置。</p>

<h2 id="说明">说明</h2>

<p><code>WebGLUniformLocation</code> 对象未定义任何属于自己并能直接访问其内容的方法和属性。在使用 <code>WebGLUniformLocation</code> 对象时，{{domxref("WebGLRenderingContext")}} 的方法是有用的：</p>

<ul>
 <li>{{domxref("WebGLRenderingContext.getUniformLocation()")}}</li>
 <li>{{domxref("WebGLRenderingContext.uniform()")}}</li>
</ul>

<h2 id="示例">示例</h2>

<h3 id="获取一个统一位置">获取一个统一位置</h3>

<pre class="brush: js">var canvas = document.getElementById("canvas");
var gl = canvas.getContext("webgl");

var location = gl.getUniformLocation(WebGLProgram, "uniformName");</pre>

<h2 id="规范">规范</h2>

{{Specifications}}

<h2 id="浏览器兼容性">浏览器兼容性</h2>

{{Compat}}

<h2 id="参见">参见</h2>

<ul>
 <li>{{domxref("WebGLRenderingContext.getUniformLocation()")}}</li>
</ul>