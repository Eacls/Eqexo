---
abbrlink: ''
categories:
- - 实用教程
cover: https://preview.cloud.189.cn/image/imageAction?param=DC5FBB0A6C586B6EA0E86847DB8EDE8F9D85ACC87C25E9A0D4EC661B11A1A28AEABCD1BDA9F95C3E5D4E099D0C0AA815EA8422A6624E1EC4022BCE0892405C2F7869CFFF5A0BC77B5E9E13F88FB00EEC115B851F11EAC95C8AC26B3142710B6C4048961363594CCF6C4D74B640EFAE95
date: '2022-11-30 19:13:16'
description: 打造你的简洁博客
tags:
- Hexo
title: Butterfly主题魔改美化-叁
top_img: https://preview.cloud.189.cn/image/imageAction?param=00DB5C3C49A26FC88A3EA42581FD8EB39E280FE49620B799146A85DD61A8B5B9BE8616765F728A1B3ACA58CB327C6196C10BAE952E906FD7E07FEA119B1EC3244B1145C310DBEBCACFCFB2116C1C35B935461A528BBE27EA8F3C7AE1332AA25CDB673C13124E3B9C29A0A4DB0ADBC57C
updated: '2022-11-30 19:13:17'
---
## 前言

在过去建立博客的一年之间，我一共撰写了三篇Butterfly主题的美化教程，总共分为两大版本。期间我始终秉持着简洁的原则（~~技术限制~~）出了一些很小白向的教程。虽然今天的这一篇教程也都是比较简单的外挂css方式，但我认为教程 ``叁``即博客 ``3.0``已经属于比较成熟的版本了，虽然在以后可能改变我这个想法。
感谢 [Heo](https://blog.zhheo.com)、[Leonus](https://blog.leonus.cn) 所提供的样式参考以及部分源代码。

{% note info flat %}
本篇教程基于Butterfly主题4.5.1版本。
{% endnote %}

{% note info flat %}
如果你想全局应用本站样式，可以F12自行获取 ``eacls.css``以及 ``eacls2.css``。
{% endnote %}

---

## 个人信息卡片

{% tabs test4 %}

<!-- tab 预览 -->

<img src="https://preview.cloud.189.cn/image/imageAction?param=5C5234B6BB7DB3BE31801096F035CD0D8A09CABBA2F2F21CCECE45D54422995A738A0D85F20B0454030C18A07B1630F9206E636ADD8B5330F95DA003B93C6FEF6654A9EE7D454D58706575D7E537B3AFEACC50C49B4D73784BBAB27A251419DECBF4BC57228444CFAE092226EF79A8B5" width="25%" height="25%" />

<!-- endtab -->

<!-- tab 源码 -->

```CSS
/*个人信息美化*/
#aside-content>.card-widget.card-info {
  background: #fff url(https://www.eacls.top/img/info.webp) top 33% center no-repeat;
  position: relative;
}
#aside-content .card-info #card-info-btn {
  display: none;
}
#aside-content .card-info .author-info__name {
  font-weight: 700;
  color: black;
}
#aside-content .card-info .author-info__description {
  font-weight: 600;
  color: black;
}
.site-data > a .headline {
  color: rgb(0 0 0 / 100%);
}
```

<!-- endtab -->

{% endtabs %}

## 文章目录

{% tabs test4 %}

<!-- tab 预览 -->

<img src="https://preview.cloud.189.cn/image/imageAction?param=E0702E8E8360494D16DD0F483FEC49DC690DE5416ACC6657B5D89D1FC9871A21399027B482C3D78EF435BA541CD80C60892405715411B74E99CA79EDD554E05BF9BD5168F23A1FDF3775745341ED22440758C8EE621B15AE3D066F17A554ECF6D00D0E67F4924A641BF0A756E5E5090A" width="25%" height="25%" />

<!-- endtab -->

<!-- tab 源码 -->

```CSS
/* 文章目录 */
 #aside-content #card-toc .toc-content {
  margin: 10px -18px;
}
 #aside-content #card-toc .toc-content .toc-link.active {
  line-height: 1.2;
  border-radius: 12px;
  border-left-color: var(--heo-hovertext);
  background-color: var(--heo-card-bg);
  color: var(--heo-lighttext);
  font-weight: bold;
  font-size: 20px;
}
[data-theme=dark].toc .toc-item.active .toc-link .toc-text {
  color: var(--heo-white);
}
#aside-content #card-toc .toc-content .toc-item.active .toc-link {
  opacity: 1;
  border-radius: 8px;
}
#aside-content #card-toc .toc-content .toc-link {
  line-height: 1.2;
  padding: 8px;
  border-left: 0px solid transparent;
  border-radius: 12px;
  color: var(--heo-secondtext);
  cursor: default;
}
#aside-content #card-toc .toc-content .toc-link:not(.active) span {
  opacity: 0.6;
  cursor: pointer;
  filter: blur(1px);
  transition: 0.3s;
}
#aside-content #card-toc:hover .toc-content .toc-link:not(.active) span {
  filter: blur(0px);
  opacity: 1;
}
#aside-content #card-toc .toc-content .toc-link:not(.active) span:hover {
  color: var(--heo-lighttext);
}
```

<!-- endtab -->

{% endtabs %}

## 文章顶部信息栏

{% tabs test4 %}

<!-- tab 预览 -->

<img src="https://preview.cloud.189.cn/image/imageAction?param=92D404CB68C885A8A07762C1664BE1E0BE068DB40DE5AB06A657AE4270043B39ABBDA3C0527133D453B0ACAC3A7FFDA3BF1B6C8868D9F691FF2D1B9565E20D4E553703FF02573DCE67B95053B76E6194DD4273E494160C1E848B8A4466DE3A0318B068BA9745584069B2185F899873E4" width="50%" height="50%" />

<!-- endtab -->

<!-- tab 源码 -->

```CSS
/* 文章标题 */
#post-info .post-title {
  color: var(white);
  font-weight: 700;
  font-size: 2.6rem;
  line-height: 1.2;
  text-align: center;
  margin: 1rem 0 1rem 0 !important;
  -webkit-line-clamp: 2;
  padding: 0;
}

@media screen and (max-width: 768px) {
  #post-info .post-title {
    font-size: 1.6rem;
    -webkit-line-clamp: 3;
    margin: 0.2rem auto !important;
    text-align: center;
    z-index: 1;
  }
}

/*信息栏底部圆角*/
#page-header.post-bg:before {
  background-color: rgb(0 0 0 / 60%);
  border-bottom-right-radius: 11px;
  border-bottom-left-radius: 11px;
}

#page-header.post-bg {
  border-bottom-right-radius: 11px;
  border-bottom-left-radius: 11px;
}

/* 文章顶部其他信息 */
#post-meta>div {
  text-align: center;
  color:white
}
/* 隐藏信息文字 */
#post-info #post-meta .post-meta-label {
  display: none;
}
/* 图标数字间距 */
#post-info #post-meta .post-meta-icon {
  margin-right: 0.3rem;
}
/* 每组间距 */
#post-info #post-meta .post-meta-separator {
  margin: 0px 0.4rem;
}
```

<!-- endtab -->

{% endtabs %}

## 版权信息

{% tabs test4 %}

<!-- tab 预览 -->

<img src="https://preview.cloud.189.cn/image/imageAction?param=85742AD4D80E1EFBE67892F86D48F3CAF7FBBFC2DFAAE275955E371DEE3F7CD4F57C70B2A2D2472CAB734257F7090490FBAB3C8D4CE2C609DA51E1D4DDB12B9CE6583D14F5B91F969DFA102D76874426F4CF79DB853B3ADA00D1E23D372DAC7D597AFCD45A75048ABA5E28A291687AB8" width="50%" height="50%" />

<!-- endtab -->

<!-- tab 源码 -->

```CSS
/* 版权信息 */
/* 背景 */
#post .post-copyright {
  background: var(--heo-card-bg);
  padding: 2rem 1.3rem;
  overflow: hidden;
  border: var(--style-border);
  border-width: 1px;
  transition: 0.3s;
  border-radius: 11px;
}

#post .post-copyright:after {
  position: absolute;
  right: 22px;
  top: -77px;
  content: '\f25e';
  font-size: 180px;
  font-family: 'Font Awesome 5 Brands';
  color: var(--heo-fontcolor);
  opacity: 0.4;
  filter: blur(7px);
}

@media screen and (max-width: 768px) {
  #post .post-copyright {
    padding: 1rem 1.3rem;
  }
}

.post-copyright__author {
  display: flex;
  align-items: center;
}

.post-copyright__original {
  background: var(--heo-fontcolor);
  color: var(--heo-card-bg);
  padding: 0.2rem 0.5rem;
  font-size: 0.7rem;
  border-radius: 8px;
  margin-right: 0.5rem;
  font-weight: bold;
  line-height: 1.5;
  white-space: nowrap;
}

.post-copyright__original:hover {
  background: var(--heo-main);
  color: var(--heo-white);
}

@media screen and (max-width: 768px) {
  #post .post-copyright {
    box-shadow: var(--heo-shadow-border);
  }

  .post-copyright .post-meta-original {
    display: none;
  }

  .post-copyright__original {
    display: none;
  }

  #post .post-copyright:after {
    display: none;
  }
}


/* 作者名 */
#post .post-copyright .post-copyright-info a {
  padding: 0;
  color: var(--heo-fontcolor);
  font-weight: bold;
}

#post .post-copyright .post-copyright__notice .post-copyright-info a {
  padding: 0 4px;
}

#post .post-copyright .post-copyright-info a:hover {
  color: var(--heo-lighttext);
}

#post .post-copyright .post-copyright-info {
  padding-left: 0;
  color: var(--heo-fontcolor);
  overflow: hidden;
  display: -webkit-box;
  -webkit-line-clamp: 1;
  -webkit-box-orient: vertical;
}

#post .post-copyright .post-copyright-title {
  padding-left: 0;
  color: var(--heo-fontcolor);
  overflow: hidden;
  display: -webkit-box;
  -webkit-line-clamp: 1;
  -webkit-box-orient: vertical;
  font-size: 1rem;
  font-weight: bold;
}

#post .post-copyright .post-copyright-title:hover {
  color: var(--heo-lighttext);
}

#post>div.post-copyright>div.post-copyright__author>span>span {
  padding: 0;
  color: var(--heo-fontcolor);
  font-weight: bold;
  font-size: 1rem;
  line-height: 1.38;
  overflow: hidden;
  display: -webkit-box;
  -webkit-line-clamp: 1;
  -webkit-box-orient: vertical;
}

@media screen and (max-width: 768px) {
  #post>div.post-copyright>div.post-copyright__author>span>span {
    -webkit-line-clamp: 3;
  }

  #post .post-copyright .post-copyright-info {
    -webkit-line-clamp: 2;
  }

  #post .post-copyright .post-copyright-title {
    -webkit-line-clamp: 3;
    line-height: 1.2;
  }
}

/* 链接 */
#post>div.post-copyright>div.post-copyright__type {
  line-height: 16px;
  display: flex;
  margin-top: 8px;
}

#post>div.post-copyright>div.post-copyright__type>span>a {
  font-size: 14px;
  opacity: 0.6;
  line-height: 16px;
}

#post>div.post-copyright>div.post-copyright__type>span>a:hover {
  opacity: 1;
  background: none;
}

#post-copyright-url a {
  overflow: hidden;
  display: -webkit-box;
  -webkit-line-clamp: 1;
  -webkit-box-orient: vertical;
}
/* 提示 */
#post>div.post-copyright>div.post-copyright__notice {
  font-size: 0.7rem;
  line-height: 1rem;
  margin: 0.5rem 0;
}
/*装饰圈*/
#post .post-copyright:before {
  display: none;
}

#post .post-copyright .post-copyright-meta {
    color: #5a7ed7;
    font-weight: bold;
}
#post .post-copyright {
    padding: 2rem 1.3rem;
    border-radius: 11px;
    border-style: solid;
}
```

<!-- endtab -->

{% endtabs %}

## 右下角按钮

{% tabs test4 %}

<!-- tab 预览 -->

<img src="https://preview.cloud.189.cn/image/imageAction?param=CA9ACA8F14F2F0D9984BB4BBEE96C9521BB2FD450D0F4CE19189BDD958E5597781FA8A5B3E371D2DD9AC2C4AFA95FAE71FB5E732C421EA7FD326E577D4887958DBB45BAA43268C84CA122EF649CEA43F028DD788C1087A61FCF68B450DE08DC67414EB40B45CE48E05F1FFED73A19AC4" width="25%" height="25%" />

<!-- endtab -->

<!-- tab 源码 -->

```CSS
/*右下角按钮*/
#rightside > div > button, #rightside > div > a {
  display: block;
  margin-bottom: 6px;
  width: 40px;
  height: 40px;
  border-radius: 25px;
  background-color: #f1f1f1;
  color: #2d587a;
  text-align: center;
  font-size: 16px;
  line-height: 40px;
}
```

<!-- endtab -->

{% endtabs %}

## 评论内容背景

{% tabs test4 %}

<!-- tab 预览 -->

<img src="https://preview.cloud.189.cn/image/imageAction?param=06D1CB5101B1B5BF029B35BCF7BF4644B9882BCD9F48883D47070A6CF5D209B0CBB8CA93E5A0077BB742E0FD39064B9867116657FA843747BB759626149605EE2403D82136567E922123F1994B1BFCD88E5B2763B1DD7FFD8A9E2C9A956045A48D048FD0FAC8D98867CB3FEB87CB757C" width="50%" height="50%" />

<!-- endtab -->

<!-- tab 源码 -->

```CSS
/*评论背景*/
#twikoo .tk-content {
  background: rgb(213 213 213 / 60%);
  padding: 10px 15px;
  border-radius: 7px;
}
```

<!-- endtab -->

{% endtabs %}

## 本地搜索框

{% tabs test4 %}

<!-- tab 预览 -->

<img src="https://preview.cloud.189.cn/image/imageAction?param=F2612C5D3D0E588EE6F36291D99C72A10213C7761ACE0D061F58DF93A9318D222631AC1EB8831898F6CFACFF9D15218A2C55BFC94FDECB3895511DBB3081912B54E64C503A94BAD93F81249BDA5E74CB9B33D907E91539F211ED2AADAFD8CAB86A69A9EDADB4AD1AFEEDC9721179239B" width="50%" height="50%" />

<!-- endtab -->

<!-- tab 源码 -->

```CSS
/*本地搜索美化*/
.search-dialog .search-nav {
    color: #000000;
    font-size: 1.6em;
    line-height: 2;
}
#local-search .search-dialog .local-search-box input {
  padding: 13px 21px;
  border: 3px solid #4182d9;
  border-radius: 11px;
}
hr {
  border: 3px dashed #4f80d8;
}
```

<!-- endtab -->

{% endtabs %}

## 友链界面

{% tabs test4 %}

<!-- tab 预览 -->

<img src="https://preview.cloud.189.cn/image/imageAction?param=C468AC3C95265C74E896FE3096395483A75A6727EB694079EE7B645DFBEAD6177DA0A18254B3CDCAD42D59AA8977C19AAEA8C2DBA6F204BA207F480B21EDAD14E3831902BDFFEF3406E6FA4142C9B631D5A55D1495D3F38E16A0B903716230FC890D4800F555A48195C23EB5ECB1C4BB" width="50%" height="50%" />

<!-- endtab -->

<!-- tab 源码 -->

```CSS
/*友链美化*/
#article-container .flink .flink-list > .flink-list-item {
  margin: 15px 7px;
  height: 99px;
  border-radius: 11px;
  line-height: 17px;
  border-style: groove;
  border-color: #f4f4f4;
}
/* 头像微调 */
.flink-item-icon {
  margin-right: 0 !important;
  transition: .5s !important;
}
.flink-item-name,
.flink-item-desc {
  padding-left: 10px !important;
}
/* 去掉原来自带的before */
#article-container .flink .flink-list>.flink-list-item::before {
  content: none;
}
/* 鼠标经过改变背景 */
#article-container .flink .flink-list>.flink-list-item:hover {
  background-color: #739d8f;
  box-shadow: 0 0 20px rgba(0, 0, 0, .3);
}
/* 鼠标经过改变文字颜色 */
#article-container .flink .flink-list>.flink-list-item:hover a {
  color: white !important;
}
/* 鼠标经过头像滚动 */
#article-container .flink .flink-list>.flink-list-item:hover .flink-item-icon {
  width: 60px;
  margin-left: -70px;
  -webkit-transform: rotate(-180deg);
  -moz-transform: rotate(-180deg);
  -o-transform: rotate(-180deg);
  -ms-transform: rotate(-180deg);
  transform: rotate(-180deg);
}
/*侧边栏标签美化*/
#aside-content .card-tag-cloud a {
  color: var(--heo-fontcolor) !important;
  font-size: 0.8rem;
  border-radius: 9px;
  border-style: dashed;
}
#aside-content .item-headline {
  font-weight: 700;
}
```

<!-- endtab -->

{% endtabs %}

## 页脚美化

{% tabs test4 %}

<!-- tab 预览 -->

<img src="https://preview.cloud.189.cn/image/imageAction?param=57F49F1A36990AC53099045AEB0D1F0B306BBB278DBA1EADFA700410B0F542A3CD9D9E1A6DB086962E511A4DEF4414531F8CA9D04AE7E27178C60CB1943E1CF8D7CA6DEBDB8914558B59228A315B0ECF24439EA76C7522763D378DA8244AAAC508B019B11A6C29C06846934D63C814EC" width="50%" height="50%" />

<!-- endtab -->

<!-- tab 源码 -->

```CSS
/*页脚美化*/
#footer-wrap {
  text-align: left;
  background-color: #203e57;
}
```

<!-- endtab -->

{% endtabs %}

## 侧边栏标签

{% tabs test4 %}

<!-- tab 预览 -->

<img src="https://preview.cloud.189.cn/image/imageAction?param=E61F52199B71004E9C5832F956AD9D36B5D37F43455C042DAB2D6A4BE5A3AEE584C6E075EDB841E192A10F9112C9A3CF8E629F9EC476EFB8EEBCFF2D894565E935B40A2823D9276E9084971DD992351D5D87F6B2ECB90B4096177F5F84F6CABEAB6D9C86FD72DC12A740FA2D896F7626" width="25%" height="25%" />

<!-- endtab -->

<!-- tab 源码 -->

```CSS
/*侧边栏标签美化*/
#aside-content .card-tag-cloud a {
  color: var(--heo-fontcolor) !important;
  font-size: 0.8rem;
  border-radius: 9px;
  border-style: dashed;
}
#aside-content .item-headline {
  font-weight: 700;
}
```

<!-- endtab -->

{% endtabs %}

## 选中字体颜色

{% tabs test4 %}

<!-- tab 预览 -->

<img src="https://preview.cloud.189.cn/image/imageAction?param=FB81F3FA5F852DCEC69EE17B52589396F130B51104C651F2721B125A4103F8FF0C0CFA103DAD49BC6C1B31DABC734AAAF9BA31968F0017ED68800D88CE1858FCFF0EFE9600C219046E4D573943868F3E5929EB0C6D8A606F7E780333F5BB0F3D597A0E1014297EE303F342B37E38D899" width="25%" height="25%" />

<!-- endtab -->

<!-- tab 源码 -->

```CSS
/*选中颜色*/
*::selection {
  background: #df3030;
  color: #f7f7f7;
}
```

<!-- endtab -->

{% endtabs %}
