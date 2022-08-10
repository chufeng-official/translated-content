---
title: Reflect.getOwnPropertyDescriptor()
slug: Web/JavaScript/Reference/Global_Objects/Reflect/getOwnPropertyDescriptor
translation_of: Web/JavaScript/Reference/Global_Objects/Reflect/getOwnPropertyDescriptor
---
<div>{{JSRef}}</div>

<p>静态方法 <code><strong>Reflect</strong></code><strong><code>.getOwnPropertyDescriptor()</code></strong> 与 {{jsxref("Object.getOwnPropertyDescriptor()")}} 方法相似。如果在对象中存在，则返回给定的属性的属性描述符。否则返回 {{jsxref("undefined")}}。 </p>

<h2 id="语法">语法</h2>

<pre class="syntaxbox">Reflect.getOwnPropertyDescriptor(target, propertyKey)
</pre>

<h3 id="参数">参数</h3>

<dl>
 <dt><code>target</code></dt>
 <dd>需要寻找属性的目标对象。</dd>
 <dt><code>propertyKey</code></dt>
 <dd>获取自己的属性描述符的属性的名称。</dd>
</dl>

<h3 id="返回值">返回值</h3>

<p>如果属性存在于给定的目标对象中，则返回属性描述符；否则，返回 {{jsxref("undefined")}}。</p>

<h3 id="异常">异常</h3>

<p>抛出一个 {{jsxref("TypeError")}}，如果目标不是 {{jsxref("Object")}}。</p>

<h2 id="描述">描述</h2>

<p><code>Reflect.getOwnPropertyDescriptor</code>方法返回一个属性描述符，如果给定的属性存在于对象中，否则返回 {{jsxref("undefined")}} 。 与  {{jsxref("Object.getOwnPropertyDescriptor()")}} 的唯一不同在于如何处理非对象目标。</p>

<h2 id="示例">示例</h2>

<h3 id="使用_Reflect.getOwnPropertyDescriptor()">使用 <code>Reflect.getOwnPropertyDescriptor()</code></h3>

<pre class="brush: js">Reflect.getOwnPropertyDescriptor({x: "hello"}, "x");
// {value: "hello", writable: true, enumerable: true, configurable: true}

Reflect.getOwnPropertyDescriptor({x: "hello"}, "y");
// undefined

Reflect.getOwnPropertyDescriptor([], "length");
// {value: 0, writable: true, enumerable: false, configurable: false}
</pre>

<h3 id="与_Object.getOwnPropertyDescriptor()_的不同点">与 <code>Object.getOwnPropertyDescriptor() 的不同点</code></h3>

<p>如果该方法的第一个参数不是一个对象（一个原始值），那么将造成 {{jsxref("TypeError")}} 错误。而对于 {{jsxref("Object.getOwnPropertyDescriptor")}}，非对象的第一个参数将被强制转换为一个对象处理。</p>

<pre class="brush: js">Reflect.getOwnPropertyDescriptor("foo", 0);
// TypeError: "foo" is not non-null object

Object.getOwnPropertyDescriptor("foo", 0);
// { value: "f", writable: false, enumerable: true, configurable: false }</pre>

<h2 id="规范">规范</h2>

{{Specifications}}

<h2 id="浏览器兼容性">浏览器兼容性</h2>

{{Compat}}

<h2 id="相关链接">相关链接</h2>

<ul>
 <li>{{jsxref("Reflect")}}</li>
 <li>{{jsxref("Object.getOwnPropertyDescriptor()")}}</li>
</ul>