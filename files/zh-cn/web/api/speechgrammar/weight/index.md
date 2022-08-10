---
title: SpeechGrammar.weight
slug: Web/API/SpeechGrammar/weight
tags:
  - API
  - SpeechGrammar
  - Web Speech API
  - 实验性
  - 属性
  - 引用
  - 权重
  - 识别
  - 语音识别
translation_of: Web/API/SpeechGrammar/weight
---
<p>{{APIRef("Web Speech API")}}{{SeeCompatTable}}</p>

<p>{{domxref("SpeechGrammar")}} 接口的可选属性 <strong><code>weight</code></strong> 设置并返回了一个  <code>SpeechGrammar</code> 对象的权重。</p>

<h2 id="语法">语法</h2>

<pre class="syntaxbox">var myGrammarWeight = speechGrammarInstance.weight;</pre>

<h3 id="值">值</h3>

<p>浮点数表示了当前文法的权重，范围在 0.0-1.0 之间。</p>

<h2 id="样例">样例</h2>

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

{{Compat("api.SpeechGrammar.weight")}}

<h2 id="相关链接">相关链接</h2>

<ul>
 <li><a href="/en-US/docs/Web/API/Web_Speech_API">Web Speech API</a></li>
</ul>