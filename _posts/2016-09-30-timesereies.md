---
layout: post
tags: [時間序列]
date: 2016-09-30 19:18
thumbnail: http://cdn1.thedataschool.co.uk/wp-content/uploads/2016/02/20161846/timeseries.png
title: 時間序列模型分析 - 是否需要定態
published: true
categories:
 - 統計觀念
---

數據分析可以成功的原因來自於使用統計學的分析方法，以及電腦軟體的運用。觀察迴歸分析與計量經濟學的基礎皆是從「線性模式」出發，藉由最小平方法的計算，得到估計係數的數學式，此時，一點都不需要分配的假設 - 常態分配。<br />

於是，在高等計量經濟學當中，逐漸地只寫出iid的符號，至於Normal假設則是慢慢消失。但，我們反思，即使沒有寫出Normal符號，是否估計係數的分配就能夠得到，或許讀者可以問問你的老師 (笑)。<br />

<!--more-->

有趣的是，同樣的狀況發生在線性模式改為二次式或三次式，即使教科書上寫出來高階次方數的函數，我們卻沒有見過有人跑出結果來 (笑)。這是否表示那是所有撰寫者與理論家的最終極目標呢？我們不可而知.......<br />

此時，為了能夠讓資料符合線性模式，資料使用者只能做一件事情，那就是 - <b><span style="background-color: yellow; color: red;">資料轉換</span></b>，也就是定態(<a href="http://nccur.lib.nccu.edu.tw/bitstream/140.119/36864/7/101407.pdf" target="_blank">Stationary</a>)。<br />

讓資料定態的方式最簡單的就是差分，然後檢查是否滿足定態條件(請參考任何一本時間序列教科書都會寫)。只因欲檢定的序列資料若不是定態的話，要做「差分」直到定態(<a href="http://nccur.lib.nccu.edu.tw/bitstream/140.119/34015/7/52001107.pdf" target="_blank">連結</a>&nbsp;p.2)。對資料分析的人員而言，當資料進行差分後將會發生什麼事情呢？<br />

可想而知，部分資料特性將會消失！
如果你驗證過資料特性，如<a href="http://econcloud.blogspot.tw/2015/07/blog-post_42.html" target="_blank">從巨量資料分析方法找台日韓兌美元匯率機率密度函數</a>，從排序後的資料了解匯率母體分配圖與係數告知之資料特性，那麼，當資料不排序，而是依時間進行迴歸分析，是否就能知道時間變數(固定趨勢)其實就是可以抓住的趨勢，無論固定趨勢、波動或小部分不規則性(但具備短時間同方向)都可以被時間變數所表示。<br />

唯一的問題就是你用線性模式看資料！所以，才需要捨棄部分資料特性，方能使用線性模式去配適，以及忘記了配適後還要轉回原本的資料(但數學轉不回去，Jacobin算不出來)，所以，我們看到的都是資料差分、差分、再差分，滿足定態後的資料再去線性估計，而不是真實資料配適出估計多項式或線性估計後再反轉回原始資料的方程式。<br />

於是，我們可以得到一個結論

<blockquote class="tr_bq">
資料為了適用線性模式需要做定態</blockquote>
<blockquote class="tr_bq">
找出資料真實模式須使用原始資料&nbsp;</blockquote>


參考資料

1.&nbsp;<a href="http://homepage.ntu.edu.tw/~sschen/Book/Slides/Ch2Basic.pdf" target="_blank">連結</a><br />
2. www3.nccu.edu.tw/~jthuang/class16b.ppt<br />
3. https://www.cyut.edu.tw/~finance/docs/1030-1.pdf<br />
4. <a href="http://yaya.it.cycu.edu.tw/course/grad_proj/90/%E5%94%90%E5%BF%83%E6%80%A1.pdf">連結</a><br />
<div>
<br />
<br /></div>
