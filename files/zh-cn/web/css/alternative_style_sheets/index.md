---
title: Alternative style sheets
slug: Web/CSS/Alternative_style_sheets
translation_of: Web/CSS/Alternative_style_sheets
---
<div>{{cssref}}</div>

<p>Specifying <strong>alternative style sheets</strong> in a web page provides a way for users to see multiple versions of a page, based on their needs or preferences.</p>

<p>在网页中指定可替代样式表允许用户为网页选择他们喜欢的样式。</p>

<p>Firefox lets the user select the stylesheet using the <em>View &gt; Page Style</em> submenu. Internet Explorer also supports this feature (beginning with IE 8), also accessed from <em>View &gt; Page Style</em>. Chrome requires an extension to use the feature (as of version 48). The web page can also provide its own user interface to let the user switch styles.</p>

<p>Firefox 允许用户通过菜单栏中 查看 &gt; 页面样式 选择样式表。Internet Explorer 也支持这一功能（从 IE8 开始）（菜单栏 查看 &gt; 页面样式）。网页也可提供自己的用户界面让用户</p>

<p>在 Firefox 和 Internet Explorer（从 IE8（6？）开始）中，用户可以通过菜单栏中的 查看 &gt; 页面样式 来选择网页的样式。网页也可以提供选择样式的界面。</p>

<h2 id="An_example_specifying_the_alternative_stylesheets">An example: specifying the alternative stylesheets</h2>

<h2 id="示例：提供可替代样式表">示例：提供可替代样式表</h2>

<p>The alternate stylesheets are commonly specified using a {{HTMLElement("link")}} element with <code>rel="alternate stylesheet"</code> and <code>title="..."</code> attributes. For example:</p>

<p>一般使用&lt;{{HTMLElement("link")}}&gt;指定可替换样式表。在这个标签中指定<code>rel="alternate stylesheet"</code> 属性和 <code>title="..."</code>属性</p>

<pre class="brush: html">&lt;link href="reset.css" rel="stylesheet" type="text/css"&gt;

&lt;link href="default.css" rel="stylesheet" type="text/css" title="Default Style"&gt;
&lt;link href="fancy.css" rel="alternate stylesheet" type="text/css" title="Fancy"&gt;
&lt;link href="basic.css" rel="alternate stylesheet" type="text/css" title="Basic"&gt;
</pre>

<p>In this example, the styles "Default Style", "Fancy", and "Basic" will be listed in the <em>Page Style</em> submenu, with "Default Style" pre-selected. When the user selects a different style, the page will immediately be re-rendered using that style sheet.</p>

<p>在此例中，“页面样式”菜单中会出现“Default Style”、“Fancy”和“Basic”的选项。“Default Style”默认选中。如果用户选择一个不同的样式，浏览器就使用用户选择的样式。</p>

<p>No matter what style is selected, the rules from the reset.css stylesheet will always be applied.</p>

<p>无论用户选择何种样式，reset.css 总会被应用。</p>

<h3 id="尝试">尝试</h3>

<p><a href="/samples/cssref/altstyles/index.html">Click here</a> for a working example you can try out.</p>

<p><a href="https://mdn.github.io/css-examples/alt-style-sheets/">点击此处</a>进入示例。</p>

<h2 id="细节">细节</h2>

<p>网页中的样式表分为三类：</p>



<p>Any stylesheet in a document falls into one of the following categories:</p>

<ul>
 <li><strong>Persistent</strong> (no <code>rel="alternate"</code>, no <code>title=""</code>): always applies to the document.</li>
 <li><strong>Preferred</strong> (no <code>rel="alternate"</code>, with <code>title="..."</code> specified): applied by default, but {{domxref("StyleSheet.disabled", "disabled", "", 1)}} if an alternate stylesheet is selected. <strong>There can only be one preferred stylesheet</strong>, so providing stylesheets with different title attributes will cause some of them to be ignored. See <a href="/en-US/docs/Correctly_Using_Titles_With_External_Stylesheets">Correctly Using Titles With External Stylesheets</a> for a more detailed discussion.</li>
 <li><strong>Alternate</strong> (<code>rel="alternate stylesheet"</code>, <code>title="..."</code> must be specified): disabled by default, can be selected.</li>
</ul>

<p>When style sheets are referenced with a <code>title</code> attribute on the {{HTMLElement("link", "&lt;link rel=\"stylesheet\"&gt;")}} or {{HTMLElement("style")}} element, the title becomes one of the choices offered to the user. Style sheets linked with the same <code>title</code> are part of the same choice. Style sheets linked without a <code>title</code> attribute are always applied.</p>

<p>Use <code>rel="stylesheet"</code> to link to the default style, and <code>rel="alternate stylesheet"</code> to link to alternative style sheets. This tells the browser which style sheet title should be selected by default, and makes that default selection apply in browsers that do not support alternate style sheets.</p>

<h2 id="Specifications">Specifications</h2>

{{Specifications}}

<h2 id="浏览器兼容性">浏览器兼容性</h2>

<p>{{Compat}}</p>