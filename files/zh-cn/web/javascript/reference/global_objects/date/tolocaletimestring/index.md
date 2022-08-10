---
title: Date.prototype.toLocaleTimeString()
slug: Web/JavaScript/Reference/Global_Objects/Date/toLocaleTimeString
translation_of: Web/JavaScript/Reference/Global_Objects/Date/toLocaleTimeString
---
<div>{{JSRef("Global_Objects", "Date")}}</div>

<p>The <code><strong>toLocaleTimeString()</strong></code> 方法返回该日期对象时间部分的字符串，该字符串格式因不同语言而不同。新增的参数 <code>locales</code> 和 <code>options</code> 使程序能够指定使用哪种语言格式化规则，允许定制该方法的表现（behavior）。在旧版本浏览器中， <code>locales</code> 和 <code>options</code> 参数被忽略，使用的语言环境和返回的字符串格式是各自独立实现的。</p>

<div>{{EmbedInteractiveExample("pages/js/date-tolocaletimestring.html")}}</div>



<h2 id="Syntax">语法</h2>

<pre class="syntaxbox"><var>dateObj</var>.toLocaleTimeString([locales [, options]])</pre>

<h3 id="Parameters">参数</h3>

<p>查看<a href="#Browser_Compatibility">浏览器兼容性</a>小节，看下哪些浏览器支持 <code>locales</code> 和 <code>options</code> 参数，还可以参看<a href="#Example:_Checking_for_support_for_locales_and_options_arguments">例子：检测 <code>locales</code> 和 <code>options</code> 参数支持情况</a>。</p>

<p>{{page('zh-US/docs/JavaScript/Reference/Global_Objects/DateTimeFormat','Parameters')}}</p>

<p>The default value for each date-time component property is <code>undefined</code>, but if the <code>hour</code>, <code>minute</code>, <code>second</code> properties are all <code>undefined</code>, then <code>hour</code>, <code>minute</code>, and <code>second</code> are assumed to be "numeric".</p>

<h2 id="Examples">例子</h2>

<h3 id="Example:_Using_toLocaleTimeString">例子：使用 <code>toLocaleTimeString</code></h3>

<p>没有指定语言环境（locale）时，返回一个使用默认语言环境和格式设置（options）的格式化字符串。</p>

<pre class="brush:js">var date = new Date(Date.UTC(2012, 11, 12, 3, 0, 0));

// toLocaleTimeString without arguments depends on the implementation,
// the default locale, and the default time zone
alert(date.toLocaleTimeString());
// → "7:00:00 PM" if run in en-US locale with time zone America/Los_Angeles</pre>

<h3 id="Example:_Checking_for_support_for_locales_and_options_arguments">例子：检测 <code>locales</code> 和 <code>options</code> 支持情况</h3>

<p><code>locales</code> 和 <code>options</code> 参数不是所有的浏览器都支持。为了检测一种实现环境（implementation）是否支持它们，可以使用不合法的语言标签，如果实现环境支持该参数，则会抛出一个 <code>RangeError</code> 异常，反之会忽略参数。</p>

<pre class="brush: js">function toLocaleTimeStringSupportsLocales() {
    try {
        new Date().toLocaleTimeString("i");
    } catch (e) {
        return e​.name === "RangeError";
    }
    return false;
}
</pre>

<h3 id="Example:_Using_locales">例子：使用 <code>locales</code> 参数</h3>

<p>下例展示了本地化时间格式的一些变化。为了在应用的用户界面得到某种语言的时间格式，必须确保使用 <code>locales</code> 参数指定了该语言（可能还需要设置某些回退语言）。</p>

<pre class="brush: js">var date = new Date(Date.UTC(2012, 11, 20, 3, 0, 0));

// formats below assume the local time zone of the locale;
// America/Los_Angeles for the US

// US English uses 12-hour time with AM/PM
alert(date.toLocaleTimeString("en-US"));
// → "7:00:00 PM"

// British English uses 24-hour time without AM/PM
alert(date.toLocaleTimeString("en-GB"));
// → "03:00:00"

// Korean uses 12-hour time with AM/PM
alert(date.toLocaleTimeString("ko-KR"));
// → "오후 12:00:00"

// Arabic in most Arabic speaking countries uses real Arabic digits
alert(date.toLocaleTimeString("ar-EG"));
// → "٧:٠٠:٠٠ م"

// when requesting a language that may not be supported, such as
// Balinese, include a fallback language, in this case Indonesian
alert(date.toLocaleTimeString(["ban", "id"]));
// → "11.00.00"
</pre>

<h3 id="Example:_Using_options">例子：使用 <code>options</code> 参数</h3>

<p>可以使用 <code>options </code>参数来自定义 <code>toLocaleTimeString</code> 方法返回的字符串。</p>

<pre class="brush: js">var date = new Date(Date.UTC(2012, 11, 20, 3, 0, 0));

// an application may want to use UTC and make that visible
var options = {timeZone: "UTC", timeZoneName: "short"};
alert(date.toLocaleTimeString("en-US", options));
// → "3:00:00 AM GMT"

// sometimes even the US needs 24-hour time
alert(date.toLocaleTimeString("en-US", {hour12: false}));
// → "19:00:00"
</pre>

<h2 id="Performance">性能</h2>

<p>当格式化大量日期时，最好创建一个 <a href="/en-US/docs/Web/JavaScript/Reference/Global_Objects/DateTimeFormat"><code>Intl.DateTimeFormat</code></a> 对象，然后使用该对象 <a href="/en-US/docs/Web/JavaScript/Reference/Global_Objects/DateTimeFormat/format"><code>format</code></a> 属性提供的方法。</p>

<h2 id="规范">规范</h2>

{{Specifications}}

<h2 id="浏览器兼容性">浏览器兼容性</h2>

<p>{{Compat}}</p>

<h2 id="See_Also">相关链接</h2>

<ul>
 <li>{{jsxref("Global_Objects/DateTimeFormat", "DateTimeFormat")}}</li>
 <li>{{jsxref("Date.prototype.toLocaleDateString()")}}</li>
 <li>{{jsxref("Date.prototype.toLocaleString()")}}</li>
 <li>{{jsxref("Date.prototype.toTimeString()")}}</li>
</ul>