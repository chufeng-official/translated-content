---
title: PerformanceEntry.entryType
slug: Web/API/PerformanceEntry/entryType
translation_of: Web/API/PerformanceEntry/entryType
---
<div>{{APIRef("Performance Timeline API")}}</div>

<p>The <strong><code>entryType</code></strong>  返回一个代表 performance metric 类型的{{domxref("DOMString")}} , 例如被 performance.mark("begin") 所创建的 entry 的 entryType 就是 "<code>mark</code>". 此属性只读。</p>

<h2 id="Syntax">语法</h2>

<pre class="syntaxbox">var <em>type</em> = <em>entry</em>.entryType;</pre>

<h3 id="Return_Value">返回值</h3>

<p>返回值取决于 <code>PerformanceEntry</code> 对象的 subtype， entryType 的取值会影响{{domxref('PerformanceEntry.name')}} 属性， 具体如下表所示. </p>

<table class="standard-table">
 <thead>
  <tr>
   <th scope="col">Value</th>
   <th scope="col">Subtype</th>
   <th scope="col">Type of name property</th>
   <th scope="col">Description of name property</th>
  </tr>
 </thead>
 <tbody>
  <tr>
   <td><code>frame</code>, <code>navigation</code></td>
   <td>{{domxref('PerformanceFrameTiming')}}, {{domxref('PerformanceNavigationTiming')}}</td>
   <td>{{domxref("URL")}}</td>
   <td>The document's address.</td>
  </tr>
  <tr>
   <td><code>resource</code></td>
   <td>{{domxref('PerformanceResourceTiming')}}</td>
   <td>{{domxref("URL")}}</td>
   <td>The resolved URL of the requested resource. This value doesn't change even if the request is redirected.</td>
  </tr>
  <tr>
   <td><code>mark</code></td>
   <td>{{domxref('PerformanceMark')}}</td>
   <td>{{domxref("DOMString")}}</td>
   <td>The name used when the mark was created by calling {{domxref("Performance.mark","performance.mark()")}}.</td>
  </tr>
  <tr>
   <td><code>measure</code></td>
   <td>{{domxref('PerformanceMeasure')}}</td>
   <td>{{domxref("DOMString")}}</td>
   <td>name used when the measure was created by calling {{domxref("Performance.measure","performance.measure()")}}.</td>
  </tr>
  <tr>
   <td><code>paint</code></td>
   <td>{{domxref('PerformancePaintTiming')}}</td>
   <td>{{domxref("DOMString")}}</td>
   <td>Either <code>'first-paint'</code> or <code>'first-contentful-paint'</code>.</td>
  </tr>
 </tbody>
</table>

<h2 id="范例">范例</h2>

<p>下面的代码说明了  <code>entryType</code> 属性的用法。</p>

<pre class="brush: js">function run_PerformanceEntry() {

  // check for feature support before continuing
  if (performance.mark === undefined) {
    console.log("performance.mark not supported");
    return;
  }

  // Create a performance entry named "begin" via the mark() method
  performance.mark("begin");

  // Check the entryType of all the "begin" entries
  var entriesNamedBegin = performance.getEntriesByName("begin");
  //entriesNamedBegin
  //    Array [ PerformanceMark ]
  //entriesNamedBegin[0]
  //    PerformanceMark { name: "begin", entryType: "mark", startTime: 94661370.14, duration: 0 }
  //entriesNamedBegin[0].entryType
  //    "mark"
  //entriesNamedBegin[0].name
  //    "begin"

  for (var i=0; i &lt; entriesNamedBegin.length; i++) {
      var typeOfEntry = entriesNamedBegin[i].entryType;
      console.log("Entry is type: " + typeOfEntry);
  }

}
</pre>

<h2 id="Specifications">Specifications</h2>

{{Specifications}}

<h2 id="Browser_compatibility">Browser compatibility</h2>

<p>{{Compat}}</p>