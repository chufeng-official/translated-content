---
title: SpeechGrammar.src
slug: Web/API/SpeechGrammar/src
tags:
  - API
  - SpeechGrammar
  - Web Speech API
  - src
  - 实验性
  - 属性
  - 引用
  - 识别
  - 语音
translation_of: Web/API/SpeechGrammar/src
---
<p>{{APIRef("Web Speech API")}}{{SeeCompatTable}}</p>

<p><code><strong>src</strong></code> 属性是 {{domxref("SpeechGrammar")}} 接口设置并返回的一个字符串，包含了 <code>SpeechGrammar</code> 对象的文法。</p>

<h2 id="语法">语法</h2>

<pre class="syntaxbox">var myGrammar = speechGrammarInstance.src;</pre>

<h3 id="值">值</h3>

<p>{{domxref("DOMString")}} 用以表示文法。</p>

<h2 id="示例">示例</h2>

<pre class="brush: js">var grammar = '#JSGF V1.0; grammar colors; public &lt;color&gt; = aqua | azure | beige | bisque | black | blue | brown | chocolate | coral | crimson | cyan | fuchsia | ghostwhite | gold | goldenrod | gray | green | indigo | ivory | khaki | lavender | lime | linen | magenta | maroon | moccasin | navy | olive | orange | orchid | peru | pink | plum | purple | red | salmon | sienna | silver | snow | tan | teal | thistle | tomato | turquoise | violet | white | yellow ;'
var recognition = new SpeechRecognition();
var speechRecognitionList = new SpeechGrammarList();
speechRecognitionList.addFromString(grammar, 1);
recognition.grammars = speechRecognitionList;


console.log(speechRecognitionList[0].src); // 应该返回和上面文法变量一样的内容
console.log(speechRecognitionList[0].weight); // 应该返回 1 - 与上面第四行所设置的权重一致
</pre>

<h2 id="规范">规范</h2>

{{Specifications}}

<h2 id="浏览器兼容性">浏览器兼容性</h2>

{{Compat("api.SpeechGrammar.src")}}

<h2 id="相关链接">相关链接</h2>

<ul>
 <li><a href="/en-US/docs/Web/API/Web_Speech_API">Web Speech API</a></li>
</ul>