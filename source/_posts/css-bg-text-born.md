---
title: 稍微有点炫酷的字体特效
categories: css
tags:
  - background
  - text
---

## 稍微有点炫酷的字体特效

### 效果图 
![测试地址](/assets/img/document/text-background-style.gif)

### 效果解析
#### 字体效果
字体效果利用是字体透明，加backgrond-clip ，背景显示在字体上，
主要代码是如下
```
background-clip: text;
-webkit-background-clip: text;
color: transparent;
background-image: url("https://img95.699pic.com/photo/40159/9971.gif_wh300.gif");
```

#### border边框的特效
首先是边框的初始状态
```
border: 10px solid;
border-image: linear-gradient(45deg, #f863dd, #9198e5) 1;
```
再加上个动画
```
animation: borderTransform 3s infinite;

 @keyframes borderTransform {
      0% {
        border-image: linear-gradient(45deg, #f863dd, #9198e5) 1;
      }
      33% {
        border-image: linear-gradient(135deg, #3a48e6, #aa188f) 1;
      }
      66% {
        border-image: linear-gradient(45deg, #22d7b5, #cd1b39) 1;
      }
      100% {
        border-image: linear-gradient(45deg, #f863dd, #9198e5) 1;
      }
    }
```