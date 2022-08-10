---
title: state
slug: Web/API/History/state
translation_of: Web/API/History/state
---
<p>返回在 history 栈顶的 <code>任意</code> 值的拷贝。 通过这种方式可以查看 state 值，不必等待 <code><a href="https://developer.mozilla.org/en-US/docs/Web/Events/popstate">popstate</a></code>事件发生后再查看。</p>

<h2 id="语法">语法</h2>

<pre class="brush: js">let currentState = history.state;</pre>

<p>如果不进行下面两种类型的调用，state 的值将会是 null </p>

<p>{{domxref("History.pushState","pushState()")}} or {{domxref("History.replaceState","replaceState()")}}.</p>

<h2 id="例子">例子</h2>

<p>下面 log 例句输出 history.state 的值，首先是在没有执行 {{domxref("History.pushState","pushState()")}} 语句进而将值 push 到 history 之前的 log。下面一行 log 语句再次输出 state 值，此时 history.state 已经有值。可以在脚本文件中执行下面语句，或者在控制台直接执行。</p>

<pre class="brush: js">// 值为 null 因为我们还没有修改 history 栈
console.log(`History.state before pushState: ${history.state}`);

// 现在 push 一些数据到栈里
history.replaceState({name: 'Example'}, "pushState example", 'page3.html');

// 现在 state 已经有值了
console.log(`History.state after pushState: ${history.state}`);</pre>

<h2 id="规范">规范</h2>

{{Specifications}}

<h2 id="Browser_compatibility">Browser compatibility</h2>



<p>{{Compat("api.History.state")}}</p>

<h2 id="See_also">See also</h2>

<ul>
 <li><a href="/en-US/docs/Web/API/History_API/Working_with_the_History_API">Working with the History API</a></li>
</ul>