#[[excerpt]] [简悦 + Logseq + Github Page 无代码全自动化知识管理发布方案](https://zhuanlan.zhihu.com/p/467192292) 
- tags: #[[SimpRead]] 
- read date: [[2022_04_04  ]]
- desc: 在简悦标注，自动生成符合 Logseq 的标注文件，然后发布到 Github Page 的无代码化全自动方案。感谢 @tiensonqin 提供了这么棒的双链笔记 Logseq，得益于 @pengx17 发布的 Logseq Publish GitHub Action，可以非常…
- [ ](<http://localhost:7026/pdf/简悦 + Logseq + Github Page 无代码全自动化知识管理发布方案#id=1649017643548>)  ### Hazel

自动化方案选择是 Hazel 这个监控文件夹变化而进行一系列自动化操作的 Mac App，如果你是 Windows 用户可以使用 [Dropit](https://link.zhihu.com/?target=http%3A//www.dropitproject.com/)。

（对上图）简单的说明

*   除了监控 `page` 文件夹外也可以是其它文件夹 e.g. `journals` `logseq` `assets` 甚至于监控根目录的 `README.md`（当此文件改动时再提交)。
*   为了降低执行的频率，文件改动一分钟后再执行，这里的数字可以改为任意值。
*   Shell 代码很简单，就是 Push 到 Github

```
  cd /<your path>/knowledge-garden
  git add .
  git commit -m "auto save:Update some logseq pages."
  git push origin maincrontab
```

- [ ](<http://localhost:7026/pdf/简悦 + Logseq + Github Page 无代码全自动化知识管理发布方案#id=1649017643592>)  ![](https://pic2.zhimg.com/v2-583332f7f65cadc287d859ecac0e4a6d_r.jpg)

