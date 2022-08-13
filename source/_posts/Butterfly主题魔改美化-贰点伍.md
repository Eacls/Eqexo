---
abbrlink: ''
categories:
- 实用教程
cover: https://preview.cloud.189.cn/image/imageAction?param=E6827909F7D2C1714496455CF07B9C61818A0E8AD293B14F196D62222960E233BEDBD7834EFBA29A609FAC8E33472F42D0075044E4737F87314764386D29C29A7A1063BDFDDC0746B16BADC0DFDD51C6B0E9241DA117DCD44C41F776AAEF157A55673BAAC5D6859FD9394D46D5AF1772
date: '2022-08-13 06:55:46'
description: 文章页面风格协调
tags:
- Hexo
title: Butterfly主题魔改美化-贰点伍
top_img: https://preview.cloud.189.cn/image/imageAction?param=4037525B5116A9E3A21832EF9B312D9D162FE4822D76482C36C3F59A1B9C9109FC52161B154221F75349C436842C39BEF16E2169E6A1B618734DAF99333BF2B3E757E6C29DDEEED054353664B03579C0DA901557A5B360D45E7C20F70BA6FA9A721A94D780CD50549516F4D4D647B719
updated: '2022-08-13 06:55:47'
---## 为什么是贰点伍而不是叁

这篇文章更多的是对[魔改美化贰](https://www.eacls.top/posts/286b8081/)的一个补充，完善那些在贰中未提及但影响整体协调性的点。至于叁，将会是一次大改，暂不确定出品日期。

---

## 版权卡片美化

{% tabs test4 %}

<!-- tab 预览 -->

**![ ](https://preview.cloud.189.cn/image/imageAction?param=B7A74D3AA9F50ADAE2304E338439F734DB5C1331A769E36A7C64A5527CFDEF2DF06F00CBBA11032D26A778752F8588F767C775CF5A135970E50C023785616B0EF70FD8CC103544E4A4326212C63F4CE93E386DFB928F5DD262F49E31681AE2E2E98AE84454777B2EEE9616031BCBF624)**

<!-- endtab -->

<!-- tab 源码 -->

```CSS
/*版权卡片美化*/
#post .post-copyright {
position: relative;
margin: 2rem 0 0.5rem;
padding: 1.5rem 0.8rem;
border: 8px solid #f6f6f6; /*卡片边框*/
border-radius: 20px; /*边框圆角*/

#post .post-copyright:before {
position: absolute;
top: -1.9rem; /*C位置*/
color: #49b1f540; /*C颜色*/
font-size: 6rem; /*C大小*/
}
```

<!-- endtab -->

{% endtabs %}

## 文章分页卡片美化

{% tabs test4 %}

<!-- tab 预览 -->

**![ ](https://preview.cloud.189.cn/image/imageAction?param=D78AB1A5F8FC66E257AFE6E64B129DA7E13DD8E09A45A9C85455AC40935BB65B966A6880729B1DB8A02DC49669616828478E2ADA87E6DA42F9CB5035356EBB4605FD08C9931113F93A0B982C01A7DC3E8A085AD9454B2A8507D9299663E81F7DCA4C0904723CC2ABFD9B3DB697872D81)**

<!-- endtab -->

<!-- tab 源码 -->

```
/*文章分页卡片美化*/
#pagination .prev-post a, #pagination .next-post a {
  border-style: ridge;
  border-width: 8px;
  border-color: #d2d2d2;
}
```

<!-- endtab -->

{% endtabs %}

## 相关推荐卡片美化

{% tabs test4 %}

<!-- tab 预览 -->

**![ ](https://preview.cloud.189.cn/image/imageAction?param=BD13D26372330F6914FEE143742FB4A3797D5968F9AA12FE3CA335E19B113C7C762D1BF057AC4523A1884A56A7A5A7B73E5419E43A21373C2138E0A96B342E9BC33723B5919D7895E8783E8BC575A14B66BBE63B4B130335359A22ABFFFF21761CD0C5473A5CD07C0904D58518E24F5E)**

<!-- endtab -->

<!-- tab 源码 -->

```
/*文章相关推荐卡片美化*/
.relatedPosts > .relatedPosts-list > div {
  border-radius: 20px;
}
```

<!-- endtab -->

{% endtabs %}

## 目录颜色圆角调整

{% tabs test4 %}

<!-- tab 预览 -->

**![ ](https://preview.cloud.189.cn/image/imageAction?param=D4845D7B6E4D387FB54F9DDEC6589D0662D3F6D273E796BCB76757BA19606A240B6A3A54088BE5023D5D4EF7F305DA8B117AB291B018C80DABFF2FAAC8425CDC5654CE40EFDD6C8EE502E99771F04E107523122BD664D2804E9DF481283D88D04E6224F08579124015A3F5E78277624E)**

<!-- endtab -->

<!-- tab 源码 -->

```
#aside-content #card-toc .toc-content .toc-link.active {
  background: #669cbe;
  border-radius: 5px;
}
```

<!-- endtab -->

{% endtabs %}

## 关于魔改美化理念

**博客的魔改美化应遵循阅读体验优先的原则，保持纯净页面，因而不做繁冗的增添与过于商业性质的修改。**
