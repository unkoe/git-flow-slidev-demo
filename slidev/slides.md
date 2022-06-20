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
---

# Git 工作流 

选择和使用

<div class="pt-12">
  <span @click="$slidev.nav.next" class="px-2 py-1 rounded cursor-pointer" hover="bg-white bg-opacity-10">
    按空格进行翻页 <carbon:arrow-right class="inline"/>
  </span>
</div>

<div class="abs-br m-6 flex gap-2">
  <button @click="$slidev.nav.openInEditor()" title="Open in Editor" class="text-xl icon-btn opacity-50 !border-none !hover:text-white">
    <carbon:edit />
  </button>
  <a href="https://github.com/slidevjs/slidev" target="_blank" alt="GitHub"
    class="text-xl icon-btn opacity-50 !border-none !hover:text-white">
    <carbon-logo-github />
  </a>
</div>

<!--
The last comment block of each slide will be treated as slide notes. It will be visible and editable in Presenter Mode along with the slide. [Read more in the docs](https://sli.dev/guide/syntax.html#notes)
-->

---

# 什么是Git工作流?

Git 作为一个源码管理系统，不可避免涉及到多人协作。

协作必须有一个规范的工作流程，让大家有效地合作，使得项目井井有条地发展下去。"工作流程"在英语里，叫做"workflow"或者"flow"，原意是水流，比喻项目像水流那样，顺畅、自然地向前流动，不会发生冲击、对撞、甚至漩涡。

![git flow](https://www.ruanyifeng.com/blogimg/asset/2015/bg2015122301.png)


<br>
<br>
<br>


相关的博客： [Git工作流程](https://www.ruanyifeng.com/blog/2015/12/git-workflow.html)


<!--
You can have `style` tag in markdown to override the style for the current page.
Learn more: https://sli.dev/guide/syntax#embedded-styles
-->

<style>
h1 {
  background-color: #2B90B6;
  background-image: linear-gradient(45deg, #4EC5D4 10%, #146b8c 20%);
  background-size: 100%;
  -webkit-background-clip: text;
  -moz-background-clip: text;
  -webkit-text-fill-color: transparent;
  -moz-text-fill-color: transparent;
}
</style>

<!--
# Git 工作流
-->

---

# Gitflow 介绍

最早诞生、并得到广泛采用的一种工作流程，就是Git flow 。

### 两个长期分支。

- 主分支master
- 开发分支develop

前者用于存放对外发布的版本，任何时候在这个分支拿到的，都是稳定的分布版；后者用于日常开发，存放最新的开发版。

### 三种临时分支。

- 功能分支（feature branch）
- 补丁分支（hotfix branch）
- 预发分支（release branch）

一旦完成开发，它们就会被合并进develop或master，然后被删除。


---

# 分支模型

<img src='https://nvie.com/img/git-model@2x.png'>

Git flow 的详细介绍:
- [一个成功的 Git 分支模型](https://nvie.com/posts/a-successful-git-branching-model/)
- [中文版《Git 分支管理策略》](https://www.ruanyifeng.com/blog/2012/07/git.html)

<style>

img {
  width: 30%;
  height: 70% 
}
</style>

---

# 模型讨论

1. 我们的开发状态是否需要进行版本管理？
2. Git flow 模型是否适用于我们？
3. 判断削减模型。例如取消 release 和 hotfix 分支，事实上结合开发模式和工具对此考虑。
4. [git flow 插件](https://github.com/arslanbilal/git-cheat-sheet/blob/master/other-sheets/git-cheat-sheet-zh.md)
![git flow](https://github.com/arslanbilal/git-cheat-sheet/raw/master/Img/git-flow-commands.png)


---

# Gitflow 命令视图
<img src="https://github.com/arslanbilal/git-cheat-sheet/raw/master/Img/git-flow-commands-without-flow.png">

[git-flow](https://www.atlassian.com/git/tutorials/comparing-workflows/gitflow-workflow)

<style>

img {
  width: 80%;
  height: 80% 
}
</style>
---

# 三种 Git 工作流 

**Gitflow** 诞生后，因为时代和开发模式的变化又出现了其它的 Git 工作流程。

Vincent Driessen 也提到了他创造的这个Git开发模型面对持续交互的挑战。

目前主流的工作流有三种。

- Git flow
- Github flow
- Gitlab flow

Gitflow是被使用的最多的开发模型，而 Github flow 和 Gitlab flow 则对 Gitflow 的模型进行了简化和调整。

[三种工作流的介绍](https://www.ruanyifeng.com/blog/2015/12/git-workflow.html)

---

# Github flow

- 创建一个新分支
- 进行更改并添加提交
- 打开拉取请求
- 审查
- 部署
- 合并

<img src="https://pic3.zhimg.com/80/v2-bafaef976e8842a50403d61912239b52_1440w.jpg">

<style>
img {
  width: 70%;
  height: 50%;
}
</style>

---

# Gitlab flow

![gitlab flow](https://camo.qiitausercontent.com/0845268343ff051296a5677ff0ac0a22afac168b/68747470733a2f2f71696974612d696d6167652d73746f72652e73332e616d617a6f6e6177732e636f6d2f302f3138353338392f36386235613237622d653332622d643631662d363032302d3936646533626131643333352e706e67)

<style>
img {
  width: 30%;
  height: 30%; 
}
</style>
