---
title: Selection.isCollapsed
slug: Web/API/Selection/isCollapsed
translation_of: Web/API/Selection/isCollapsed
---
<p>{{ ApiRef() }}</p>
<h3 id="Summary">概述</h3>
<p>返回一个布尔值用于描述选区的起始点和终止点是否位于一个位置（即是否框选了，译者注）。</p>
<h3 id="Syntax">用法</h3>
<pre class="eval"><i>sel</i>.isCollapsed
</pre>
<h3 id="Notes">注意</h3>
<p>即使是一个被折叠了的选区，其 rangeCount 的结果也可能大于 0。sel.getRangeAt(0) 会在选区被折叠的情况下返回一个值。</p>