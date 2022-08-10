---
title: Document.dir
slug: Web/API/Document/dir
translation_of: Web/API/Document/dir
---
<p>{{ApiRef("")}}</p>

<p>Document.dir 的本质是 DOMString，代表了文档的文字朝向，是从左到右 (默认) 还是从右到左。</p>

<p>'rtl'(right to left) 代表从右到左，'ltr'(left to right) 代表从左到右。</p>

<h2 id="语法">语法</h2>

<pre class="syntaxbox">console.log(document.dir);// "" (译者添加)
document.dir = "ltr"//(默认);
document.dir = "rtl";
<em>dirStr</em> = <em>document.</em>dir;
<em>document.dir</em> = <em>dirStr;</em>
</pre>

<p>（译者注：第一次调用该属性时，可能返回空字符串""，译者环境：chrome，版本 53.0.2785.116 m）</p>

<h2 id="Specifications">说明</h2>

{{Specifications}}

<h2 id="浏览器兼容性">浏览器兼容性</h2>

{{Compat("api.Document.dir")}}

<h2 id="参见">参见</h2>

<ul>
 <li><a href="http://msdn.microsoft.com/en-us/library/ms533731.aspx">http://msdn.microsoft.com/en-us/library/ms533731.aspx</a></li>
</ul>