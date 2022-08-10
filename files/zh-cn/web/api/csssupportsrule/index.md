---
title: CSSSupportsRule
slug: Web/API/CSSSupportsRule
translation_of: Web/API/CSSSupportsRule
---
<p>{{APIRef("CSSOM")}}</p>

<p>该 <strong><code>CSSSupportsRule</code></strong> 接口描述了代表一个 CSS 对象{{cssxref("@supports")}} <a href="/en-US/docs/Web/CSS/At-rule">at-rule</a>. 它实现了 {{domxref("CSSConditionRule")}} 接口，因此 {{domxref("CSSRule 指定规则")}} 和{{domxref("CSSGroupingRule")}} 用一个类型值接口 <code>12</code> (<code>CSSRule.SUPPORTS_RULE</code>).</p>

<h2 id="句法">句法</h2>

<p>该语法使用所描述的<a href="http://dev.w3.org/2006/webapi/WebIDL/">WebIDL</a> 格式。</p>

<pre class="syntaxbox">接口 CSSSupportsRule : CSSConditionRule {
}
</pre>

<h2 id="性能">性能</h2>

<p>作为{{domxref("CSSConditionRule")}} 因此一个 {{domxref("CSSRule 指定规则")}} and 和一{{domxref("CSSGroupingRule")}}, <code>CSSSupportsRule</code> 还实现了，这些接口的属性。它没有特定的属性</p>

<h2 id="方法">方法</h2>

<p>作为{{domxref("CSSConditionRule")}} 因此一个 {{domxref("CSSRule 指定规则")}}和{{domxref("CSSGroupingRule")}}, <code>CSSSupportsRule</code> 也实现了这个接口的方法。他没有具体属性的方法</p>

<h2 id="规范">规范</h2>

{{Specifications}}

<h2 id="游览器兼容性">游览器兼容性</h2>

{{Compat("api.CSSSupportsRule")}}

<h2 id="See_also">See also</h2>

<ul>
 <li>{{cssxref("@supports")}}</li>
</ul>