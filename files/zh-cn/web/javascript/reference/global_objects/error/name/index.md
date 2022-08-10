---
title: Error.prototype.name
slug: Web/JavaScript/Reference/Global_Objects/Error/name
translation_of: Web/JavaScript/Reference/Global_Objects/Error/name
---
<p>{{JSRef("Global_Objects", "Error", "EvalError,InternalError,RangeError,ReferenceError,SyntaxError,TypeError,URIError")}}</p>

<h2 id="Summary">概述</h2>

<p><code><strong>name</strong></code> 属性表示 error 类型的名称。初始值为"Error".</p>

<h2 id="Description">描述</h2>

<p>默认情况下，{{jsxref("Error")}}对象的<code>name</code>属性值为"Error".<code>name 属性和</code>{{jsxref("Error.prototype.message", "message")}}属性一起，通过调用{{jsxref("Error.prototype.toString()")}}方法，会作为最后异常信息的字符串表示。</p>

<h2 id="Examples">示例</h2>

<h3 id="Example:_Throwing_a_custom_error">例子：抛出一个自定义错误</h3>

<pre class="brush:js">var e = new Error("Malformed input"); // e.name 默认是"Error"

e.name = "ParseError";                // 修改之后，e.toString() 会成为下面这样的字符串
throw e;                              // "ParseError: Malformed input"
</pre>

<h2 id="规范">规范</h2>

{{Specifications}}

<h2 id="浏览器兼容性">浏览器兼容性</h2>

{{Compat}}

<h2 id="See_also">相关链接</h2>

<ul>
 <li>{{jsxref("Error.prototype.message")}}</li>
 <li>{{jsxref("Error.prototype.toString()")}}</li>
</ul>