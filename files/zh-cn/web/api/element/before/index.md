---
title: Element.before()
slug: Web/API/Element/before
tags:
  - API
  - DOM
  - Method
  - Node
  - Reference
translation_of: Web/API/Element/before
original_slug: Web/API/ChildNode/before
browser-compat: api.Element.before
---
<div>{{APIRef("DOM")}} {{SeeCompatTable}}</div>

<p> <code><strong>ChildNode</strong></code><strong><code>.before</code></strong> 方法可以在<code>ChildNode</code> 这个节点的父节点中插入一些列的 {{domxref("Node")}} 或者 {{domxref("DOMString")}} 对象，位置就是在<code>ChildNode</code> 节点的前面，{{domxref("DOMString")}} 对象其实和 {{domxref("Text")}} 节点一样的方式来完成插入的。</p>

<h2 id="语法">语法</h2>

<pre class="syntaxbox">[Throws, Unscopable]
void Element.before((Node or DOMString)... nodes);
</pre>

<h3 id="Parameters参数">Parameters 参数</h3>

<dl>
 <dt><code>nodes</code></dt>
 <dd>一系列的 {{domxref("Node")}} 或者 {{domxref("DOMString")}} </dd>
</dl>

<h3 id="Exceptions">Exceptions</h3>

<ul>
 <li>{{domxref("HierarchyRequestError")}}: 当节点插入了错误的层级就会出现报错，需要遵循 html 标签的层级关系，</li>
</ul>

<h2 id="Examples事例">Examples 事例</h2>

<h3 id="Inserting_an_element插入元素节点">Inserting an element 插入元素节点</h3>

<pre class="brush: js">var parent = document.createElement("div");
var child = document.createElement("p");
parent.appendChild(child);
var span = document.createElement("span");

child.before(span);

console.log(parent.outerHTML);
// "&lt;div&gt;&lt;span&gt;&lt;/span&gt;&lt;p&gt;&lt;/p&gt;&lt;/div&gt;"
</pre>

<h3 id="Inserting_text插入文本节点">Inserting text 插入文本节点</h3>

<pre class="brush: js">var parent = document.createElement("div");
var child = document.createElement("p");
parent.appendChild(child);

child.before("Text");

console.log(parent.outerHTML);
// "&lt;div&gt;Text&lt;p&gt;&lt;/p&gt;&lt;/div&gt;"</pre>

<h3 id="Inserting_an_element_and_text同时插入文本和元素">Inserting an element and text 同时插入文本和元素</h3>

<pre class="brush: js">var parent = document.createElement("div");
var child = document.createElement("p");
parent.appendChild(child);
var span = document.createElement("span");

child.before(span, "Text");

console.log(parent.outerHTML);
// "&lt;div&gt;&lt;span&gt;&lt;/span&gt;Text&lt;p&gt;&lt;/p&gt;&lt;/div&gt;"</pre>

<h3 id="Element.before()_is_unscopable不可使用区域"><code>Element.before()</code> is unscopable 不可使用区域</h3>

<p>The <code>before()</code> 不能配合 with 声明使用，See {{jsxref("Symbol.unscopables")}} for more information.</p>

<pre class="brush: js">with(node) {
  before("foo");
}
// ReferenceError: before is not defined </pre>

<h2 id="Polyfill">Polyfill</h2>

<p>兼容 ie9 或者更高版本的方法，You can polyfill the <code>before() method</code> in Internet Explorer 9 and higher with the following code:</p>

<pre class="brush: js">// from: https://github.com/jserz/js_piece/blob/master/DOM/ChildNode/before()/before().md
(function (arr) {
  arr.forEach(function (item) {
    if (item.hasOwnProperty('before')) {
      return;
    }
    Object.defineProperty(item, 'before', {
      configurable: true,
      enumerable: true,
      writable: true,
      value: function before() {
        var argArr = Array.prototype.slice.call(arguments),
          docFrag = document.createDocumentFragment();

        argArr.forEach(function (argItem) {
          var isNode = argItem instanceof Node;
          docFrag.appendChild(isNode ? argItem : document.createTextNode(String(argItem)));
        });

        this.parentNode.insertBefore(docFrag, this);
      }
    });
  });
})([Element.prototype, CharacterData.prototype, DocumentType.prototype]);</pre>

<h2 id="Specification">Specification</h2>

{{Specifications}}

<h2 id="Browser_compatibility">Browser compatibility</h2>

{{Compat("api.Element.before")}}

<h2 id="See_also">See also</h2>

<ul>
 <li>{{domxref("ChildNode")}} and {{domxref("ParentNode")}}</li>
 <li>{{domxref("ChildNode.after()")}}</li>
 <li>{{domxref("ParentNode.append()")}}</li>
 <li>{{domxref("Node.appendChild()")}}</li>
 <li>{{domxref("Node.insertBefore()")}}</li>
 <li>{{domxref("NodeList")}}</li>
</ul>