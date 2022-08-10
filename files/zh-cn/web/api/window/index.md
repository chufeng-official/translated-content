---
title: Window
slug: Web/API/Window
tags:
  - API
  - DOM
  - JavaScript
  - Window
  - global
  - 作用域
  - 全局
  - 参考
  - 接口
  - 标签页
  - 浏览器
translation_of: Web/API/Window
---
<div>{{APIRef("DOM")}}</div>

<p><code>window</code> 对象表示一个包含 DOM 文档的窗口，其 <code>document</code> 属性指向窗口中载入的 <a href="/zh-CN/docs/Web/API/Document">DOM 文档</a> 。使用 {{ Domxref("document.defaultView") }} 属性可以获取指定文档所在窗口。</p>

<p><code>window</code>作为全局变量，代表了脚本正在运行的窗口，暴露给 Javascript 代码。</p>

<p>本节为 DOM <code>Window</code> 对象中可用的所有方法、属性和事件提供简要参考。<code>window</code> 对象实现了 <code>Window</code> 接口，此接口继承自 <code><a href="http://www.w3.org/TR/DOM-Level-2-Views/views.html#Views-AbstractView">AbstractView</a></code> 接口。一些额外的全局函数、命名空间、对象、接口和构造函数与 window 没有典型的关联，但却是有效的，它们在 <a href="/en-US/docs/JavaScript/Reference">JavaScript 参考</a> 和 <a href="/en-US/docs/DOM/DOM_Reference">DOM 参考</a> 中列出。</p>

<p>在有标签页功能的浏览器中，每个标签都拥有自己的 <code>window</code> 对象；也就是说，同一个窗口的标签页之间不会共享一个 <code>window</code> 对象。有一些方法，如 {{ Domxref("window.resizeTo") }} 和 {{ Domxref("window.resizeBy") }} 之类的方法会作用于整个窗口而不是 <code>window</code> 对象所属的那个标签。一般而言，如果一样东西无法恰当地作用于标签，那么它就会作用于窗口。</p>

<p>{{InheritanceDiagram}}</p>

<h2 id="Constructors">Constructors</h2>

<p>See also the <a href="/en-US/docs/DOM/DOM_Reference">DOM Interfaces</a>.</p>

<dl>
 <dt>{{domxref("DOMParser")}}</dt>
 <dd><code>DOMParser</code> can parse XML or HTML source stored in a string into a DOM <a href="/en-US/docs/DOM/document">Document</a>. <code>DOMParser</code> is specified in <a href="https://w3c.github.io/DOM-Parsing/">DOM Parsing and Serialization</a>.</dd>
 <dt>{{domxref("Window.GeckoActiveXObject")}}</dt>
 <dd>{{todo("NeedsContents")}}</dd>
 <dt>{{domxref("Image")}}</dt>
 <dd>Used for creating an {{domxref("HTMLImageElement")}}.</dd>
 <dt>{{domxref("Option")}}</dt>
 <dd>Used for creating an {{domxref("HTMLOptionElement")}}</dd>
 <dt>{{domxref("Window.QueryInterface")}}</dt>
 <dd>{{todo("NeedsContents")}}</dd>
 <dt>{{domxref("Window.StaticRange")}} {{experimental_inline}} {{readonlyinline}}</dt>
 <dd>Returns a {{domxref('StaticRange.StaticRange','StaticRange()')}} constructor which creates a {{domxref('StaticRange')}} object.</dd>
 <dt>{{domxref("Worker")}}</dt>
 <dd>Used for creating a <a href="/en-US/docs/DOM/Using_web_workers">Web worker</a></dd>
 <dt>{{domxref("Window.XMLSerializer")}}</dt>
 <dd>{{todo("NeedsContents")}}</dd>
 <dt>{{domxref("Window.XPCNativeWrapper")}}</dt>
 <dd>{{todo("NeedsContents")}}</dd>
 <dt>{{domxref("Window.XPCSafeJSObjectWrapper")}}</dt>
 <dd>{{todo("NeedsContents")}}</dd>
</dl>

<h2 id="属性">属性</h2>

<p>这个接口从 {{domxref("EventTarget")}} 接口继承属性，也从 <code>WindowOrWorkerGlobalScope</code> 这个 mixin 中继承属性。</p>

<p>注意，对象类型的属性（例如：覆盖内建元素的原型）被列于下面单独的小节之中。</p>

<dl>
 <dt>{{domxref("Window.closed")}} {{Non-standard_inline}} {{readOnlyInline}}</dt>
 <dd>这个属性指示当前窗口是否关闭。</dd>
 <dt>{{domxref("Window.console")}} {{ReadOnlyInline}}</dt>
 <dd>返回 console 对象的引用，该对象提供了对浏览器调试控制台的访问。</dd>
 <dt>{{domxref("Window.content")}} 和 <code>Window._content</code> {{Non-standard_inline}} {{Deprecated_Inline}} {{ReadOnlyInline}}</dt>
 <dd>返回当前 window 的 content 元素的引用。通过带下划线的过时变种方法不再可以获得 Web content。</dd>
 <dt>{{domxref("Window.controllers")}} {{non-standard_inline}} {{ReadOnlyInline}}</dt>
 <dd>返回当前 chrome window 的 XUL 控制器对象。</dd>
 <dt>{{domxref("Window.customElements")}} {{ReadOnlyInline}}</dt>
 <dd>returns a reference to the {{domxref("CustomElementRegistry")}} object, which can be used to register new <a href="/en-US/docs/Web/Web_Components/Using_custom_elements">custom elements</a> and get information about previously registered custom elements.</dd>
 <dt>{{domxref("Window.crypto")}} {{readOnlyInline}}</dt>
 <dd>返回浏览器 crypto 对象。</dd>
 <dt>{{domxref("Window.defaultStatus")}} {{Deprecated_Inline}}</dt>
 <dd>获取或设置指定窗口的状态栏文本。</dd>
 <dt>{{domxref("Window.devicePixelRatio")}} {{non-standard_inline}} {{ReadOnlyInline}}</dt>
 <dd>返回当前显示器的物理像素和设备独立像素的比例。</dd>
 <dt>{{domxref("Window.dialogArguments")}} {{ReadOnlyInline}}</dt>
 <dd>获取在调用 {{domxref("window.showModalDialog()")}} 时传递给窗口的参数（如果它是一个对话框）。这是一个 <code>nsIArray</code>。</dd>
 <dt>{{domxref("Window.directories")}} {{Deprecated_Inline}}</dt>
 <dd>{{domxref("window.personalbar")}} 的另一种形式。</dd>
 <dt>{{domxref("Window.document")}} {{ReadOnlyInline}}</dt>
 <dd>返回对当前窗口所包含文档的引用。</dd>
 <dt>{{domxref("Window.DOMMatrix")}} {{readOnlyInline}} {{experimental_inline}}</dt>
 <dd>Returns a reference to a {{domxref("DOMMatrix")}} object, which represents 4x4 matrices, suitable for 2D and 3D operations.</dd>
 <dt>{{domxref("Window.DOMMatrixReadOnly")}} {{readOnlyInline}} {{experimental_inline}}</dt>
 <dd>Returns a reference to a {{domxref("DOMMatrixReadOnly")}} object, which represents 4x4 matrices, suitable for 2D and 3D operations.</dd>
 <dt>{{domxref("Window.DOMPoint")}} {{readOnlyInline}} {{experimental_inline}}</dt>
 <dd>Returns a reference to a {{domxref("DOMPoint")}} object, which represents a 2D or 3D point in a coordinate system.</dd>
 <dt>{{domxref("Window.DOMPointReadOnly")}} {{readOnlyInline}} {{experimental_inline}}</dt>
 <dd>Returns a reference to a {{domxref("DOMPointReadOnly")}} object, which represents a 2D or 3D point in a coordinate system.</dd>
 <dt>{{domxref("Window.DOMQuad")}} {{readOnlyInline}} {{experimental_inline}}</dt>
 <dd>Returns a reference to a {{domxref("DOMQuad")}} object, which provides represents a quadrilaterial object, that is one having four corners and four sides.</dd>
 <dt>{{domxref("Window.DOMRect")}} {{readOnlyInline}} {{experimental_inline}}</dt>
 <dd>Returns a reference to a {{domxref("DOMRect")}} object, which represents a rectangle.</dd>
 <dt>{{domxref("Window.DOMRectReadOnly")}} {{readOnlyInline}} {{experimental_inline}}</dt>
 <dd>Returns a reference to a {{domxref("DOMRectReadOnly")}} object, which represents a rectangle.</dd>
 <dt>{{domxref("Window.event")}} {{ReadOnlyInline}}</dt>
 <dd>Returns the <strong>current event</strong>, which is the event currently being handled by the JavaScript code's context, or <code>undefined</code> if no event is currently being handled. The {{domxref("Event")}} object passed directly to event handlers should be used instead whenever possible.</dd>
 <dt>{{domxref("Window.frameElement")}} {{readOnlyInline}}</dt>
 <dd>返回嵌入窗口的元素，如果未嵌入窗口，则返回 null。</dd>
 <dt>{{domxref("Window.frames")}} {{readOnlyInline}}</dt>
 <dd>返回当前窗口中所有子窗体的数组。</dd>
 <dt>{{domxref("Window.fullScreen")}}</dt>
 <dd>此属性表示窗口是否以全屏显示。</dd>
 <dt>{{domxref("Window.globalStorage")}} {{Non-standard_inline}} {{Deprecated_Inline}}</dt>
 <dd>Gecko 13 (Firefox 13) 开始废弃。使用 {{domxref("Window.localStorage")}} 替代它。<br>
 原本是：用于存储跨页面数据的多重存储对象。</dd>
 <dt>{{domxref("Window.history")}} {{ReadOnlyInline}}</dt>
 <dd>返回一个对 history 对象的引用。</dd>
 <dt>{{domxref("Window.innerHeight")}} {{readOnlyInline}}</dt>
 <dd>获得浏览器窗口的内容区域的高度，包含水平滚动条 (如果有的话)。</dd>
 <dt>{{domxref("Window.innerWidth")}} {{readOnlyInline}}</dt>
 <dd>获得浏览器窗口的内容区域的宽度，包含垂直滚动条 (如果有的话)。</dd>
 <dt>{{domxref("Window.isSecureContext")}} {{experimental_inline}} {{readOnlyInline}}</dt>
 <dd>指出上下文环境是否能够使用安全上下文环境的特征。</dd>
 <dt>{{domxref("Window.length")}} {{readOnlyInline}}</dt>
 <dd>返回窗口中的 frames 数量。参见 {{domxref("window.frames")}}。</dd>
 <dt>{{domxref("Window.location")}}</dt>
 <dd>获取、设置 window 对象的 location，或者当前的 URL.</dd>
 <dt>{{domxref("Window.locationbar")}} {{ReadOnlyInline}}</dt>
 <dd>返回 locationbar 对象，其可视性可以在窗口中切换。</dd>
 <dt>{{domxref("Window.localStorage")}} {{readOnlyInline}}</dt>
 <dd>返回用来存储只能在创建它的源下访问的数据的本地存储对象的引用</dd>
 <dt>{{domxref("Window.menubar")}} {{ReadOnlyInline}}</dt>
 <dd>返回菜单条对象，它的可视性可以在窗口中切换</dd>
 <dt>{{domxref("Window.messageManager")}}</dt>
 <dd>返回窗口的 <a href="/en-US/docs/The_message_manager">message manager</a> 对象。</dd>
 <dt>{{domxref("Window.mozAnimationStartTime")}} {{ReadOnlyInline}} {{Deprecated_inline}}</dt>
 <dd>返回当前动画循环开始经过的毫秒数</dd>
 <dt>{{domxref("Window.mozInnerScreenX")}} {{ReadOnlyInline}} {{non-standard_inline}}</dt>
 <dd>Returns the horizontal (X) coordinate of the top-left corner of the window's viewport, in screen coordinates. This value is reported in CSS pixels. See <code>mozScreenPixelsPerCSSPixel</code> in <code>nsIDOMWindowUtils</code> for a conversion factor to adapt to screen pixels if needed.</dd>
 <dt>{{domxref("Window.mozInnerScreenY")}} {{ReadOnlyInline}} {{non-standard_inline}}</dt>
 <dd>Returns the vertical (Y) coordinate of the top-left corner of the window's viewport, in screen coordinates. This value is reported in CSS pixels. See <code>mozScreenPixelsPerCSSPixel</code> for a conversion factor to adapt to screen pixels if needed.</dd>
 <dt>{{domxref("Window.mozPaintCount")}} {{non-standard_inline}} {{ReadOnlyInline}}</dt>
 <dd>Returns the number of times the current document has been rendered to the screen in this window. This can be used to compute rendering performance.</dd>
 <dt>{{domxref("Window.name")}}</dt>
 <dd>获取/设置窗口的名称。</dd>
 <dt>{{domxref("Window.navigator")}} {{readOnlyInline}}</dt>
 <dd>返回对 navigator 对象的引用。</dd>
 <dt>{{domxref("Window.opener")}}</dt>
 <dd>返回对打开当前窗口的那个窗口的引用。</dd>
 <dt>{{domxref("Window.orientation")}} {{non-standard_inline}} {{deprecated_inline}} {{readOnlyInline}}</dt>
 <dd>Returns the orientation in degrees (in 90 degree increments) of the viewport relative to the device's natural orientation.</dd>
 <dt>{{domxref("Window.outerHeight")}} {{readOnlyInline}}</dt>
 <dd>返回浏览器窗口的外部高度。</dd>
 <dt>{{domxref("Window.outerWidth")}} {{readOnlyInline}}</dt>
 <dd>返回浏览器窗口的外部宽度。</dd>
 <dt>{{domxref("Window.scrollX","Window.pageXOffset")}} {{readOnlyInline}}</dt>
 <dd>{{domxref("window.scrollX")}}的别名。</dd>
 <dt>{{domxref("Window.scrollY","Window.pageYOffset")}} {{readOnlyInline}}</dt>
 <dd>{{domxref("window.scrollY")}}的别名。</dd>
 <dt>{{domxref("Window.parent")}} {{readOnlyInline}}</dt>
 <dd>返回当前窗口或子窗口的父窗口的引用。</dd>
 <dt>{{domxref("Window.performance")}} {{readOnlyInline}}</dt>
 <dd>Returns a {{domxref("Performance")}} object, which includes the {{domxref("Performance.timing", "timing")}} and {{domxref("Performance.navigation", "navigation")}} attributes, each of which is an object providing <a href="/en-US/docs/Navigation_timing">performance-related</a> data. See also <a href="/en-US/docs/Web/API/Navigation_timing_API/Using_Navigation_Timing">Using Navigation Timing</a> for additional information and examples.</dd>
 <dt>{{domxref("Window.personalbar")}} {{readOnlyInline}}</dt>
 <dd>返回 personalbar 对象，它的可视性可以在窗口中切换。</dd>
 <dt>{{domxref("Window.pkcs11")}} {{Deprecated_Inline}}</dt>
 <dd>Formerly provided access to install and remove PKCS11 modules.</dd>
 <dt>{{domxref("Window.returnValue")}}</dt>
 <dd>The return value to be returned to the function that called {{domxref("window.showModalDialog()")}} to display the window as a modal dialog.</dd>
 <dt>{{domxref("Window.screen")}} {{readOnlyInline}}</dt>
 <dd>Returns a reference to the screen object associated with the window.</dd>
 <dt>{{domxref("Window.screenX")}} and {{domxref("Window.screenLeft")}} {{readOnlyInline}}</dt>
 <dd>Both properties return the horizontal distance from the left border of the user's browser viewport to the left side of the screen.</dd>
 <dt>{{domxref("Window.screenY")}} and {{domxref("Window.screenTop")}} {{readOnlyInline}}</dt>
 <dd>Both properties return the vertical distance from the top border of the user's browser viewport to the top side of the screen.</dd>
 <dt>{{domxref("Window.scrollbars")}} {{readOnlyInline}}</dt>
 <dd>Returns the scrollbars object, whose visibility can be toggled in the window.</dd>
 <dt>{{domxref("Window.scrollMaxX")}} {{non-standard_inline}} {{ReadOnlyInline}}</dt>
 <dd>The maximum offset that the window can be scrolled to horizontally, that is the document width minus the viewport width.</dd>
 <dt>{{domxref("Window.scrollMaxY")}} {{non-standard_inline}} {{ReadOnlyInline}}</dt>
 <dd>The maximum offset that the window can be scrolled to vertically (i.e., the document height minus the viewport height).</dd>
 <dt>{{domxref("Window.scrollX")}} {{readOnlyInline}}</dt>
 <dd>Returns the number of pixels that the document has already been scrolled horizontally.</dd>
 <dt>{{domxref("Window.scrollY")}} {{readOnlyInline}}</dt>
 <dd>Returns the number of pixels that the document has already been scrolled vertically.</dd>
 <dt>{{domxref("Window.self")}} {{ReadOnlyInline}}</dt>
 <dd>Returns an object reference to the window object itself.</dd>
 <dt>{{domxref("Window.sessionStorage")}}</dt>
 <dd>Returns a reference to the session storage object used to store data that may only be accessed by the origin that created it.</dd>
 <dt>{{domxref("Window.sidebar")}} {{non-standard_inline}} {{ReadOnlyInline}}</dt>
 <dd>Returns a reference to the window object of the sidebar.</dd>
 <dt>{{domxref("Window.speechSynthesis")}} {{ReadOnlyInline}}</dt>
 <dd>Returns a {{domxref("SpeechSynthesis")}} object, which is the entry point into using <a href="/en-US/docs/Web/API/Web_Speech_API">Web Speech API</a> speech synthesis functionality.</dd>
 <dt>{{domxref("Window.status")}}</dt>
 <dd>Gets/sets the text in the statusbar at the bottom of the browser.</dd>
 <dt>{{domxref("Window.statusbar")}} {{readOnlyInline}}</dt>
 <dd>Returns the statusbar object, whose visibility can be toggled in the window.</dd>
 <dt>{{domxref("Window.toolbar")}} {{readOnlyInline}}</dt>
 <dd>Returns the toolbar object, whose visibility can be toggled in the window.</dd>
 <dt>{{domxref("Window.top")}} {{readOnlyInline}}</dt>
 <dd>Returns a reference to the topmost window in the window hierarchy. This property is read only.</dd>
 <dt>{{domxref("Window.visualViewport")}} {{readOnlyInline}}</dt>
 <dd>Returns a {{domxref("VisualViewport")}} object which represents the visual viewport for a given window.</dd>
 <dt>{{domxref("Window.window")}} {{ReadOnlyInline}}</dt>
 <dd>Returns a reference to the current window.</dd>
 <dt><code>window[0]</code>, <code>window[1]</code>, etc.</dt>
 <dd>Returns a reference to the <code>window</code> object in the frames. See {{domxref("Window.frames")}} for more details.</dd>
</dl>

<h3 id="Properties_implemented_from_elsewhere">Properties implemented from elsewhere</h3>

<dl>
 <dt>{{domxref("caches")}} {{readOnlyinline}}</dt>
 <dd>Returns the {{domxref("CacheStorage")}} object associated with the current context. This object enables functionality such as storing assets for offline use, and generating custom responses to requests.</dd>
 <dt>{{domxref("indexedDB")}} {{readonlyInline}}</dt>
 <dd>Provides a mechanism for applications to asynchronously access capabilities of indexed databases; returns an {{domxref("IDBFactory")}} object.</dd>
 <dt>{{domxref("isSecureContext")}} {{readOnlyinline}}</dt>
 <dd>Returns a boolean indicating whether the current context is secure (<code>true</code>) or not (<code>false</code>).</dd>
 <dt>{{domxref("origin")}} {{readOnlyinline}}</dt>
 <dd>Returns the global object's origin, serialized as a string. (This does not yet appear to be implemented in any browser.)</dd>
</dl>

<h2 id="方法">方法</h2>

<p><em>This interface inherits methods from the {{domxref("EventTarget")}} interface and implements methods from <code>WindowOrWorkerGlobalScope</code> and {{domxref("EventTarget")}}.</em></p>

<dl>
 <dt>{{domxref("Window.alert()")}}</dt>
 <dd>Displays an alert dialog.</dd>
 <dt>{{domxref("Window.back()")}} {{Non-standard_inline}} {{Deprecated_Inline}}</dt>
 <dd>Moves back one in the window history. This method is obsolete; you should instead use {{domxref("History.back", "window.history.back()")}}.</dd>
 <dt>{{domxref("Window.blur()")}}</dt>
 <dd>Sets focus away from the window.</dd>
 <dt>{{domxref("Window.cancelAnimationFrame()")}} {{experimental_inline}}</dt>
 <dd>Enables you to cancel a callback previously scheduled with {{domxref("Window.requestAnimationFrame")}}.</dd>
 <dt>{{domxref("Window.cancelIdleCallback()")}} {{experimental_inline}}</dt>
 <dd>Enables you to cancel a callback previously scheduled with {{domxref("Window.requestIdleCallback")}}.</dd>
 <dt>{{domxref("Window.captureEvents()")}} {{Deprecated_inline}}</dt>
 <dd>Registers the window to capture all events of the specified type.</dd>
 <dt>{{domxref("Window.clearImmediate()")}}</dt>
 <dd>Cancels the repeated execution set using <code>setImmediate</code>.</dd>
 <dt>{{domxref("Window.close()")}}</dt>
 <dd>Closes the current window.</dd>
 <dt>{{domxref("Window.confirm()")}}</dt>
 <dd>Displays a dialog with a message that the user needs to respond to.</dd>
 <dt>{{domxref("Window.disableExternalCapture()")}} {{Deprecated_Inline}}</dt>
 <dd>{{todo("NeedsContents")}}</dd>
 <dt>{{domxref("Window.dispatchEvent()")}}</dt>
 <dd>Used to trigger an event.</dd>
 <dt>{{domxref("Window.dump()")}} {{Non-standard_inline}}</dt>
 <dd>Writes a message to the console.</dd>
 <dt>{{domxref("Window.enableExternalCapture()")}} {{Deprecated_Inline}}</dt>
 <dd>{{todo("NeedsContents")}}</dd>
 <dt>{{domxref("Window.find()")}}</dt>
 <dd>Searches for a given string in a window.</dd>
 <dt>{{domxref("Window.focus()")}}</dt>
 <dd>Sets focus on the current window.</dd>
 <dt>{{domxref("Window.forward()")}} {{Non-standard_inline}} {{Deprecated_Inline}}</dt>
 <dd>Moves the window one document forward in the history. This method is obsolete; you should instead use {{domxref("History.forward", "window.history.forward()")}}.</dd>
 <dt>{{domxref("Window.getAttention()")}} {{Non-standard_inline}} {{Deprecated_Inline}}</dt>
 <dd>Flashes the application icon.</dd>
 <dt>{{domxref("Window.getAttentionWithCycleCount()")}}</dt>
 <dd>{{todo("NeedsContents")}}</dd>
 <dt>{{domxref("Window.getComputedStyle()")}}</dt>
 <dd>Gets computed style for the specified element. Computed style indicates the computed values of all CSS properties of the element.</dd>
 <dt>{{domxref("Window.getDefaultComputedStyle()")}} {{Non-standard_inline}}</dt>
 <dd>Gets default computed style for the specified element, ignoring author stylesheets.</dd>
 <dt>{{domxref("Window.getSelection()")}}</dt>
 <dd>Returns the selection object representing the selected item(s).</dd>
 <dt>{{domxref("Window.home()")}} {{Non-standard_inline}} {{Deprecated_Inline}}</dt>
 <dd>Returns the browser to the home page.</dd>
 <dt>{{domxref("Window.matchMedia()")}}</dt>
 <dd>Returns a {{domxref("MediaQueryList")}} object representing the specified media query string.</dd>
 <dt>{{domxref("Window.maximize()")}}</dt>
 <dd>{{todo("NeedsContents")}}</dd>
 <dt>{{domxref("Window.minimize()")}} (top-level XUL windows only)</dt>
 <dd>Minimizes the window.</dd>
 <dt>{{domxref("Window.moveBy()")}}</dt>
 <dd>Moves the current window by a specified amount.</dd>
 <dt>{{domxref("Window.moveTo()")}}</dt>
 <dd>Moves the window to the specified coordinates.</dd>
 <dt>{{domxref("Window.open()")}}</dt>
 <dd>打开一个新窗口。</dd>
 <dt>{{domxref("Window.openDialog()")}} {{Non-standard_inline}} {{Deprecated_Inline}}</dt>
 <dd>打开一个新的对话框窗口。</dd>
 <dt>{{domxref("Window.postMessage()")}}</dt>
 <dd>为一个窗口向另一个窗口发送数据字符串提供了一种安全方法，该窗口不必与第一个窗口处于相同的域中。</dd>
 <dt>{{domxref("Window.print()")}}</dt>
 <dd>打开打印对话框以打印当前文档。</dd>
 <dt>{{domxref("Window.prompt()")}}</dt>
 <dd>返回用户在提示对话框中输入的文本。</dd>
 <dt>{{domxref("Window.releaseEvents()")}} {{Non-standard_inline}} {{Deprecated_inline}}</dt>
 <dd>释放捕获特定类型事件的窗口。</dd>
 <dt>{{domxref("Window.requestAnimationFrame()")}}</dt>
 <dd>告诉浏览器一个动画正在进行中，请求浏览器为下一个动画帧重新绘制窗口。</dd>
 <dt>{{domxref("Window.requestIdleCallback()")}} {{experimental_inline}}</dt>
 <dd>启用在浏览器空闲期间对任务进行调度。</dd>
 <dt>{{domxref("Window.resizeBy()")}}</dt>
 <dd>将当前窗口调整到一定的大小。</dd>
 <dt>{{domxref("Window.resizeTo()")}}</dt>
 <dd>动态调整窗口。</dd>
 <dt>{{domxref("Window.restore()")}} {{Non-standard_inline}} {{Deprecated_Inline}}</dt>
 <dd>{{todo("NeedsContents")}}</dd>
 <dt>{{domxref("Window.routeEvent()")}} {{Deprecated_Inline}}</dt>
 <dd>{{todo("NeedsContents")}}</dd>
 <dt>{{domxref("Window.scroll()")}}</dt>
 <dd>滚动窗口到文档中的特定位置。</dd>
 <dt>{{domxref("Window.scrollBy()")}}</dt>
 <dd>按给定的数量在窗口中滚动文档。</dd>
 <dt>{{domxref("Window.scrollByLines()")}} {{Non-standard_inline}}</dt>
 <dd>按给定行数滚动文档。</dd>
 <dt>{{domxref("Window.scrollByPages()")}} {{Non-standard_inline}}</dt>
 <dd>按指定页数滚动当前文档。</dd>
 <dt>{{domxref("Window.scrollTo()")}}</dt>
 <dd>滚动到文档中的特定坐标集。</dd>
 <dt>{{domxref("Window.setCursor()")}} {{Non-standard_inline}} (top-level XUL windows only)</dt>
 <dd>更改当前窗口的光标。</dd>
 <dt>{{domxref("Window.setImmediate()")}}</dt>
 <dd>在浏览器完成其他繁重任务后执行一个函数。</dd>
 <dt>{{domxref("Window.setResizable()")}} {{Non-standard_inline}}</dt>
 <dd>切换用户调整窗口大小的能力。</dd>
 <dt>{{domxref("Window.sizeToContent()")}} {{Non-standard_inline}}</dt>
 <dd>根据内容设置窗口大小。</dd>
 <dt>{{domxref("Window.stop()")}}</dt>
 <dd>这个方法停止窗口加载。</dd>
 <dt>{{domxref("Window.updateCommands()")}} {{Non-standard_inline}}</dt>
 <dd>更新当前 chrome 窗口 (UI) 命令的状态。</dd>
</dl>

<h3 id="Methods_implemented_from_elsewhere">Methods implemented from elsewhere</h3>

<dl>
 <dt>{{domxref("EventTarget.addEventListener()")}}</dt>
 <dd>Register an event handler to a specific event type on the window.</dd>
 <dt>{{domxref("atob()")}}</dt>
 <dd>Decodes a string of data which has been encoded using base-64 encoding.</dd>
 <dt>{{domxref("btoa()")}}</dt>
 <dd>Creates a base-64 encoded ASCII string from a string of binary data.</dd>
 <dt>{{domxref("clearInterval()")}}</dt>
 <dd>Cancels the repeated execution set using {{domxref("setInterval()")}}.</dd>
 <dt>{{domxref("clearTimeout()")}}</dt>
 <dd>Cancels the delayed execution set using {{domxref("setTimeout()")}}.</dd>
 <dt>{{domxref("createImageBitmap()")}}</dt>
 <dd>Accepts a variety of different image sources, and returns a {{domxref("Promise")}} which resolves to an {{domxref("ImageBitmap")}}. Optionally the source is cropped to the rectangle of pixels originating at <em>(sx, sy)</em> with width sw, and height sh.</dd>
 <dt>{{domxref("fetch()")}}</dt>
 <dd>Starts the process of fetching a resource from the network.</dd>
 <dt>{{domxref("EventTarget.removeEventListener")}}</dt>
 <dd>Removes an event listener from the window.</dd>
 <dt>{{domxref("setInterval()")}}</dt>
 <dd>Schedules a function to execute every time a given number of milliseconds elapses.</dd>
 <dt>{{domxref("setTimeout()")}}</dt>
 <dd>Schedules a function to execute in a given amount of time.</dd>
</dl>

<h3 id="Obsolete_methods">Obsolete methods</h3>

<dl>
 <dt>{{domxref("Window.showModalDialog()")}} {{Deprecated_Inline}}</dt>
 <dd>Displays a modal dialog. <strong>This method was removed completely in Chrome 43, and Firefox 55.</strong></dd>
</dl>

<h2 id="Event_handlers">Event handlers</h2>

<p>These are properties of the window object that can be set to establish event handlers for the various things that can happen in the window that might be of interest.</p>

<p><em>This interface inherits event handlers from the {{domxref("EventTarget")}} interface.</em></p>

<div class="note">
<p><strong>Note:</strong> Starting in {{Gecko("9.0")}}, you can now use the syntax <code>if ("onabort" in window)</code> to determine whether or not a given event handler property exists. This is because event handler interfaces have been updated to be proper web IDL interfaces. See <a href="/en-US/docs/DOM/DOM_event_handlers">DOM event handlers</a> for details.</p>
</div>

<dl>
 <dt>{{domxref("Window.onappinstalled")}}</dt>
 <dd>Called when the page is installed as a webapp. See {{event('appinstalled')}} event.</dd>
 <dt>{{domxref("Window.onbeforeinstallprompt")}}</dt>
 <dd>An event handler property dispatched before a user is prompted to save a web site to a home screen on mobile.</dd>
 <dt>{{domxref("Window.ondevicelight")}}</dt>
 <dd>An event handler property for any ambient light levels changes</dd>
 <dt>{{domxref("Window.ondevicemotion")}}</dt>
 <dd>Called if accelerometer detects a change (For mobile devices)</dd>
 <dt>{{domxref("Window.ondeviceorientation")}}</dt>
 <dd>Called when the orientation is changed (For mobile devices)</dd>
 <dt>{{domxref("Window.ondeviceorientationabsolute")}} {{non-standard_inline}} Chrome only</dt>
 <dd>An event handler property for any device orientation changes.</dd>
 <dt>{{domxref("Window.ondeviceproximity")}}</dt>
 <dd>An event handler property for device proximity event</dd>
 <dt>{{domxref("Window.ongamepadconnected")}}</dt>
 <dd>Represents an event handler that will run when a gamepad is connected (when the {{event('gamepadconnected')}} event fires).</dd>
 <dt>{{domxref("Window.ongamepaddisconnected")}}</dt>
 <dd>Represents an event handler that will run when a gamepad is disconnected (when the {{event('gamepaddisconnected')}} event fires).</dd>
 <dt>{{domxref("Window.onmozbeforepaint")}}</dt>
 <dd>An event handler property for the <code>MozBeforePaint</code> event, which is sent before repainting the window if the event has been requested by a call to the {{domxref("Window.mozRequestAnimationFrame()")}} method.</dd>
 <dt>{{domxref("Window.onpaint")}}</dt>
 <dd>An event handler property for paint events on the window.</dd>
 <dt>{{domxref("Window.onrejectionhandled")}} {{experimental_inline}}</dt>
 <dd>An event handler for handled {{jsxref("Promise")}} rejection events.</dd>
 <dt>{{domxref("Window.onuserproximity")}}</dt>
 <dd>An event handler property for user proximity events.</dd>
 <dt>{{domxref("Window.onvrdisplayconnect")}}</dt>
 <dd>Represents an event handler that will run when a compatible VR device has been connected to the computer (when the {{event("vrdisplayconnected")}} event fires).</dd>
 <dt>{{domxref("Window.onvrdisplaydisconnect")}}</dt>
 <dd>Represents an event handler that will run when a compatible VR device has been disconnected from the computer (when the {{event("vrdisplaydisconnected")}} event fires).</dd>
 <dt>{{domxref("Window.onvrdisplayactivate")}}</dt>
 <dd>Represents an event handler that will run when a display is able to be presented to (when the {{event("vrdisplayactivate")}} event fires), for example if an HMD has been moved to bring it out of standby, or woken up by being put on.</dd>
 <dt>{{domxref("Window.onvrdisplaydeactivate")}}</dt>
 <dd>Represents an event handler that will run when a display can no longer be presented to (when the {{event("vrdisplaydeactivate")}} event fires), for example if an HMD has gone into standby or sleep mode due to a period of inactivity.</dd>
 <dt>{{domxref("Window.onvrdisplayblur")}}</dt>
 <dd>Represents an event handler that will run when presentation to a display has been paused for some reason by the browser, OS, or VR hardware (when the {{event("vrdisplayblur")}} event fires) — for example, while the user is interacting with a system menu or browser, to prevent tracking or loss of experience.</dd>
 <dt>{{domxref("Window.onvrdisplayfocus")}}</dt>
 <dd>Represents an event handler that will run when presentation to a display has resumed after being blurred (when the {{event("vrdisplayfocus")}} event fires).</dd>
 <dt>{{domxref("Window.onvrdisplaypresentchange")}}</dt>
 <dd>represents an event handler that will run when the presenting state of a VR device changes — i.e. goes from presenting to not presenting, or vice versa (when the {{event("vrdisplaypresentchange")}} event fires).</dd>
</dl>

<h3 id="Event_handlers_implemented_from_elsewhere">Event handlers implemented from elsewhere</h3>

<dl>
 <dt>{{domxref("GlobalEventHandlers.onabort")}}</dt>
 <dd>Called when the loading of a resource has been aborted, such as by a user canceling the load while it is still in progress</dd>
 <dt>{{domxref("WindowEventHandlers.onafterprint")}}</dt>
 <dd>Called when the print dialog box is closed. See {{event("afterprint")}} event.</dd>
 <dt>{{domxref("WindowEventHandlers.onbeforeprint")}}</dt>
 <dd>Called when the print dialog box is opened. See {{event("beforeprint")}} event.</dd>
 <dt>{{domxref("WindowEventHandlers.onbeforeunload")}}</dt>
 <dd>An event handler property for before-unload events on the window.</dd>
 <dt>{{domxref("GlobalEventHandlers.onblur")}}</dt>
 <dd>Called after the window loses focus, such as due to a popup.</dd>
 <dt>{{domxref("GlobalEventHandlers.onchange")}}</dt>
 <dd>An event handler property for change events on the window.</dd>
 <dt>{{domxref("GlobalEventHandlers.onclick")}}</dt>
 <dd>Called after the ANY mouse button is pressed &amp; released</dd>
 <dt>{{domxref("GlobalEventHandlers.ondblclick")}}</dt>
 <dd>Called when a double click is made with ANY mouse button.</dd>
 <dt>{{domxref("GlobalEventHandlers.onclose")}}</dt>
 <dd>Called after the window is closed</dd>
 <dt>{{domxref("GlobalEventHandlers.oncontextmenu")}}</dt>
 <dd>Called when the RIGHT mouse button is pressed</dd>
 <dt>{{domxref("GlobalEventHandlers.onerror")}}</dt>
 <dd>Called when a resource fails to load OR when an error occurs at runtime. See {{event("error")}} event.</dd>
 <dt>{{domxref("GlobalEventHandlers.onfocus")}}</dt>
 <dd>Called after the window receives or regains focus. See {{event("focus")}} events.</dd>
 <dt>{{domxref("WindowEventHandlers.onhashchange")}}</dt>
 <dd>An event handler property for {{event('hashchange')}} events on the window; called when the part of the URL after the hash mark ("#") changes.</dd>
 <dt>{{domxref("GlobalEventHandlers.oninput")}}</dt>
 <dd>Called when the value of an &lt;input&gt; element changes</dd>
 <dt>{{domxref("GlobalEventHandlers.onkeydown")}}</dt>
 <dd>Called when you begin pressing ANY key. See {{event("keydown")}} event.</dd>
 <dt>{{domxref("GlobalEventHandlers.onkeypress")}}</dt>
 <dd>Called when a key (except Shift, Fn, and CapsLock) is in pressed position. See {{event("keypress")}} event.</dd>
 <dt>{{domxref("GlobalEventHandlers.onkeyup")}}</dt>
 <dd>Called when you finish releasing ANY key. See {{event("keyup")}} event.</dd>
 <dt>{{domxref("WindowEventHandlers.onlanguagechange")}}</dt>
 <dd>An event handler property for {{event("languagechange")}} events on the window.</dd>
 <dt>{{domxref("GlobalEventHandlers.onload")}}</dt>
 <dd>Called after all resources and the DOM are fully loaded. WILL NOT get called when the page is loaded from cache, such as with back button.</dd>
 <dt>{{domxref("WindowEventHandlers.onmessage")}}</dt>
 <dd>Is an {{event("Event_handlers", "event handler")}} representing the code to be called when the {{event("message")}} event is raised.</dd>
 <dt>{{domxref("GlobalEventHandlers.onmousedown")}}</dt>
 <dd>Called when ANY mouse button is pressed.</dd>
 <dt>{{domxref("GlobalEventHandlers.onmousemove")}}</dt>
 <dd>Called continously when the mouse is moved inside the window.</dd>
 <dt>{{domxref("GlobalEventHandlers.onmouseout")}}</dt>
 <dd>Called when the pointer leaves the window.</dd>
 <dt>{{domxref("GlobalEventHandlers.onmouseover")}}</dt>
 <dd>Called when the pointer enters the window</dd>
 <dt>{{domxref("GlobalEventHandlers.onmouseup")}}</dt>
 <dd>Called when ANY mouse button is released</dd>
 <dt>{{domxref("WindowEventHandlers.onoffline")}}</dt>
 <dd>Called when network connection is lost. See {{event("offline")}} event.</dd>
 <dt>{{domxref("WindowEventHandlers.ononline")}}</dt>
 <dd>Called when network connection is established. See {{event("online")}} event.</dd>
 <dt>{{domxref("WindowEventHandlers.onpagehide")}}</dt>
 <dd>Called when the user navigates away from the page, before the onunload event. See {{event("pagehide")}} event.</dd>
 <dt>{{domxref("WindowEventHandlers.onpageshow")}}</dt>
 <dd>Called after all resources and the DOM are fully loaded. See {{event("pageshow")}} event.</dd>
 <dt>{{domxref("WindowEventHandlers.onpopstate")}}</dt>
 <dd>Called when a back button is pressed.</dd>
 <dt>{{domxref("GlobalEventHandlers.onreset")}}</dt>
 <dd>Called when a form is reset</dd>
 <dt>{{domxref("GlobalEventHandlers.onresize")}}</dt>
 <dd>Called continuously as you are resizing the window.</dd>
 <dt>{{domxref("GlobalEventHandlers.onscroll")}}</dt>
 <dd>Called when the scroll bar is moved via ANY means. If the resource fully fits in the window, then this event cannot be invoked</dd>
 <dt>{{domxref("GlobalEventHandlers.onwheel")}}</dt>
 <dd>Called when the mouse wheel is rotated around any axis</dd>
 <dt>{{domxref("GlobalEventHandlers.onselect")}}</dt>
 <dd>Called after text in an input field is selected</dd>
 <dt>{{domxref("GlobalEventHandlers.onselectionchange")}}</dt>
 <dd>Is an {{event("Event_handlers", "event handler")}} representing the code to be called when the {{event("selectionchange")}} event is raised.</dd>
 <dt>{{domxref("WindowEventHandlers.onstorage")}}</dt>
 <dd>Called when there is a change in session storage or local storage. See {{event("storage")}} event</dd>
 <dt>{{domxref("GlobalEventHandlers.onsubmit")}}</dt>
 <dd>Called when a form is submitted</dd>
 <dt>{{domxref("WindowEventHandlers.onunhandledrejection")}} {{experimental_inline}}</dt>
 <dd>An event handler for unhandled {{jsxref("Promise")}} rejection events.</dd>
 <dt>{{domxref("WindowEventHandlers.onunload")}}</dt>
 <dd>Called when the user navigates away from the page.</dd>
</dl>

<h2 id="Events">Events</h2>

<p>Listen to these events using <code><a href="/en-US/docs/Web/API/EventTarget/addEventListener">addEventListener()</a></code> or by assigning an event listener to the <code>on<em>eventname</em></code> property of this interface.</p>

<dl>
 <dt><code><a href="/en-US/docs/Web/API/Window/error_event">error</a></code></dt>
 <dd>Fired when when a resource failed to load, or can't be used. For example, if a script has an execution error or an image can't be found or is invalid.<br>
 Also available via the {{domxref("GlobalEventHandlers/onerror", "onerror")}} 属性。</dd>
 <dt><code><a href="/en-US/docs/Web/API/Window/languagechange_event">languagechange</a></code></dt>
 <dd>Fired at the global scope object when the user's preferred language changes.<br>
 Also available via the <code><a href="/en-US/docs/Web/API/Window/languagechange_event">onlanguagechange</a></code> 属性。</dd>
 <dt><code><a href="/en-US/docs/Web/API/Window/orientationchange_event">orientationchange</a></code></dt>
 <dd>Fired when the orientation of the device has changed.<br>
 Also available via the <code><a href="/en-US/docs/Web/API/Window/onorientationchange">onorientationchange</a></code> 属性。</dd>
 <dt><code><a href="/en-US/docs/Web/API/Window/devicemotion_event">devicemotion</a></code></dt>
 <dd>Fired at a regular interval, indicating the amount of physical force of acceleration the device is receiving and the rate of rotation, if available.</dd>
 <dt><code><a href="/en-US/docs/Web/API/Window/deviceorientation_event">deviceorientation</a></code></dt>
 <dd>Fired when fresh data is available from the magnetometer orientation sensor about the current orientation of the device as compared to the Earth coordinate frame.</dd>
 <dt><code>{{domxref("Document/defaultView/resize_event", "resize")}}</code></dt>
 <dd>Fired when the window has been resized.<br>
 Also available via the <code><a href="/en-US/docs/Web/API/GlobalEventHandlers/onresize">onresize</a></code> 属性。</dd>
 <dt><code>{{domxref("Document/defaultView/storage_event", "storage")}}</code></dt>
 <dd>Fired when a storage area (<code>localStorage</code> or <code>sessionStorage</code>) has been modified in the context of another document.<br>
 Also available via the <code><a href="/en-US/docs/Web/API/Window/storage_event">onstorage</a></code> 属性。</dd>
</dl>

<h3 id="Animation_events">Animation events</h3>

<dl>
 <dt><code><a href="/en-US/docs/Web/API/Window/animationcancel_event">animationcancel</a></code></dt>
 <dd>Fired when an animation unexpectedly aborts.<br>
 Also available via the <code><a href="/en-US/docs/Web/API/GlobalEventHandlers/onanimationcancel">onanimationcancel</a></code> 属性。</dd>
 <dt><code><a href="/en-US/docs/Web/API/Window/animationend_event">animationend</a></code></dt>
 <dd>Fired when an animation has completed normally.<br>
 Also available via the <code><a href="/en-US/docs/Web/API/GlobalEventHandlers/onanimationend">onanimationend</a></code> 属性。</dd>
 <dt><code><a href="/en-US/docs/Web/API/Window/animationiteration_event">animationiteration</a></code></dt>
 <dd>Fired when an animation iteration has completed.<br>
 Also available via the <code><a href="/en-US/docs/Web/API/GlobalEventHandlers/onanimationiteration">onanimationiteration</a></code> 属性。</dd>
 <dt><code><a href="/en-US/docs/Web/API/Window/animationstart_event">animationstart</a></code></dt>
 <dd>Fired when an animation starts.<br>
 Also available via the <code><a href="/en-US/docs/Web/API/GlobalEventHandlers/onanimationstart">onanimationstart</a></code> 属性。</dd>
</dl>

<h3 id="Clipboard_events">Clipboard events</h3>

<dl>
 <dt><code><a href="/en-US/docs/Web/API/Window/clipboardchange_event">clipboardchange</a></code></dt>
 <dd>Fired when the system clipboard content changes.</dd>
 <dt><code><a href="/en-US/docs/Web/API/Window/copy_event">copy</a></code></dt>
 <dd>Fired when the user initiates a copy action through the browser's user interface.<br>
 Also available via the <a href="/en-US/docs/Web/API/HTMLElement/oncopy"><code>oncopy</code></a> 属性。</dd>
 <dt><code><a href="/en-US/docs/Web/API/Window/cut_event">cut</a></code></dt>
 <dd>Fired when the user initiates a cut action through the browser's user interface.<br>
 Also available via the <a href="/en-US/docs/Web/API/HTMLElement/oncut"><code>oncut</code></a> 属性。</dd>
 <dt><code><a href="/en-US/docs/Web/API/Window/paste_event">paste</a></code></dt>
 <dd>Fired when the user initiates a paste action through the browser's user interface.<br>
 Also available via the <a href="/en-US/docs/Web/API/HTMLElement/onpaste"><code>onpaste</code></a> 属性。</dd>
</dl>

<h3 id="Connection_events">Connection events</h3>

<dl>
 <dt><code><a href="/en-US/docs/Web/API/Window/offline_event">offline</a></code></dt>
 <dd>Fired when the browser has lost access to the network and the value of <code>navigator.onLine</code> has switched to <code>false</code>.<br>
 Also available via the {{domxref("WindowEventHandlers.onoffline", "onoffline")}} 属性。</dd>
 <dt><code><a href="/en-US/docs/Web/API/Window/online_event">online </a></code></dt>
 <dd>Fired when the browser has gained access to the network and the value of <code>navigator.onLine</code> has switched to <code>true</code>.<br>
 Also available via the {{domxref("WindowEventHandlers.ononline", "ononline")}} 属性。</dd>
</dl>

<h3 id="Focus_events">Focus events</h3>

<dl>
 <dt><code><a href="/en-US/docs/Web/API/Window/blur_event">blur</a></code></dt>
 <dd>Fired when an element has lost focus.<br>
 Also available via the <a href="/en-US/docs/Web/API/GlobalEventHandlers/onblur"><code>onblur</code></a> 属性。</dd>
 <dt><code><a href="/en-US/docs/Web/API/Window/focus_event">focus</a></code></dt>
 <dd>Fired when an element has gained focus.<br>
 Also available via the <a href="/en-US/docs/Web/API/GlobalEventHandlers/onfocus"><code>onfocus</code></a> property</dd>
</dl>

<h3 id="Gamepad_events">Gamepad events</h3>

<dl>
 <dt><code><a href="/en-US/docs/Web/API/Window/gamepadconnected_event">gamepadconnected</a></code></dt>
 <dd>Fired when the browser detects that a gamepad has been connected or the first time a button/axis of the gamepad is used.<br>
 Also available via the <code><a href="/en-US/docs/Web/API/Window/ongamepadconnected">ongamepadconnected</a></code> 属性。</dd>
 <dt><code><a href="/en-US/docs/Web/API/Window/gamepaddisconnected_event">gamepaddisconnected</a></code></dt>
 <dd>Fired when the browser detects that a gamepad has been disconnected.<br>
 Also available via the <code><a href="/en-US/docs/Web/API/Window/ongamepaddisconnected">ongamepaddisconnected</a></code> property</dd>
</dl>

<h3 id="History_events">History events</h3>

<dl>
 <dt><code><a href="/en-US/docs/Web/API/Window/hashchange_event">hashchange</a></code></dt>
 <dd>Fired when the fragment identifier of the URL has changed (the part of the URL beginning with and following the <code>#</code> symbol).<br>
 Also available via the <code><a href="/en-US/docs/Web/API/Window/hashchange_event">onhashchange</a></code> 属性。</dd>
 <dt><code><a href="/en-US/docs/Web/API/Window/pagehide_event">pagehide</a></code></dt>
 <dd>Sent when the browser hides the current document while in the process of switching to displaying in its palce a different document from the session's history. This happens, for example, when the user clicks the Back button or when they click the Forward button to move ahead in session history.<br>
 Also available through the <code><a href="/en-US/docs/Mozilla/Tech/XUL/Attribute/onpagehide">onpagehide</a></code> event handler 属性。</dd>
 <dt><code><a href="/en-US/docs/Web/API/Window/pageshow_event">pageshow</a></code></dt>
 <dd>Sent when the browser makes the document visible due to navigation tasks, including not only when the page is first loaded, but also situations such as the user navigating back to the page after having navigated to another within the same tab.<br>
 Also available using the <code><a href="/en-US/docs/Mozilla/Tech/XUL/Attribute/onpageshow">onpageshow</a></code> event handler 属性。</dd>
 <dt><code>{{domxref("Document/defaultView/popstate_event", "popstate")}}</code></dt>
 <dd>Fired when the active history entry changes.<br>
 Also available using the <code><a href="/en-US/docs/Web/API/Window/popstate_event">onpopstate</a></code> event handler 属性。</dd>
</dl>

<h3 id="Load_unload_events">Load &amp; unload events</h3>

<dl>
 <dt><code><a href="/en-US/docs/Web/API/Window/beforeunload_event">beforeunload</a></code></dt>
 <dd>Fired when the window, the document and its resources are about to be unloaded.<br>
 Also available via the <code><a href="/en-US/docs/Web/API/Window/beforeunload_event">onbeforeunload</a></code> 属性。</dd>
 <dt><code><a href="/en-US/docs/Web/API/Window/DOMContentLoaded_event">DOMContentLoaded</a></code></dt>
 <dd>Fired when the document has been completely loaded and parsed, without waiting for stylesheets, images, and subframes to finish loading.</dd>
 <dt><code><a href="/en-US/docs/Web/API/Window/load_event">load</a></code></dt>
 <dd>Fired when the whole page has loaded, including all dependent resources such as stylesheets images.<br>
 Also available via the <code><a href="/en-US/docs/Web/API/GlobalEventHandlers/onload">onload</a></code> 属性。</dd>
 <dt><code><a href="/en-US/docs/Web/API/Window/unload_event">unload</a></code></dt>
 <dd>Fired when the document or a child resource is being unloaded.<br>
 Also available via the <code><a href="/en-US/docs/Web/API/Window/unload_event">onunload</a></code> 属性。</dd>
</dl>

<h3 id="Manifest_events">Manifest events</h3>

<dl>
 <dt><code><a href="/en-US/docs/Web/API/Window/appinstalled_event">appinstalled</a></code></dt>
 <dd>Fired when the browser has successfully installed a page as an application.<br>
 Also available via the <a href="/en-US/docs/Web/API/Window/onappinstalled">onappinstalled</a> 属性。</dd>
 <dt><code><a href="/en-US/docs/Web/API/Window/beforeinstallprompt_event">beforeinstallprompt</a></code></dt>
 <dd>Fired when a user is about to be prompted to install a web application.<br>
 Also available via the <code><a href="/en-US/docs/Web/API/Window/onbeforeinstallprompt">onbeforeinstallprompt</a></code> 属性。</dd>
</dl>

<h3 id="Messaging_events">Messaging events</h3>

<dl>
 <dt><code><a href="/en-US/docs/Web/API/Window/message_event">message</a></code></dt>
 <dd>Fired when the window receives a message, for example from a call to <code><a href="/en-US/docs/Web/API/Window/postMessage">Window.postMessage()</a></code> from another browsing context.<br>
 Also available via the <code><a href="/en-US/docs/Web/API/Window/message_event">onmessage</a></code> 属性。</dd>
 <dt><code><a href="/en-US/docs/Web/API/Window/messageerror_event">messageerror</a></code></dt>
 <dd>Fired when a <code>Window</code> object receives a message that can't be deserialized.<br>
 Also available via the <code><a href="/en-US/docs/Web/API/Window/messageerror_event">onmessageerror</a></code> 属性。</dd>
</dl>

<h3 id="Print_events">Print events</h3>

<dl>
 <dt><code><a href="/en-US/docs/Web/API/Window/afterprint_event">afterprint</a></code></dt>
 <dd>Fired after the associated document has started printing or the print preview has been closed.<br>
 Also available via the <a href="/en-US/docs/Web/API/Window/afterprint_event"><code>onafterprint</code></a> 属性。</dd>
 <dt><code><a href="/en-US/docs/Web/API/Window/beforeprint_event">beforeprint</a></code></dt>
 <dd>Fired when the associated document is about to be printed or previewed for printing.<br>
 Also available via the <a href="/en-US/docs/Web/API/Window/beforeprint_event"><code>onbeforeprint</code></a> 属性。</dd>
</dl>

<h3 id="Promise_rejection_events">Promise rejection events</h3>

<dl>
 <dt><code><a href="/en-US/docs/Web/API/Window/rejectionhandled_event">rejectionhandled</a></code></dt>
 <dd>Sent every time a JavaScript {{jsxref("Promise")}} is rejected, regardless of whether or not there is a handler in place to catch the rejection.<br>
 Also available through the <code><a href="/en-US/docs/Web/API/Window/rejectionhandled_event">onrejectionhandled</a></code> event handler 属性。</dd>
 <dt><code><a href="/en-US/docs/Web/API/Window/unhandledrejection_event">unhandledrejection</a></code></dt>
 <dd>Sent when a JavaScript {{jsxref("Promise")}} is rejected but there is no handler in place to catch the rejection.<br>
 Also available using the <code><a href="/en-US/docs/Web/API/Window/unhandledrejection_event">onunhandledrejection</a></code> event handler 属性。</dd>
</dl>

<h3 id="Transition_events">Transition events</h3>

<dl>
 <dt><code><a href="/en-US/docs/Web/API/Window/transitioncancel_event">transitioncancel</a></code></dt>
 <dd>Fired when a <a href="/en-US/docs/CSS/Using_CSS_transitions">CSS transition</a> is canceled.<br>
 Also available via the <code><a href="/en-US/docs/Web/API/GlobalEventHandlers/ontransitioncancel">ontransitioncancel</a></code> 属性。</dd>
 <dt><code><a href="/en-US/docs/Web/API/Window/transitionend_event">transitionend</a></code></dt>
 <dd>Fired when a <a href="/en-US/docs/CSS/Using_CSS_transitions">CSS transition</a> has completed.<br>
 Also available via the <code><a href="/en-US/docs/Web/API/GlobalEventHandlers/ontransitionend">ontransitionend</a></code> 属性。</dd>
 <dt><code><a href="/en-US/docs/Web/API/Window/transitionrun_event">transitionrun</a></code></dt>
 <dd>Fired when a <a href="/en-US/docs/CSS/Using_CSS_transitions">CSS transition</a> is first created.<br>
 Also available via the <code><a href="/en-US/docs/Web/API/GlobalEventHandlers/ontransitionrun">ontransitionrun</a></code> 属性。</dd>
 <dt><code><a href="/en-US/docs/Web/API/Window/transitionstart_event">transitionstart</a></code></dt>
 <dd>Fired when a <a href="/en-US/docs/CSS/Using_CSS_transitions">CSS transition</a> has actually started.<br>
 Also available via the <code><a href="/en-US/docs/Web/API/GlobalEventHandlers/ontransitionstart">ontransitionstart</a></code> 属性。</dd>
</dl>

<h3 id="WebVR_events">WebVR events</h3>

<dl>
 <dt><code><a href="/en-US/docs/Web/API/Window/vrdisplayactivate_event">vrdisplayactivate</a></code></dt>
 <dd>Fired when a VR display becomes available to be presented to, for example if an HMD has been moved to bring it out of standby, or woken up by being put on.<br>
 Also available via the <code><a href="/en-US/docs/Web/API/Window/onvrdisplayactivate">onvrdisplayactivate</a></code> 属性。</dd>
 <dt><code><a href="/en-US/docs/Web/API/Window/vrdisplayblur_event">vrdisplayblur</a></code></dt>
 <dd>Fired when presentation to a VR display has been paused for some reason by the browser, OS, or VR hardware.<br>
 Also available via the <code><a href="/en-US/docs/Web/API/Window/onvrdisplayblur">onvrdisplayblur</a></code> 属性。</dd>
 <dt><code><a href="/en-US/docs/Web/API/Window/vrdisplayconnect_event">vrdisplayconnect</a></code></dt>
 <dd>Fired when a compatible VR display is connected to the computer.<br>
 Also available via the <code><a href="/en-US/docs/Web/API/Window/onvrdisplayconnect">onvrdisplayconnect</a></code> 属性。</dd>
 <dt><code><a href="/en-US/docs/Web/API/Window/vrdisplaydeactivate_event">vrdisplaydeactivate</a></code></dt>
 <dd>Fired when a VR display can no longer be presented to, for example if an HMD has gone into standby or sleep mode due to a period of inactivity.<br>
 Also available via the <code><a href="/en-US/docs/Web/API/Window/onvrdisplaydeactivate">onvrdisplaydeactivate</a></code> 属性。</dd>
 <dt><code><a href="/en-US/docs/Web/API/Window/vrdisplaydisconnect_event">vrdisplaydisconnect</a></code></dt>
 <dd>Fired when a compatible VR display is disconnected from the computer.<br>
 Also available via the <code><a href="/en-US/docs/Web/API/Window/onvrdisplaydisconnect">onvrdisplaydisconnect</a></code> 属性。</dd>
 <dt><code><a href="/en-US/docs/Web/API/Window/vrdisplayfocus_event">vrdisplayfocus</a></code></dt>
 <dd>Fired when presentation to a VR display has resumed after being blurred.<br>
 Also available via the <code><a href="/en-US/docs/Web/API/Window/onvrdisplayfocus">onvrdisplayfocus</a></code> 属性。</dd>
 <dt><code><a href="/en-US/docs/Web/API/Window/vrdisplaypresentchange_event">vrdisplaypresentchange</a></code></dt>
 <dd>fired when the presenting state of a VR display changes — i.e. goes from presenting to not presenting, or vice versa.<br>
 Also available via the <code><a href="/en-US/docs/Web/API/Window/onvrdisplaypresentchange">onvrdisplaypresentchange</a></code> 属性。</dd>
 <dt><code><a href="/en-US/docs/Web/API/Window/vrdisplaypointerrestricted_event">vrdisplaypointerrestricted</a></code></dt>
 <dd>Fired when the VR display's pointer input is restricted to consumption via a <a href="/en-US/docs/Web/API/Pointer_Lock_API">pointerlocked element</a>.<br>
 Also available via the <code><a href="/en-US/docs/Web/API/Window/onvrdisplaypointerrestricted">onvrdisplaypointerrestricted</a></code> 属性。</dd>
 <dt><code><a href="/en-US/docs/Web/API/Window/vrdisplaypointerunrestricted_event">vrdisplaypointerunrestricted</a></code></dt>
 <dd>Fired when the VR display's pointer input is no longer restricted to consumption via a <a href="/en-US/docs/Web/API/Pointer_Lock_API">pointerlocked element</a>.<br>
 Also available via the <code><a href="/en-US/docs/Web/API/Window/onvrdisplaypointerunrestricted">onvrdisplaypointerunrestricted</a></code> 属性。</dd>
</dl>

<h2 id="接口">接口</h2>

<p>See <a href="/en-US/docs/DOM/DOM_Reference">DOM Reference</a></p>

<h2 id="浏览器兼容性">浏览器兼容性</h2>



<p>{{Compat("api.Window")}}</p>

<h2 id="参见">参见</h2>

<ul>
 <li><a href="/en-US/docs/Working_with_windows_in_chrome_code">Working with windows in chrome code</a></li>
</ul>