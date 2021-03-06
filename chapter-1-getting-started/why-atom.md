# 为什么选择 Atom？

这个世界上有那么多种编辑器，为什么你要花时间学习和使用 Atom 呢？

虽然 Sublime 和 TextMate 之类的编辑器已经非常好用了，但它们仅提供了很有限的拓展性。而在另一个极端，Emacs 和 Vim 提供了灵活的拓展性，但它们并不是很友好，需要使用专用的编程语言来配置和拓展。

我们觉得我们可以做得更好。我们的目标是在保证易用性的同时提供充分的可拓展性（hackability）：这个编辑器会受到第一天学习编程的新生欢迎，而且当他们成长为编程专家时也难以割舍。

当我们使用 Atom 来开发 Atom 的时候，随着它的逐渐完善，我们愈发觉得已经离不开它了。从表面上来看，Atom 是一个能满足你的期待的，现代化的桌面文本编辑器，而在表面之下，这是一个值得你去一同完善的系统。

## Atom 的核心

Web 技术虽然有其缺陷，但经过二十年的发展，Web 已经逐渐成长为了一个强大的具有活力的平台。所以当我们计划写一个自用的可拓展的文本编辑器时，Web 技术显然是一个好的选择，但首先我们需要摆脱来自 Web 的限制。

### 混合本地代码与 Web 技术

Web 浏览器很适合用来浏览网页，但写代码是一种需要可靠的工具的专业活动。更重要的是，浏览器出于安全的考虑，严格限制了对本地系统的访问，但对一个文本编辑器而言，不能向本地系统写入文件是不可接受的。

因此，我们没有把 Atom 构建为一个传统的 Web 应用，Atom 是一个专门被设计用作文本编辑器，而不是网页浏览器的 Chromium 定制版。Atom 的每一个窗口实际上都是一个本地渲染的网页。

所有来自 Node.js 可用的 API 在 Atom 窗口的 JavaScript 中同样可用，这种结合带来了一种独一无二的开发体验。

因为一切都是本地的，你不需要将静态资源打包、不需要关注脚本的异步加载，如果你希望加载一些代码。只需要在文件的最顶部 `require` 它即可，Node.js 的模块系统允许你将一个系统分割为小的、专注于某一功能的包。

### JavaScript 与 C++ 的结合

与原生代码交互也很简单。例如，你基于 Oniguruma 正则引擎开发了一个用来提供对 TextMate 语法识别的支持。在浏览器里，你可能需要使用 NaCl 或 Esprima, 而在 Node 里这个过程变得非常简单。

在 Node.js 的 API 之外，我们还提供了一些 API 例如使用系统的对话框、使用菜单栏和右键菜单、操纵窗口尺寸等等。

### Web 技术：最有趣的部分

另一个好消息就是当你为 Atom 编写代码时，这些代码一定会被允许在最新版本的 Chromium 中。这意味着你可以无视与浏览器兼容性有关的黑科技，使用全部的最新的 Web 功能。

例如，Atom 的工作区和窗格都是基于 flexbox 来进行布局的。这是一项刚刚出现的技术，从我们使用它之后也发生了很多变化，但不要紧，因为它工作得很好。

我们确信将 Atom 构建在 Web 技术之上是一个好的选择，因为整个行业都在推动着 Web 技术的发展。原生UI技术不断产生又不断淘汰，而 Web 是一个每年都变得更加强大和普及的标准。我们对于深入探索这一强大的技术感到无比兴奋。

## 一个开源的文本编辑器

GitHub 的目标是帮助大家构建更好的软件，而 Atom 则是实现这一目标的重要补充。Atom 是一项长期的投资，GitHub 会持续投入开发力量来推动它的发展。但我们也意识到不能让它受限于我们的能力，就像之所以 Emacs 和 Vim 在过去的三十年间被广泛使用，是因为只有开源，才能构建一个持久的、有活力的文本编辑器社区。

整个 Atom 编辑器都是免费且开源的，你可以在 <https://github.com/atom> 这个组织下找到它。
