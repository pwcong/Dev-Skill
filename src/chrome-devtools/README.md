# Chrome DevTools 中的骚操作

### 截图 DOM 元素

当你只想对一个特别的 DOM 节点进行截图时，你可能需要使用其他工具弄半天，但现在你直接选中那个节点，打开 命令（Command） 菜单并且使用 节点截图 就可以了。

截取特定节点对应上图命令是 `Screenshot Capture node screenshot` 。

不只是这样，你同样可以用这种方式 实现全屏截图 ：通过 `Screenshot Capture full size screenshot` 命令。

在控制台中使用上次操作的值

使用$_可以引用在控制台执行的前一步操作的返回值。如果您正在控制台调试一些 JavaScript 代码，并且需要引用先前的返回值，那么这可能非常方便。

### 编辑页面上的任何文本 

在控制台输入 `document.body.contentEditable="true"` 或者 `document.designMode = 'on'` 就可以实现对网页的编辑了。

### 动画检查

DevTools 中有一个动画面板，默认情况下它是关闭的，很多人可能不太清楚这个功能。它可以让你控制和操纵 CSS 动画，并且可视化这些动画是如何工作的。
要打开该面板，可以在 DevTools 右上角菜单 → More tools 中打开 Animations ：

默认情况下，DevTools 会“监听”动画。一旦触发，它们将被添加到列表中。你能看到这些动画块如何显示。在动画本身上，DevTools 会向我们展示哪些属性正在更改，例如 background-color 或 transform。
然后，我们可以通过使用鼠标拖动或调整时间轴来修改该动画：

### 递增/递减 CSS 属性值

作为前端开发，平时少不了通过 Elements 面板去查找元素以及它的 css 样式。有时调整像素 px 会比较麻烦一点，这时就可以使用快捷键去帮你完成：

- 增量 0.1
  - Mac： Option +向上和 Option +向下
  - Windows： Alt +向上和 Alt +向下
- 增量 1
  - Mac：向上+向下
  - Windows：向上+向下
- 增量 10
  - Mac：⇧+向上和 ⇧+向下
  - Windows：⇧+向上和 ⇧+向下
- 递增 100
  - Mac： ⌘+向上和 ⌘+向下
  - Windows： Ctrl +向上和 Ctrl +向下
    复制代码
    在低端设备和弱网情况下进行测试 📱
    我们平时开发一般都是在办公室（wifi 网速加快），而且设备一般都是市面上较新的。但是产品的研发和推广，一定要考虑低设备人群和弱网的情况。
    在 Chrome DevTools 中可以轻松调节 CPU 功能和网络速度。这样，我们就可以测试 Web 应用程序性能并进行相应优化。
    具体打开方式是：在 Chrome DevTools 中通过 CMD/Ctrl + Shift + p 打开命令菜单。然后输入 Show Performance 打开性能面板。

### copying & saving

在调试的过程中，我们总会有对 Dev Tools 里面的数据进行 复制 或者 保存 的操作，其实他们也是有一些小技巧的！
copy()
可以通过全局的方法 copy() 在 console 里 copy 任何你能拿到的资源

### table

Devtools 提供的用于将对象数组记录为表格的 API
