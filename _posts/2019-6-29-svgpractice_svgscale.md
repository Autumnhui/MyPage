---
layout: post
title: 图片高糊？在SVG的世界不存在的！
author: Autumnhui
date: 2019-6-29
categories:
     - svg
---

# 为什么是SVG？

在前面的文章中，我们了解到，SVG图片是由数学定义来得出来的，我们对svg的修改可以通过修改svg的代码来实现，我们也可以利用工具去创造一些svg图片。

正是因为SVG生成的特别之处，它 **可以无限放大、缩小而图片的质量不受到影响。**

---

#### 我们找个SVG来演示一下~
<br>
<br>
<center> ↓ 这里是一个宽高都是100px的svg ↓<br><br>
<svg width=100px height=100px version="1.1" id="Layer_1" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" x="0px" y="0px"
	 viewBox="0 0 512 512" style="enable-background:new 0 0 512 512;" xml:space="preserve">
<polygon style="fill:#D32E2A;" points="385.829,128 385.829,256 347.429,291.072 307.2,256 272.457,241.371 306.59,165.51 "/>
<polygon style="fill:#3A5BBC;" points="384,385.219 256,385.219 255.39,383.391 226.133,356.291 255.39,308.041 270.629,271.848 
	355.962,302.043 "/>
<polygon style="fill:#FBBB00;" points="256.61,128.61 288.305,164.901 256.61,203.959 241.371,240.152 161.524,200.253 128,126.781 
	256,126.781 "/>
<polygon style="fill:#28B446;" points="239.543,270.629 204.495,346.843 126.171,384 126.171,256 163.962,232.558 204.8,256 "/>
<polygon style="fill:#518EF8;" points="512,256 384,385.219 270.629,271.848 307.2,256 385.829,256 "/>
<polygon style="fill:#91C646;" points="255.39,383.391 255.39,512 126.171,384 239.543,270.629 255.39,307.2 255.39,308.041 "/>
<polygon style="fill:#FFD837;" points="241.371,240.152 204.8,256 126.171,256 0,256 128,126.781 "/>
<polygon style="fill:#F14336;" points="385.829,128 272.457,241.371 256.61,204.8 256.61,203.959 256.61,128.61 256.61,0 "/>
</svg>
</center>

#### 我们在不改变svg本身模样的情况下，只修改大小，看看会不会变模糊~
<br>
<br>
<center> ↓ 这里是一个宽高都是500px的svg ↓<br><br>
<svg width=500px height=500px version="1.1" id="Layer_1" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" x="0px" y="0px"
	 viewBox="0 0 512 512" style="enable-background:new 0 0 512 512;" xml:space="preserve">
<polygon style="fill:#D32E2A;" points="385.829,128 385.829,256 347.429,291.072 307.2,256 272.457,241.371 306.59,165.51 "/>
<polygon style="fill:#3A5BBC;" points="384,385.219 256,385.219 255.39,383.391 226.133,356.291 255.39,308.041 270.629,271.848 
	355.962,302.043 "/>
<polygon style="fill:#FBBB00;" points="256.61,128.61 288.305,164.901 256.61,203.959 241.371,240.152 161.524,200.253 128,126.781 
	256,126.781 "/>
<polygon style="fill:#28B446;" points="239.543,270.629 204.495,346.843 126.171,384 126.171,256 163.962,232.558 204.8,256 "/>
<polygon style="fill:#518EF8;" points="512,256 384,385.219 270.629,271.848 307.2,256 385.829,256 "/>
<polygon style="fill:#91C646;" points="255.39,383.391 255.39,512 126.171,384 239.543,270.629 255.39,307.2 255.39,308.041 "/>
<polygon style="fill:#FFD837;" points="241.371,240.152 204.8,256 126.171,256 0,256 128,126.781 "/>
<polygon style="fill:#F14336;" points="385.829,128 272.457,241.371 256.61,204.8 256.61,203.959 256.61,128.61 256.61,0 "/>
</svg>
<br>
<br>
我们直接把它放大了5倍，显然，图片的质量丝毫没有改变！下面我们试试缩小？
</center>
<br>
<br>
<center> ↓ 这里是一个宽高都是50px的svg ↓<br><br>
<svg width=50px height=50px version="1.1" id="Layer_1" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" x="0px" y="0px"
	 viewBox="0 0 512 512" style="enable-background:new 0 0 512 512;" xml:space="preserve">
<polygon style="fill:#D32E2A;" points="385.829,128 385.829,256 347.429,291.072 307.2,256 272.457,241.371 306.59,165.51 "/>
<polygon style="fill:#3A5BBC;" points="384,385.219 256,385.219 255.39,383.391 226.133,356.291 255.39,308.041 270.629,271.848 
	355.962,302.043 "/>
<polygon style="fill:#FBBB00;" points="256.61,128.61 288.305,164.901 256.61,203.959 241.371,240.152 161.524,200.253 128,126.781 
	256,126.781 "/>
<polygon style="fill:#28B446;" points="239.543,270.629 204.495,346.843 126.171,384 126.171,256 163.962,232.558 204.8,256 "/>
<polygon style="fill:#518EF8;" points="512,256 384,385.219 270.629,271.848 307.2,256 385.829,256 "/>
<polygon style="fill:#91C646;" points="255.39,383.391 255.39,512 126.171,384 239.543,270.629 255.39,307.2 255.39,308.041 "/>
<polygon style="fill:#FFD837;" points="241.371,240.152 204.8,256 126.171,256 0,256 128,126.781 "/>
<polygon style="fill:#F14336;" points="385.829,128 272.457,241.371 256.61,204.8 256.61,203.959 256.61,128.61 256.61,0 "/>
</svg>
<br>
<br>
把svg的长宽限定为50px，svg的质量也没有受损！
</center>

### 优势与劣势

我们可以看到，SVG的优势很多————
1. 图片小，加载速度快，对网页非常友好；
2. 可编辑，我们可以对它的颜色，样式，大小进行修改创造；
3. 结合CSS可以进行动画效果。
等等

而劣势也非常明显————
1. 图形相对简单，如果复杂的话创造需要大量时间；
2. 不便于传播（相对于我们日常使用的图片格式来讲）；
3. 更适合用来作为网页的小图标

---

虽然缺点存在，但是结合位图与矢量图的优缺点，取长补短，创造出更有趣的玩法。