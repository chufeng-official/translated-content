---
title: document.mozFullScreenEnabled
slug: Web/API/Document/fullscreenEnabled
translation_of: Web/API/Document/fullscreenEnabled
original_slug: Web/API/Document/mozFullScreenEnabled
---
<p>{{ ApiRef() }}</p>
<h3 id="Summary">概述</h3>
<p>返回一个布尔值，表明浏览器是否支持全屏模式。全屏模式只在那些不包含窗口化的插件的页面中可用.对于一个{{ HTMLElement("iframe") }}元素中的页面，则它必需拥有{{ HTMLAttrXRef("mozallowfullscreen", "iframe") }}属性。</p>
<h3 id="Syntax">语法</h3>
<pre class="eval"><em>var isFullScreenAvailable</em> = <em>document</em>.mozFullScreenEnabled;
</pre>
<p>如果当前文档可以进入全屏模式，则<code>isFullScreenAvailable</code>为<code>true</code></p>
<h3 id="Example">例子</h3>
<pre class="eval">function requestFullScreen() {
  if (document.mozFullScreenEnabled) {
    videoElement.requestFullScreen();
  } else {
    console.log('你的浏览器不支持全屏模式！');
  }
}
</pre>
<h3 id="备注">备注</h3>
<p>进入页面<a href="/zh-cn/DOM/Using_full-screen_mode">使用全屏模式</a>查看详情和示例。</p>
<h3 id="Specification">浏览器兼容性</h3>
{{Compat("api.Document.fullscreenEnabled")}}