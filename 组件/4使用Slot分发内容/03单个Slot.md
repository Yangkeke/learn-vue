### 单个Slot

除非子组件模板包括至少一个 <slot> 插口，否则父组件的内容就会被丢弃。 当子组件模板只有一个没有属性的slot时，父组件整个内容段将插入到slot所在的DOM位置，并替换掉slot标签本身。

最初在 <slot> 标签中的任何内容都被视为备用内容。备用内容在子组件的作用域内编译，并且只有宿主元素为空，且没有要插入的内容才显示备用内容。

假定 my-component 组件有下面模板：

<div>
  <h2>我是子组件的标题</h2>
  <slot>
    只有在没有要分发的内容时才会显示
  </slot>
</div>

父组件模板：

<div>
  <h1>我是父组件的标题</h1>
  <my-component>
    <p>这是一些初始内容</p>
    <p>这是更多的初始内容</p>
  </my-component>
</div>

渲染结果：

<div>
  <h1>我是父组件的标题</h1>
  <div>
    <h2>我是子组件的标题</h2>
    <p>这是一些初始内容</p>
    <p>这是更多的初始内容</p>
  </div>
</div>