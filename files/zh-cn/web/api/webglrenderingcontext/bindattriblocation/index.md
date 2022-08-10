---
title: WebGLRenderingContext.bindAttribLocation()
slug: Web/API/WebGLRenderingContext/bindAttribLocation
tags:
  - WebGL
  - WebGLRenderingContext
translation_of: Web/API/WebGLRenderingContext/bindAttribLocation
---
<p>{{APIRef("WebGL")}}</p>

<p>WebGL API 的 WebGLRenderingContext.bindAttribLocation（）方法将通用顶点索引绑定到属性变量。</p>

<h2 id="语法">语法</h2>

<pre>void <var>gl</var>.bindAttribLocation(<var>program</var>, <var>index</var>, <var>name</var>);
</pre>

<h3 id="参数">参数</h3>

<dl>
 <dt><code>program</code></dt>
 <dd>要绑定的{{domxref("WebGLProgram")}} 对象。</dd>
 <dt>index</dt>
 <dd>{{domxref("GLuint")}} 指定要绑定的通用顶点的索引。</dd>
 <dt>name</dt>
 <dd>{{domxref("DOMString")}}指定要绑定到通用顶点索引的变量的名称。 该名称不能以“webgl_”或“_webgl_”开头，因为这些名称将保留供 WebGL 使用。</dd>
</dl>

<h3 id="返回值">返回值</h3>

<p>None.</p>

<h2 id="示例">示例</h2>

<pre>gl.bindAttribLocation(program, colorLocation, 'vColor');
</pre>

<h2 id="规范">规范</h2>

{{Specifications}}

<h2 id="浏览器兼容性">浏览器兼容性</h2>

<p>{{Compat}}</p>

<h2 id="另见">另见</h2>

<ul>
 <li>{{domxref("WebGLRenderingContext.getActiveAttrib()")}}</li>
 <li>{{domxref("WebGLRenderingContext.getAttribLocation()")}}</li>
 <li>{{domxref("WebGLRenderingContext.getVertexAttrib()")}}</li>
</ul>