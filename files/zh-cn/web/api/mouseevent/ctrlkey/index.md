---
title: MouseEvent.ctrlKey
slug: Web/API/MouseEvent/ctrlKey
translation_of: Web/API/MouseEvent/ctrlKey
---
<p>{{APIRef("DOM Events")}}</p>

<p><strong><code>MouseEvent.ctrlKey</code></strong> 是只读属性，可返回一个布尔值，当 ctrl 键被按下，返回 true，否则返回 false。</p>

<h2 id="语法">语法</h2>

<pre class="syntaxbox">var <em>ctrlKeyPressed</em> = <em>instanceOfMouseEvent</em>.ctrlKey
</pre>

<h3 id="返回值">返回值</h3>

<p>A boolean</p>

<h2 id="Example">示例</h2>

<pre class="brush: js">&lt;html&gt;
&lt;head&gt;
&lt;title&gt;ctrlKey example&lt;/title&gt;

&lt;script type="text/javascript"&gt;

function showChar(e){
  alert(
    "Key Pressed: " + String.fromCharCode(e.charCode) + "\n"
    + "charCode: " + e.charCode + "\n"
    + "CTRL key pressed: " + e.ctrlKey + "\n"
  );
}

&lt;/script&gt;
&lt;/head&gt;

&lt;body onkeypress="showChar(event);"&gt;
&lt;p&gt;Press any character key, with or without holding down the CTRL key.&lt;br /&gt;
You can also use the SHIFT key together with the CTRL key.&lt;/p&gt;
&lt;/body&gt;
&lt;/html&gt;
</pre>

<h2 id="规范">规范</h2>

{{Specifications}}

<h2 id="Browser_compatibility">浏览器兼容性</h2>

{{Compat("api.MouseEvent.ctrlKey")}}

<h2 id="See_also">相关链接</h2>

<ul>
 <li>{{ domxref("MouseEvent") }}</li>
</ul>