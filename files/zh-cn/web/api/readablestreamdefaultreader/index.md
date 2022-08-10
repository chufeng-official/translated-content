---
title: ReadableStreamDefaultReader
slug: Web/API/ReadableStreamDefaultReader
translation_of: Web/API/ReadableStreamDefaultReader
---
<p>{{APIRef("Streams")}}{{SeeCompatTable}}</p>

<p><br>
  <a href="/en-US/docs/Web/API/Streams_API">Streams API</a> 的 <strong>ReadableStreamDefaultReader </strong>的接口 表示一个可被用于读取来自网络提供的流数据 (例如 fetch 请求) 的默认读取器</p>

<h2 id="构造方法">构造方法</h2>

<dl>
 <dt><a href="https://developer.mozilla.org/en-US/docs/Web/API/ReadableStreamDefaultReader/ReadableStreamDefaultReader"><code>ReadableStreamDefaultReader()</code></a></dt>
 <dd>创建 和 返回 一个 <code>ReadableStreamDefaultReader()</code> 对象实例。</dd>
</dl>

<h2 id="属性">属性</h2>

<dl>
 <dt><a href="https://developer.mozilla.org/en-US/docs/Web/API/ReadableStreamDefaultReader/closed"><code>ReadableStreamDefaultReader.closed</code></a><br>
    </dt>
 <dd>允许你编写 当 stream 结束时 执行的代码 . 如果这个 stream 变成关闭状态或者 reader 的锁 (lock) 被释放 则返回一个状态是 fulfills 的 promise，如果这个 stream 报错则返回 rejects 的 promise.</dd>
</dl>

<h2 id="方法">方法</h2>

<dl>
 <dt><a href="https://developer.mozilla.org/en-US/docs/Web/API/ReadableStreamDefaultReader/cancel"><code>ReadableStreamDefaultReader.cancel()</code></a></dt>
 <dd>取消这个 stream，表示对这个 stream 失去了兴趣。提供的参数将传递给源 source，可能会也可能不会用到这些参数。</dd>
 <dt><a href="https://developer.mozilla.org/en-US/docs/Web/API/ReadableStreamDefaultReader/read"><code>ReadableStreamDefaultReader.read()</code></a></dt>
 <dd>返回一个 promise，提供对 stream 内部队列中下一个块 (chunk) 访问的 promise.</dd>
 <dt><a href="https://developer.mozilla.org/en-US/docs/Web/API/ReadableStreamDefaultReader/releaseLock"><code>ReadableStreamDefaultReader.releaseLock()</code></a></dt>
 <dd>释放读取这个 stream 的锁。</dd>
</dl>

<h2 id="例子">例子</h2>

<p>在下面的例子中，{{domxref("Response")}} 被创建为流 HTML 片段 fetched 来自其他源。</p>

<p>它展示了一个 {{domxref("ReadableStream")}} 和一个 <a href="https://developer.mozilla.org/en-US/docs/Web/API/Uint8Array"><code>Uint8Array</code></a>组合使用的例子。</p>

<pre class="brush: js">fetch("https://www.example.org/").then((response) =&gt; {
  const reader = response.body.getReader();
  const stream = new ReadableStream({
    start(controller) {
      // The following function handles each data chunk
      function push() {
        // "done" is a Boolean and value a "Uint8Array"
        return reader.read().then(({ done, value }) =&gt; {
          // Is there no more data to read?
          if (done) {
            // Tell the browser that we have finished sending data
            controller.close();
            return;
          }

          // Get the data and send it to the browser via the controller
          controller.enqueue(value);
        }).then(push);
      };

      push();
    }
  });

  return new Response(stream, { headers: { "Content-Type": "text/html" } });
});
</pre>

<h2 id="规范">规范</h2>

{{Specifications}}

<h2 id="浏览器兼容性">浏览器兼容性</h2>

{{Compat("api.ReadableStreamDefaultReader")}}