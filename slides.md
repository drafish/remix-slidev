---
# try also 'default' to start simple
theme: seriph
# random image from a curated Unsplash collection by Anthony
# like them? see https://unsplash.com/collections/94734566/slidev
background: https://source.unsplash.com/collection/94734566/1920x1080
# apply any windi css classes to the current slide
class: 'text-center'
# https://sli.dev/custom/highlighters.html
highlighter: shiki
# show line numbers in code blocks
lineNumbers: false
# some information about the slides, markdown enabled
info: |
  ## Slidev Starter Template
  Presentation slides for developers.

  Learn more at [Sli.dev](https://sli.dev)
# persist drawings in exports and build
drawings:
  persist: false
# page transition
transition: slide-left
# use UnoCSS
css: unocss
---

# Remix China 项目介绍

---
layout: center
---
# 翻译计划
<br />

# 开发计划
<br />

# 运营计划
<br />

# 研究计划


---
layout: default
---

# 翻译计划

#### IDE 文档
这就是 Remix IDE 的使用文档，详细地介绍了每一个功能模块的使用方法。

- 文档地址：https://remix-ide.readthedocs.io/en/latest/index.html
- 文档仓库地址：https://github.com/ethereum/remix-ide
- crowdin：https://crowdin.com/project/remix-translation/zh-CN
- 翻译完成度：71%
- 审阅完成度：0
- 单词量：29630

---
layout: default
---

# 翻译计划
#### IDE 操作界面
目前为止 IDE 操作界面的中文翻译完成度已经非常高了，估计超过 90% 。点击下面的链接就可以体验中文版的 Remix IDE 。
https://remix.ethereum.org/?#lang=zh

- IDE 仓库地址：https://github.com/ethereum/remix-project
- crowdin：Remix 团队计划是把操作界面的翻译放到 crowdin 上维护，但目前还没放上去
- 翻译完成度：超过 90%
- 审阅完成度：0

---
layout: default
---

# 翻译计划
#### LearnEth 教程
LearnEth 是 Remix IDE 上的一个插件，它可以把 Remix IDE 变成一个交互式教学平台。大家可以通过下面的链接先体验下
https://remix.ethereum.org/?#activate=LearnEth

Remix 团队已经开发了两套课程。将来可能还会开发更多的课程。

- 教程仓库地址：https://github.com/ethereum/remix-workshops  https://github.com/Aniket-Engg/solidity-school
- crowdin：LearnETH 教程一旦制作完成就不会经常更新，是否要放到 crowdin 上维护尚需讨论
- 翻译完成度：0
- 审阅完成度：0
- 单词量：19455 + 3656

---
layout: default
---

# 开发计划

#### China Fork
我们会在国内建 Remix 项目的镜像站，包括 IDE、文档、官网。还有 Solidity 的 js 编译器镜像站。

但即使建了镜像站，还是有可能会受墙的影响。特别是 Remix IDE 有些静态文件是直接通过链接的形式引入的。这其中就有 google、github 的链接。一旦这些静态文件被墙，Remix IDE 就无法正常使用。

所以我们会开发且维护一个国内的分支，把这些静态文件的链接换成国内的链接。这个分支不会提 PR 给 Remix 的 master 分支，只会不断地将 master 分支合并到这个分支。

---
layout: default
---

# 开发计划

#### 助推国际化
对国际化的支持本来就在 Remix 团队的开发计划之内的。但因为优先级比较低，这个功能是一拖再拖。

https://github.com/ethereum/remix-project/issues/50

这个功能早在2020年就提出了，但直到2022年才开发出来。而实现这个功能的 PR 就是 Remix China 贡献的。

我估计，就算我们什么都不做，Remix 团队也迟早会实现国际化。但具体什么时候就不好说了。

而 Remix China 项目很多地方需要依赖这个国际化。特别是前面提到的翻译计划，如果要对 Remix IDE 操作界面的文案进行翻译，那前提就是这些文案本身要支持多语言切换。所以我们打算助推一把，帮助 Remix 项目尽快实现国际化支持。
---
layout: default
---

# 运营计划

#### 自媒体
Remix 团队有三个自媒体
- Twitter: https://twitter.com/EthereumRemix
- Medium: https://medium.com/remix-ide
- YouTube: https://www.youtube.com/channel/UCjTUPyFEr2xDGN6Cg8nKDaA

我们已经建了一个微信公众号，后续会把 Remix 团队在自媒体上发布的内容都同步到这个公众号上。我们也会发布一些原创的内容
---
layout: default
---

# 运营计划

#### 交流群
Remix 项目的交流群在 Gitter 上，同样是被墙的。我们会建一个微信群作为国内 Remix 用户的交流群。这个交流群的作用就是把国内的 Remix 用户聚到一起，互相帮助，解决在使用 Remix 的过程中碰到的一些问题。


---
layout: default
---

# 研究计划
研究计划是未来打算做的事。基本上都是一些需要先投入大量的时间做技术调研，然后才能明确具体要怎么做的事。
#### WebContainer
简单来说就是，WebContainer 就是⼀个可以运⾏在浏览器⻚⾯中的微型操作系统。如果 Remix IDE 能结合这项技术，那整个使⽤体验能再上升⼀个 level 。

⽬前国内智能合约 IDE 领域做得最好的就是纯⽩矩阵的 ChainIDE 。我⽤过 ChainIDE，使⽤体验完全不如 Remix 。但是 ChainIDE 有⼀个 Remix 没有的优点，就是可以提供 linux 环境，这样在 ChainIDE 上就可以⽤ truffle、hardhat、ganache 了。不过 ChainIDE 的实现⽅案⾮常笨重，是在服务器上起⼀个 linux 虚拟机，然后通过 websocket 跟前端通信。这种中⼼化的⽅案成本很⾼的，⽤户量稍微⼤⼀点，服务器估计就扛不住了。

如果 Remix 能结合 WebContainer 的话，我估计能把 ChainIDE 秒成渣渣。

---
layout: default
---

# 研究计划
#### VSCODE
这个改进估计工作量会比较大，而且如果真要做的话就需要维护网页版和桌面版两个版本了。我感觉是有点划不来。针对桌面版IDE，其实我有一套更好的开发方案。就是把Remix IDE 上的功能通过插件的形式移植到VSCODE上。这样就不需要去关心怎么集成terminal了，因为VSCODE本身就集成了terminal。我们只需要关心哪些功能是Remix IDE上有的，但是VSCODE没有的，把这些功能给搬过来就好了。而且VSCODE也有网页版，而且网页版还可以集成github codespaces，这样云端开发环境也搞定了。而且后面如果我们想集成chatgpt来写合约，在VSCODE上也会容易很多。我感觉这个方案甚至比Remix IDE还要好，没有弱点

#### 数字人民币

---
layout: end
---

