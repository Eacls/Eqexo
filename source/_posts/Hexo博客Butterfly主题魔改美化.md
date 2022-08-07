---
categories:
- 实用教程
comments: null
cover: https://preview.cloud.189.cn/image/imageAction?param=D46AAD69B808AEECA37C93A0EB7E1E52FC04A29912945EC7D849F8E14F9D473E03AF9B6E1EFF847419D35F747182A11A6395347B1B3EA69E162CCCBD0FC2FED3C68721F2E7A6996BB3E7C41AD7C99D647A443D026BB41130FFE8ECA1357051B5C97552A0402CF3781D31333B2520ACD2
date: 2022-1-11
description: 关于本站魔改美化相关教程
tags:
- Hexo
title: Hexo博客Butterfly主题魔改美化
top_img: https://preview.cloud.189.cn/image/imageAction?param=02752F480DE3A48DEAC3B84474EE6A7E91F2EB7096FE3CFB5031FDC056FDCE95B0B560538E0DCB9DAD42A71C219139B787A37FFB8C60EBFA98919414B62F5F36F1F3685FAC9C1DCF49D2CE751B24C75184A6B13D6929656F819BFC427F0DB54DD1C88F0B693DA221EDDC6EBB8AB0E661
updated: 2022-1-12
---
## 前言

在2021年末，我想搭建一个博客网站，无意间接触了Hexo这样实用的静态博客框架，找到了Butterfly这样好看的主题。因而开始花大把时间去研究。时至今日，在与各位大佬携手共进的过程中，打造出了一个优雅的个人博客网站。

> 本篇教程基于Butterfly主题3.8.3版本

---

## 隐藏首页图

{% tabs test4 %}

<!-- tab 预览 -->

**![](https://preview.cloud.189.cn/image/imageAction?param=DD2371F9521AFDA4CEB1D8293DCD7A4896E210E877CDD6642CC9984DA34E025511B2BC05C1008FF73DC8EDB20192C96F5F8E7179BD2DD54500F7FDC29903B1EC37343D9C136B2A77B430B9BF65D19FFA763B4739518A259FB40134028C859EBF869884CCD4FC6FF338E2832314DEFF5D)**

<!-- endtab -->

<!-- tab 源码 -->

主题配置文件内

```
# The banner image of home page
index_img: false
```

<!-- endtab -->

{% endtabs %}

## 全局背景

{% tabs test4 %}

<!-- tab 预览 -->

**![](https://preview.cloud.189.cn/image/imageAction?param=A009DAEC9B7B19260D0609C97C7E3E33847B222F1E2FBDC589A0E8FA6C77C354F8352E64885CFA29F01F220E769C31797E19AC7E4974FDA8CFCEAE1AA0CC8843A050E2FBC2FA11C199175B1761B25B38A7B78AE6D7FB33AB6E82FC668A3143C5D0B13EEE3F380C19DEDAEB6100335B6B)**

<!-- endtab -->

<!-- tab 源码 -->

你可以选择在主题配置文件内更改背景图片的url

```
# The formal of image: url(http://xxxxxx.com/xxx.jpg)
background: url( )
```

也可以选择通过引入css更改

本站渐变背景css↓

```
#web_bg {
    background: linear-gradient(180deg,#fff1eb,#ace0f9)
}
```

<!-- endtab -->

{% endtabs %}

## 引入css/js

在<u>博客根目录/themes/butterfly/source/css</u>下新建一个xxxxxx.css 或者在<u>博客根目录/themes/butterfly/source/js</u>下新建一个 xxxxxx.js 文件。 <kbd>Ctrl</kbd>+<kbd>C</kbd>和 <kbd>Ctrl</kbd>+<kbd>V</kbd> 填入内容。

修改主题配置文件 **_config.butterfly.yml**

```
inject:
  head:
    - <link rel="stylesheet" href="xxxxxx.css">
  bottom:
    - <script src="xxxxxx.js"></script>
```

其中head引入css，bottom引入js

## 顶部磁吸分类

{% tabs test4 %}

<!-- tab 预览 -->

**![](https://preview.cloud.189.cn/image/imageAction?param=840DE20FF363FEFBBDC1FF33CF8FE36C3E866ABB4486251B71BEC0041912A51F48015E6A0FB16E7B9910A7E064E9B7AA1CC59B0BBAF454E12659BB249F0B1CB51BF35ADDB5130DE4B000C2CCBBE73321A47442CDAAA44B8263EC47D8F1035BC81F383E7C9FF61FE4A6A8CC2B2F9E8079)**

<!-- endtab -->

<!-- tab 教程 -->

安装

```
npm i hexo-magnet --save
```

详细
[小冰教程贴](https://zfe.space/post/hexo-magnet.html)

<!-- endtab -->

{% endtabs %}

## 侧边栏时钟

{% tabs test4 %}

<!-- tab 预览 -->

**![](https://preview.cloud.189.cn/image/imageAction?param=9854437BEC4192A409989A60257D4389C1698EDC83B6C26387D93626B19A5AFA4216907252D6D96FE755E3B699AFD981DA2324EA6B9349C4A2D6A90D801820B38485523D89DE7EA84A5C5BEFC3B3084A5A8032D30FBED298F1687AE53604DB8AA04DD32579B381220B304B97BD617538)**

<!-- endtab -->

<!-- tab 教程 -->

安装

```
npm i hexo-electric-clock --save
```

详细
[小冰教程贴](https://zfe.space/post/hexo-electric-clock.html)

<!-- endtab -->

{% endtabs %}

## 页脚

{% tabs test4 %}

<!-- tab 预览 -->

**![](https://preview.cloud.189.cn/image/imageAction?param=5894DC402C957A31C2170ABF10217A902DD5A8ECAB47988EF46CA987A9AABF9AFE3F2C1EE348ECC6254D129A7D45B14B7505E1B08B576F7F05634F5D228DFE6E52B7741A3842737F4C3C3B0F7BEE334D84DE7B53E3C617249A104075EFE9D14134E5958B2485B075123C094B7BDA474D)**

<!-- endtab -->

<!-- tab 源码 -->

```
# Footer Background
footer_bg: # true
```

如果写为true，则会根据当前页面的top_img变化；如果写图片链接，则会呈现图片；如果写的不符合语法，则会呈现主题色。

<!-- endtab -->

{% endtabs %}

## 个人信息栏按钮圆角

{% tabs test4 %}

<!-- tab 预览 -->

**![](https://preview.cloud.189.cn/image/imageAction?param=11D8B95E129A506B2806548554E585C203FEDB6FC79FD508792B19BCFED8D8F59E3F316E1C833005119749350AD22117DA4EBF5E7155F3B4F609DD2DC011398400392A33ECF49EBBC81981B9104BFC491DA40828CA5214D57B82668EAA0DBE6AE0AB0F5E2C65062B21524AB5BE6BAA98)**

<!-- endtab -->

<!-- tab 源码 -->

```
/*GitHub开源圆角*/
#card-info-btn {
  border-radius: 7px;
  overflow: hidden;
}
```

<kbd>Ctrl</kbd>+<kbd>C</kbd>和 <kbd>Ctrl</kbd>+<kbd>V</kbd> 填入之前新建的css文件内。

<!-- endtab -->

{% endtabs %}

## 侧边小按钮

{% tabs test4 %}

<!-- tab 预览 -->

**![](https://preview.cloud.189.cn/image/imageAction?param=421154E1234EDCC087755EAC4BA90FA4331BD684D0C0C6617F615D8030A687320B6687375242EE0B8FAE7F7A1246B892B7A1511DB31465B6619C771F8B6C541820F1F0E0A01EB540B78AF997000D6E546F110EC924C7EF9DC6E39A0564A03786BE0536CDF381AF182C48DE7F40F36684)**

<!-- endtab -->

<!-- tab 源码 -->

```
/* 右侧小按钮圆角 */
#rightside>div>button,#to_comment {
    margin-right: 4px;
    border-radius: 7px;
  }

/*侧边滑动颜色*/
:root {
    --btn-bg: #3a87b9;
}
```

<kbd>Ctrl</kbd>+<kbd>C</kbd>和 <kbd>Ctrl</kbd>+<kbd>V</kbd> 填入之前新建的css文件内。

<!-- endtab -->

{% endtabs %}

## 底部切换页面按钮

{% tabs test4 %}

<!-- tab 预览 -->

**![](https://preview.cloud.189.cn/image/imageAction?param=6AEADE8A5E67FFFA52CE4B504E7EC02D89380D41778853A3931CB96013D599B19642AE2459BEA656516B101CBA2E4D2C208DD04ED84EFB2B992F63F7070E91823F26FD04725AACCA6720D48ABE0E5EC4BB5E3475D7690D7E49F3E9642959ECD6C57CCEBDF8EB84B0FD7256562A623C65)**

<!-- endtab -->

<!-- tab 源码 -->

```
/*底部切换按钮*/
.layout>.recent-posts .pagination>* {
  display: inline-block;
  margin: 0 6px;
  width: 2.5em;
  height: 2.5em;
  line-height: 2.5em;
}

/*底部圆角*/
#pagination .page-number.current {
    border-radius: 7px;
}
```

<kbd>Ctrl</kbd>+<kbd>C</kbd>和 <kbd>Ctrl</kbd>+<kbd>V</kbd> 填入之前新建的css文件内。

<!-- endtab -->

{% endtabs %}

## 首页文章卡片高度

{% tabs test4 %}

<!-- tab 预览 -->

**![](https://preview.cloud.189.cn/image/imageAction?param=B97843482931DC981E3DABDC3D4C2B1ABB32C0230B6CB31AD9BC400E80423EFBB2BF1A73506F5A02848D6E2380544133396E1EA671BD3F9F4F1B930EC2969F2C764659CD6AC60B64F0B42994D605694314654F1D61FD24E434B3290E797A205D63FFDE2223E542761830FAB717367381)**

<!-- endtab -->

<!-- tab 源码 -->

```
#recent-posts > .recent-post-item {
     height: 20em;
}
```

其中更改“20”，数字越高，卡片越高。

<kbd>Ctrl</kbd>+<kbd>C</kbd>和 <kbd>Ctrl</kbd>+<kbd>V</kbd> 填入之前新建的css文件内。

<!-- endtab -->

{% endtabs %}

## 简洁侧边栏

{% tabs test4 %}

<!-- tab 预览 -->

**![](https://preview.cloud.189.cn/image/imageAction?param=62E96A6DD4292F9C9B06725AA83158EEEBED5099239DC68D412E42492443BC0BF779118EB84FF4BBB5EFE8C56503E4511DCC0D656C4D243340F278EB455ED400C75C2C5F2D94A7CA85A4195F530CE7C33D837CF08B08C105D1AF03AAC226B146EA9B6D474EF63B129453E3CD0F08EA0B)**

<!-- endtab -->

<!-- tab 源码 -->

主题配置文件内

```
# toc (目錄)
toc:
  enable: true
  number: true
  style_simple: true
```

<!-- endtab -->

{% endtabs %}

## 更改网站logo

{% tabs test4 %}

<!-- tab 预览 -->

**![](https://preview.cloud.189.cn/image/imageAction?param=033B9568AB7169DF27EB635124891EBF470034A629FE1E097ABD2C4049CDBB2AE71BF5B5C0E1FCA4B7410F69E7FC85716444B1A58058E36C9D59601AEEEA4D855F26ECFDB1817B65EDBEB12B2710B772206BBDBF9CDF845A233DD4861B0FCEA0357A2DE4ECFE023187505F25BEA160D8)**

<!-- endtab -->

<!-- tab 方法 -->

在<u>博客根目录/themes/butterfly/source/img</u>中更换**favicon.png**;404图片同理。在更换logo图片时建议使用PS调整为32×32并添加圆角。

<!-- endtab -->

{% endtabs %}

## 网站速度优化

### 压缩图片

[压缩图片，减少负载](https://tinypng.com/)

### 异步加载

当css/js过多时，会拖慢网站加载速度，这时可以使用异步加载进行整合优化。
[糖果屋教程](https://akilar.top/posts/615d5ede/)

## 特别鸣谢

<!-- 大佬们 -->

- [Akilar糖果屋](https://akilar.top/)
- [CC康纳百川](https://blog.ccknbc.cc/)
- [小冰博客](https://zfe.space/)
- [小嘉部落格](https://blog.imzjw.cn/)
- [Gahotx's blog](https://gahotx.cn/)
