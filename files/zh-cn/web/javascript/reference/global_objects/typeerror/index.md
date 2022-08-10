---
title: TypeError
slug: Web/JavaScript/Reference/Global_Objects/TypeError
tags:
  - Error
  - JavaScript
  - Object
  - Reference
  - Référence(2)
  - TypeError
  - 参考
  - 类型错误
translation_of: Web/JavaScript/Reference/Global_Objects/TypeError
---
<div>{{JSRef}}</div>

<p><code><strong>TypeError（类型错误）</strong></code> 对象用来表示值的类型非预期类型时发生的错误。</p>

<h2 id="Syntax">语法</h2>

<pre class="syntaxbox"><code>new TypeError([<var>message</var>[, <var>fileName</var>[, <var>lineNumber</var>]]])</code></pre>

<h3 id="Parameters">参数</h3>

<dl>
 <dt><code>message 消息</code></dt>
 <dd>可选。描述此错误</dd>
 <dt><code>fileName 文件名</code> {{non-standard_inline}}</dt>
 <dd>可选。引起该异常的代码所在的文件的名字。</dd>
 <dt><code>lineNumber 行号</code> {{non-standard_inline}}</dt>
 <dd>可选。引起该异常的代码的行号。</dd>
</dl>

<h2 id="Description">描述</h2>

<p>当传入函数的<strong>操作数</strong>或<strong>参数</strong>的类型并非操作符或函数所预期的类型时，将抛出一个 TypeError 类型错误。</p>

<h2 id="Properties">属性</h2>

<dl>
 <dt>{{jsxref("TypeError.prototype")}}</dt>
 <dd>允许为一个 TypeError 类型错误附加属性。</dd>
</dl>

<h2 id="Methods">方法</h2>

<p>全局 TypeError 不包含任何方法，不过，它将从原型链中继承一些方法。</p>

<h2 id="TypeError_instances"><code>TypeError</code> 类型错误实例</h2>

<h3 id="Properties_of_TypeError_instances">属性</h3>

<div>{{page('/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/TypeError/prototype', '属性')}}</div>

<h3 id="Methods_of_TypeError_instances">方法</h3>

<div>{{page('/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/TypeError/prototype', '方法')}}</div>

<h2 id="Examples">示例</h2>

<h3 id="Example:_Catch_an_TypeError">示例：捕获类型错误</h3>

<pre class="brush: js">try {
  null.f();
} catch (e) {
  console.log(e instanceof TypeError); // true
  console.log(e.message);              // "null has no properties"
  console.log(e.name);                 // "TypeError"
  console.log(e.fileName);             // "Scratchpad/1"
  console.log(e.lineNumber);           // 2
  console.log(e.columnNumber);         // 2
  console.log(e.stack);                // "@Scratchpad/2:2:3\n"
}
</pre>

<h3 id="Example:_Create_an_TypeError">示例：创建一个类型错误</h3>

<pre class="brush: js">try {
  throw new TypeError('Hello', "someFile.js", 10);
} catch (e) {
  console.log(e instanceof TypeError); // true
  console.log(e.message);              // "Hello"
  console.log(e.name);                 // "TypeError"
  console.log(e.fileName);             // "someFile.js"
  console.log(e.lineNumber);           // 10
  console.log(e.columnNumber);         // 0
  console.log(e.stack);                // "@Scratchpad/2:2:9\n"
}
</pre>

<h2 id="规范">规范</h2>

{{Specifications}}

<h2 id="浏览器兼容性">浏览器兼容性</h2>

<div>{{Compat}}</div>

<h2 id="相关链接">相关链接</h2>

<ul>
 <li>{{jsxref("Error")}}</li>
 <li>{{jsxref("TypeError.prototype")}}</li>
</ul>