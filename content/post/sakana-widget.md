---
title: "在hugo的主题中添加石蒜模拟器🐟「Sakana! Widget」"
author: Refrain
date: 2022-09-17T10:28:29+08:00
draft: true.
categories:
- blog
---

<style>table {border: 1px;}</style>
<table><tr>
<td><img src="https://raw.githubusercontent.com/dsrkafuu/sakana-widget/main/src/characters/chisato.png"></td>
<td><img src="https://raw.githubusercontent.com/dsrkafuu/sakana-widget/main/src/characters/takina.png"></td>
</tr></table>


我们采用 [dsrkafuu/sakana-widget](https://github.com/dsrkafuu/sakana-widget)

首先需要引入模块，可以使用 CDN 直接引入

``` html
<!-- https://cdn.jsdelivr.net/npm/sakana-widget@2.3.2/lib/sakana.min.js -->
<!-- https://cdnjs.cloudflare.com/ajax/libs/sakana-widget/2.3.2/sakana.min.js -->
<div id="sakana-widget"></div>
<script>
  function initSakanaWidget() {
    new SakanaWidget().mount('#sakana-widget');
  }
</script>
<script
  async
  onload="initSakanaWidget()"
  src="https://cdn.jsdelivr.net/npm/sakana-widget@2.3.2/lib/sakana.min.js"
></script>
```

我们需要将其写在hugo主题的模板中。例如我采用的hugo-tania主题，想要添加在页面下方，在
> themes/hugo-tania/layouts/partials/footer/custom.html

中粘贴。可以看到 sakana-widget 组件出现在页面的最下方。

但是我想要让其固定在网页窗口右下角，可以直接修改

```html
<div id="sakana-widget" 
style="position:fixed;bottom:10px;right:10px;">
</div>
```
