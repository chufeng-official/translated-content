---
title: >-
  SyntaxError: Using //@ to indicate sourceURL pragmas is deprecated. Use //#
  instead
slug: Web/JavaScript/Reference/Errors/Deprecated_source_map_pragma
tags:
  - Errors
  - JavaScript
  - Source maps
translation_of: Web/JavaScript/Reference/Errors/Deprecated_source_map_pragma
---
<div>{{jsSidebar("Errors")}}</div>

<h2 id="信息">信息</h2>

<pre class="syntaxbox">Warning: SyntaxError: Using //@ to indicate sourceURL pragmas is deprecated. Use //# instead

Warning: SyntaxError: Using //@ to indicate sourceMappingURL pragmas is deprecated. Use //# instead
</pre>

<h2 id="错误类型">错误类型</h2>

<p>{{jsxref("SyntaxError")}} 的警告。不会终止 JavaScript 的执行。</p>

<h2 id="哪里错了">哪里错了？</h2>

<p>在 JavaScript 源码中使用了已废弃的 source map 语法。</p>

<p>JavaScript 源代码经常被组合和压缩，以便能更高效地从服务器获取它们。使用了 <a href="http://www.html5rocks.com/en/tutorials/developertools/sourcemaps/">source maps</a>，调试器就可以将正在执行的代码映射到原始源文件。</p>

<p>因为在 IE 浏览器中，只要页面存在 <code>//@cc_on</code> 注释，都会被 IE JScript 引擎解释为要打开条件编译，所以 source map 的规范更改了语法。<a href="https://msdn.microsoft.com/en-us/library/8ka90k2e%28v=vs.94%29.aspx">条件编译注释</a> 是 IE 的一个鲜为人知的特性，但是它破坏了 <a href="https://bugs.jquery.com/ticket/13274">jQuery</a> 和其他库的 source map。</p>

<h2 id="示例">示例</h2>

<h3 id="废弃的语法">废弃的语法</h3>

<p>使用 "@" 符号的语法已经被废弃了。</p>

<pre class="brush: js example-bad">//@ sourceMappingURL=http://example.com/path/to/your/sourcemap.map
</pre>

<h3 id="标准语法">标准语法</h3>

<p>使用 "#" 符号代替。</p>

<pre class="brush: js example-good">//# sourceMappingURL=http://example.com/path/to/your/sourcemap.map</pre>

<p>或者，您也可以为 JavaScript 文件设置 header，以避免添加注释：</p>

<pre class="brush: js example-good">X-SourceMap: /path/to/file.js.map</pre>

<h2 id="参见">参见</h2>

<ul>
 <li><a href="/en-US/docs/Tools/Debugger/How_to/Use_a_source_map">How to use a source map – Firefox Tools documentation</a></li>
 <li><a href="http://www.html5rocks.com/en/tutorials/developertools/sourcemaps/">Introduction to source maps – HTML5 rocks</a></li>
</ul>