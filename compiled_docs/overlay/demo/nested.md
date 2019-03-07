{"title":"弹层嵌套","meta":{"title":"弹层嵌套","description":"\n<p>有弹层嵌套需求时，请使用 container 属性将第二个弹层渲染到第一个弹层内部。</p>\n","order":"4"},"codes":{"jsx":"import { Overlay } from '@alifd/next';\n\nconst { Popup } = Overlay;\n\nReactDOM.render(\n    <Popup trigger={<button>Open first overlay</button>}\n        triggerType=\"click\">\n        <div className=\"overlay-demo\">\n            <Popup trigger={<button>Open second overlay</button>}\n                triggerType=\"click\"\n                container={trigger => trigger.parentNode}>\n                <div className=\"overlay-demo\">\n                    <p>Hello World From Second Overlay!</p>\n                </div>\n            </Popup>\n            <p>Hello World From First Overlay!</p>\n        </div>\n    </Popup>\n    , mountNode);\n","css":".overlay-demo {\n    width: 300px;\n    height: 100px;\n    padding: 10px;\n    border: 1px solid #999999;\n    background: #FFFFFF;\n    box-shadow: 2px 2px 20px rgba(0,0,0,0.15);\n}\n"},"body":"\n\n````jsx\nimport { Overlay } from '@alifd/next';\n\nconst { Popup } = Overlay;\n\nReactDOM.render(\n    <Popup trigger={<button>Open first overlay</button>}\n        triggerType=\"click\">\n        <div className=\"overlay-demo\">\n            <Popup trigger={<button>Open second overlay</button>}\n                triggerType=\"click\"\n                container={trigger => trigger.parentNode}>\n                <div className=\"overlay-demo\">\n                    <p>Hello World From Second Overlay!</p>\n                </div>\n            </Popup>\n            <p>Hello World From First Overlay!</p>\n        </div>\n    </Popup>\n    , mountNode);\n````\n\n````css\n.overlay-demo {\n    width: 300px;\n    height: 100px;\n    padding: 10px;\n    border: 1px solid #999999;\n    background: #FFFFFF;\n    box-shadow: 2px 2px 20px rgba(0,0,0,0.15);\n}\n````","html":"<script>(function(){\"use strict\";\n\nvar _next = require(\"@alifd/next\");\n\nvar Popup = _next.Overlay.Popup;\n\n\nReactDOM.render(React.createElement(\n    Popup,\n    { trigger: React.createElement(\n            \"button\",\n            null,\n            \"Open first overlay\"\n        ),\n        triggerType: \"click\" },\n    React.createElement(\n        \"div\",\n        { className: \"overlay-demo\" },\n        React.createElement(\n            Popup,\n            { trigger: React.createElement(\n                    \"button\",\n                    null,\n                    \"Open second overlay\"\n                ),\n                triggerType: \"click\",\n                container: function container(trigger) {\n                    return trigger.parentNode;\n                } },\n            React.createElement(\n                \"div\",\n                { className: \"overlay-demo\" },\n                React.createElement(\n                    \"p\",\n                    null,\n                    \"Hello World From Second Overlay!\"\n                )\n            )\n        ),\n        React.createElement(\n            \"p\",\n            null,\n            \"Hello World From First Overlay!\"\n        )\n    )\n), mountNode);})()</script><div class=\"highlight\"><pre class=\"language-jsx\"><code class=\"language-jsx\"><span class=\"token keyword\">import</span> <span class=\"token punctuation\">{</span> Overlay <span class=\"token punctuation\">}</span> <span class=\"token keyword\">from</span> <span class=\"token string\">'@alifd/next'</span><span class=\"token punctuation\">;</span>\n\n<span class=\"token keyword\">const</span> <span class=\"token punctuation\">{</span> Popup <span class=\"token punctuation\">}</span> <span class=\"token operator\">=</span> Overlay<span class=\"token punctuation\">;</span>\n\nReactDOM<span class=\"token punctuation\">.</span><span class=\"token function\">render</span><span class=\"token punctuation\">(</span>\n    <span class=\"token tag\"><span class=\"token tag\"><span class=\"token punctuation\">&lt;</span>Popup</span> <span class=\"token attr-name\">trigger</span><span class=\"token script language-javascript\"><span class=\"token script-punctuation punctuation\">=</span><span class=\"token punctuation\">{</span><span class=\"token tag\"><span class=\"token tag\"><span class=\"token punctuation\">&lt;</span>button</span><span class=\"token punctuation\">></span></span><span class=\"token plain-text\">Open first overlay</span><span class=\"token tag\"><span class=\"token tag\"><span class=\"token punctuation\">&lt;/</span>button</span><span class=\"token punctuation\">></span></span><span class=\"token punctuation\">}</span></span>\n        <span class=\"token attr-name\">triggerType</span><span class=\"token attr-value\"><span class=\"token punctuation\">=</span><span class=\"token punctuation\">\"</span>click<span class=\"token punctuation\">\"</span></span><span class=\"token punctuation\">></span></span><span class=\"token plain-text\">\n        </span><span class=\"token tag\"><span class=\"token tag\"><span class=\"token punctuation\">&lt;</span>div</span> <span class=\"token attr-name\">className</span><span class=\"token attr-value\"><span class=\"token punctuation\">=</span><span class=\"token punctuation\">\"</span>overlay-demo<span class=\"token punctuation\">\"</span></span><span class=\"token punctuation\">></span></span><span class=\"token plain-text\">\n            </span><span class=\"token tag\"><span class=\"token tag\"><span class=\"token punctuation\">&lt;</span>Popup</span> <span class=\"token attr-name\">trigger</span><span class=\"token script language-javascript\"><span class=\"token script-punctuation punctuation\">=</span><span class=\"token punctuation\">{</span><span class=\"token tag\"><span class=\"token tag\"><span class=\"token punctuation\">&lt;</span>button</span><span class=\"token punctuation\">></span></span><span class=\"token plain-text\">Open second overlay</span><span class=\"token tag\"><span class=\"token tag\"><span class=\"token punctuation\">&lt;/</span>button</span><span class=\"token punctuation\">></span></span><span class=\"token punctuation\">}</span></span>\n                <span class=\"token attr-name\">triggerType</span><span class=\"token attr-value\"><span class=\"token punctuation\">=</span><span class=\"token punctuation\">\"</span>click<span class=\"token punctuation\">\"</span></span>\n                <span class=\"token attr-name\">container</span><span class=\"token script language-javascript\"><span class=\"token script-punctuation punctuation\">=</span><span class=\"token punctuation\">{</span>trigger <span class=\"token operator\">=></span> trigger<span class=\"token punctuation\">.</span>parentNode<span class=\"token punctuation\">}</span></span><span class=\"token punctuation\">></span></span><span class=\"token plain-text\">\n                </span><span class=\"token tag\"><span class=\"token tag\"><span class=\"token punctuation\">&lt;</span>div</span> <span class=\"token attr-name\">className</span><span class=\"token attr-value\"><span class=\"token punctuation\">=</span><span class=\"token punctuation\">\"</span>overlay-demo<span class=\"token punctuation\">\"</span></span><span class=\"token punctuation\">></span></span><span class=\"token plain-text\">\n                    </span><span class=\"token tag\"><span class=\"token tag\"><span class=\"token punctuation\">&lt;</span>p</span><span class=\"token punctuation\">></span></span><span class=\"token plain-text\">Hello World From Second Overlay!</span><span class=\"token tag\"><span class=\"token tag\"><span class=\"token punctuation\">&lt;/</span>p</span><span class=\"token punctuation\">></span></span><span class=\"token plain-text\">\n                </span><span class=\"token tag\"><span class=\"token tag\"><span class=\"token punctuation\">&lt;/</span>div</span><span class=\"token punctuation\">></span></span><span class=\"token plain-text\">\n            </span><span class=\"token tag\"><span class=\"token tag\"><span class=\"token punctuation\">&lt;/</span>Popup</span><span class=\"token punctuation\">></span></span><span class=\"token plain-text\">\n            </span><span class=\"token tag\"><span class=\"token tag\"><span class=\"token punctuation\">&lt;</span>p</span><span class=\"token punctuation\">></span></span><span class=\"token plain-text\">Hello World From First Overlay!</span><span class=\"token tag\"><span class=\"token tag\"><span class=\"token punctuation\">&lt;/</span>p</span><span class=\"token punctuation\">></span></span><span class=\"token plain-text\">\n        </span><span class=\"token tag\"><span class=\"token tag\"><span class=\"token punctuation\">&lt;/</span>div</span><span class=\"token punctuation\">></span></span><span class=\"token plain-text\">\n    </span><span class=\"token tag\"><span class=\"token tag\"><span class=\"token punctuation\">&lt;/</span>Popup</span><span class=\"token punctuation\">></span></span>\n    <span class=\"token punctuation\">,</span> mountNode<span class=\"token punctuation\">)</span><span class=\"token punctuation\">;</span></code></pre></div><style type=\"text/css\">.overlay-demo {\n    width: 300px;\n    height: 100px;\n    padding: 10px;\n    border: 1px solid #999999;\n    background: #FFFFFF;\n    box-shadow: 2px 2px 20px rgba(0,0,0,0.15);\n}</style><div class=\"highlight\"><pre class=\"language-css\"><code class=\"language-css\"><span class=\"token selector\">.overlay-demo</span> <span class=\"token punctuation\">{</span>\n    <span class=\"token property\">width</span><span class=\"token punctuation\">:</span> 300px<span class=\"token punctuation\">;</span>\n    <span class=\"token property\">height</span><span class=\"token punctuation\">:</span> 100px<span class=\"token punctuation\">;</span>\n    <span class=\"token property\">padding</span><span class=\"token punctuation\">:</span> 10px<span class=\"token punctuation\">;</span>\n    <span class=\"token property\">border</span><span class=\"token punctuation\">:</span> 1px solid #999999<span class=\"token punctuation\">;</span>\n    <span class=\"token property\">background</span><span class=\"token punctuation\">:</span> #FFFFFF<span class=\"token punctuation\">;</span>\n    <span class=\"token property\">box-shadow</span><span class=\"token punctuation\">:</span> 2px 2px 20px <span class=\"token function\">rgba</span><span class=\"token punctuation\">(</span>0,0,0,0.15<span class=\"token punctuation\">)</span><span class=\"token punctuation\">;</span>\n<span class=\"token punctuation\">}</span></code></pre></div>"}