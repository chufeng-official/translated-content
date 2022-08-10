---
title: Window.updateCommands()
slug: Web/API/Window/updateCommands
tags:
  - chrome 窗口（UI）的命令状态。
translation_of: Web/API/Window/updateCommands
---
<p>{{ ApiRef() }}{{Non-standard_header}}</p>

<h2 id="Summary">概要</h2>

<p>更新当前 chrome 窗口（UI）的命令状态。</p>

<h2 id="Syntax">语法</h2>

<pre class="eval">window.updateCommands("sCommandName")
</pre>

<h2 id="Parameters"> 参数</h2>

<ul>
 <li><code>sCommandName</code> 是一个特定的字符串，它描述了这种更新事件的类型 (我们用到了背景色注明).</li>
</ul>

<h2 id="Notes">记录</h2>

<p>这将启用或禁用项目（根据需要在命令节点上设置或清除“disabled”属性），或通过在 XUL 命令节点的“state”属性中设置当前状态信息来确保命令状态反映选择的状态。</p>

<h2 id="Specification">规范</h2>

<p>DOM 0 级。不属于规范。</p>

<h2 id="浏览器兼容性">浏览器兼容性</h2>



<p>{{Compat("api.Window.updateCommands")}}</p>