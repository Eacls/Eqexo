---
categories:
- 实用教程
cover: https://preview.cloud.189.cn/image/imageAction?param=D46AAD69B808AEECA37C93A0EB7E1E52FC04A29912945EC7D849F8E14F9D473E03AF9B6E1EFF847419D35F747182A11A6395347B1B3EA69E162CCCBD0FC2FED3C68721F2E7A6996BB3E7C41AD7C99D647A443D026BB41130FFE8ECA1357051B5C97552A0402CF3781D31333B2520ACD2
date: '2022-08-07 21:38:43'
description: UI界面美化，提高用户视觉体验
tags:
- Hexo
title: Butterfly主题魔改美化-贰
top_img: https://preview.cloud.189.cn/image/imageAction?param=02752F480DE3A48DEAC3B84474EE6A7E91F2EB7096FE3CFB5031FDC056FDCE95B0B560538E0DCB9DAD42A71C219139B787A37FFB8C60EBFA98919414B62F5F36F1F3685FAC9C1DCF49D2CE751B24C75184A6B13D6929656F819BFC427F0DB54DD1C88F0B693DA221EDDC6EBB8AB0E661
updated: '2022-08-08 06:42:34'
---
## 前言

在今年年初时，我曾把过去魔改的内容记录成了文章：[魔改美化教程壹](https://www.eacls.top/posts/cecc48c5/)。半年过去，除了小修bug外没再有新的博客优化工作出现。今天抽了一整天时间，将我的博客进一步美化，打磨访客轻体验。

> 本篇教程基于Butterfly主题3.8.3版本（养老版本☺）

> 本篇优化方案均采用外挂css方式

---

## 全局字体修改

修改字体通常有两种方式：本地引入和外链引入。因为本地引入通常会非常拖慢速度，故本篇教程不在提供本地引入的方法，如需可阅读  [字体修改-Ordis博客](https://imbhj.com/25c13146/)  。
外链引入在css文件内添加如下代码

```
@font-face {
	font-family: Yourfontname;
        font-display: swap;
	src: url('https://xxxxxxxxxxxxx.woff') format('woff');
}
```

其中`font-family`为你所引入字体的名称，可自定义。`url`为要引入字体的链接，不建议使用jsdelivr进行加速，否则你会得到一个和放在本地差不多的响应速度。`format`为你所引入字体的类型，如不清楚可以下载下来看文件管理器内所标注的类型或者使用百度。
接下来在配置文件`_config.butterfly.yml`内找到

```
font:
  global-font-size: 16px # 字体大小
  code-font-size:
  font-family: Yourfontname, "Microsoft YaHei", "PingFang SC" # 全局字体
  code-font-family: Yourfontname, "Microsoft YaHei", "PingFang SC" # 代码字体
```

按如上填入。

## 文章页卡片宽幅占比

{% tabs test4 %}

<!-- tab 预览 -->

**![文章卡片在整体页面占比即左右边距](https://preview.cloud.189.cn/image/imageAction?param=EF8EB3AD908C75068A4AAB8524D098E2A5EFBDD47AA6624882737A66760C543BD313DE0680988B88EAF624247A2865D75360CBE8217D3D05EDD874CD2CC7ADB51BE73C0F1051F08CF120A238C9BD2DC1B58C4E3645A30CAE85D27691AF43104464D78931D517FD7CDC80B8356A81BF46)**

<!-- endtab -->

<!-- tab 源码 -->

```
/*文章页卡片宽幅占比*/
.layout {
            max-width: 1280px;
      }
```

<!-- endtab -->

{% endtabs %}

## 文章卡片圆角

如目录3图所示圆角

```
/*文章页卡片圆角*/
.layout > div:first-child:not(.recent-posts) {
  border-radius: 35px;
}
```

## 文章页信息栏美化

{% tabs test4 %}

<!-- tab 预览 -->

**![字体增大，字间距增大，位置高度调整](https://preview.cloud.189.cn/image/imageAction?param=410575F9873CD3F460CFFE0A02820A444BF29D47676C4E6B2C412D7045E373542D341FCB49F3A8BA5DE8A008A8306490DC3D711DFECDE9C1DC90A2A8EEE87DA0EE6BDC1DB5164A3C507C83296FBEDE5392C2367D4150B69DF986E09FDF70FA51789A0B6187B442E4BBB56E4054DC9CD2)**

<!-- endtab -->

<!-- tab 源码 -->

```
/*文章页信息栏美化*/
#post-info .post-title {
  font-weight: 600; /*字体粗细*/
  font-size: 2.5em; /*字体大小*/
  line-height: 2.2; /*元素高度*/
  letter-spacing: 9px; /*字体间距*/
}

/*整体位置调整*/
#page-header #post-info {
  bottom: 8rem;
}

/*移动端信息栏适配*/
#page-header.post-bg {
  height: 26rem;
}
```

<!-- endtab -->

{% endtabs %}

## 顶栏美化

{% tabs test4 %}

<!-- tab 预览 -->

**![字体加粗，调整间距，简洁ui](https://preview.cloud.189.cn/image/imageAction?param=2B26A8B2DB9D44015E577CAAD089A42B2E38B1F804F1492386CE5D4658D6EA2ADFC3609F17AD497C12319730A38212CC0BBB42A012A10E8CABFE85948CC8F6998320DC44F023BC4B7CF1A1645C976C7593F0B847A18AE3931D30E5B09214294F07CB2E398A8584E10A1662D1C37D263B)**

<!-- endtab -->

<!-- tab 方法 -->

主题配置文件`_config.butterfly.yml`内找到`menu`，将后面的icon图标删除。
并在css文件内添加如下代码

```
/*顶栏美化*/
#nav .site-page {
  font-size: 0.79em; /*字体大小*/
  letter-spacing: 3px; /*字体间距*/
  font-weight: 600; /*字体粗细*/
}

#nav {
  height: 70px; /*顶栏高度调整*/
}
#page-header.nav-fixed #nav {
  top: -70px; /*顶栏调整空缺补齐*/
}
```

<!-- endtab -->

{% endtabs %}

## 文章页目录卡片圆角

{% tabs test4 %}

<!-- tab 预览  -->

**![圆角](https://preview.cloud.189.cn/image/imageAction?param=DDFB53EACEA7D567AF6C46A41F62749CA61AE7ADE787FA303EBFDB34D8E8279FBE145EFC2D24A2E537425637ABF851DF7027FB6860A5A129877E4DD2B421330298B95476C4B5D1D8477F4B1656F99B59CB3FE8C1D1B34F73C0D074548B5D15E3340544A88E8698C61B8BAFF9C0D6B976)**

<!-- endtab -->

<!-- tab 源码 -->

```
`/*文章页目录卡片圆角*/`
#aside-content .card-widget {
border-radius: 20px;
}
```

<!-- endtab -->

{% endtabs %}

## 文章页目录美化

如目录7图所示

```
/*文章页目录美化*/
#aside-content .card-widget {
  padding: 2rem 1.2rem; /*前者为上下边距，后者为左右边距*/
}
```

## 调宽页脚

增加页脚文字上下边距

```
/*调宽页脚*/
#footer-wrap {
  padding: 3rem 2rem; /*前者为上下边距，后者为左右边距*/
}
```



## 为什么这么调整

<!-- Why do-->

- **本篇美化方案优化了Web端的阅读体验，采用平铺的方式提高显示利用面积。**
- **本篇美化方案提高了文字的粗度，提升了可读性**
- **本篇美化方案加强了对市面上主流设备的适应度，改进了UI设计**

