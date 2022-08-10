---
title: Set.prototype.forEach()
slug: Web/JavaScript/Reference/Global_Objects/Set/forEach
translation_of: Web/JavaScript/Reference/Global_Objects/Set/forEach
---
<div>{{JSRef}}</div>

<p><code>forEach</code> 方法会根据集合中元素的插入顺序，依次执行提供的回调函数。</p>

<h2 id="语法">语法</h2>

<pre class="syntaxbox"><code><em>mySet</em>.forEach(<em>callback</em>[, <em>thisArg</em>])</code></pre>

<h3 id="参数">参数</h3>

<dl>
 <dt><code>callback</code></dt>
 <dd>为集合中每个元素执行的回调函数，该函数接收三个参数：
 <dl>
  <dt><strong><code>currentValue</code>, </strong><strong><code>currentKey{{optional_inline}}</code></strong></dt>
  <dd><strong>currentValue</strong> 是正在被操作的元素。并且由于集合没有索引，所以 <strong>currentKey</strong> 也表示这个正在被操作的元素。</dd>
  <dt><strong><code>set{{optional_inline}}</code></strong></dt>
  <dd>调用当前 <code>forEach</code> 方法的集合对象</dd>
 </dl>
 </dd>
 <dt><code>thisArg</code><strong><code>{{optional_inline}}</code></strong></dt>
 <dd>回调函数执行过程中的 <code>this</code> 值。</dd>
</dl>

<h3 id="返回值">返回值</h3>

<p>{{jsxref("undefined")}}.</p>

<h2 id="描述">描述</h2>

<p><code>forEach</code> 方法会依次为集合中的元素执行回调函数，就算元素的值是 <code>undefined </code>。</p>

<p><strong>回调函数</strong>有三个参数：</p>

<ul>
 <li>元素的值</li>
 <li>元素的索引</li>
 <li>正在遍历的集合对象</li>
</ul>

<p>但是由于集合对象中没有索引 (keys)，所以前两个参数都是{{domxref("Set")}}中元素的值 (<strong>values</strong>)，之所以这样设计回调函数是为了和{{jsxref("Map.foreach", "Map")}} 以及{{jsxref("Array.forEach","Array")}}的 <code>forEach</code> 函数用法保持一致。</p>

<p>如果提供了一个 <code>thisArg</code> 参数给 <code>forEach</code> 函数，则参数将会作为回调函数中的 <code>this</code>值。否则 <code>this</code> 值为 <code>undefined</code>。回调函数中 <code>this</code> 的绑定是根据<a href="https://developer.mozilla.org/zh-CN/docs/Web/JavaScript/Reference/Operators/this">函数被调用时通用的 <code>this</code> 绑定规则来决定的</a>。</p>

<p><code>forEach</code> 函数为集合对象中每个元素都执行一次回调；它不会返回任何值。</p>

<h2 id="例子">例子</h2>

<h3 id="输出集合对象的内容">输出集合对象的内容</h3>

<p>以下代码依次打印集合对象的元素：</p>

<pre class="brush:js">function logSetElements(value1, value2, set) {
    console.log("s[" + value1 + "] = " + value2);
}

new Set(["foo", "bar", undefined]).forEach(logSetElements);

// logs:
// "s[foo] = foo"
// "s[bar] = bar"
// "s[undefined] = undefined"
</pre>

<h2 id="规范">规范</h2>

{{Specifications}}

<h2 id="浏览器兼容性">浏览器兼容性</h2>

{{Compat}}

<h2 id="参见">参见</h2>

<ul>
 <li>{{jsxref("Array.prototype.forEach()")}}</li>
 <li>{{jsxref("Map.prototype.forEach()")}}</li>
</ul>