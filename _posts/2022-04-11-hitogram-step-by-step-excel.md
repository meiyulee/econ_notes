---
title: 如何在Excel中畫直方圖 Part II
description: 直方圖是我們資料分析流程第一步驟對數據粗略觀覽的方式。若不想使用資料分析功能和樞紐分析，還有什麼辦法做到直方圖呢？且看本文教你如何使用函數繪製出直方圖
author: 李玫郁
date: 2022-04-11
categories:
 - 大數據分析
tags: [直方圖]
image: https://raw.githubusercontent.com/meiyulee/pic001/master/histogram/histogram_041.JPG
layout: post
---

1. 前言

之前我已經發布了一篇有關如何使用Excel製作直方圖《[如何在Excel中畫直方圖 Part I](https://meiyulee.github.io/leetalk/2022/04/11/hitogram-povit-table)》。除了資料分析工具和樞紐分析外，有沒有辦法直接建立次數分配表，畫出直方圖呢？答案是可以的。我們可以根據次數分配表的製作流程，搭配Excel的計數型函數，幫助我們找出各組的次數。以下我將說明如何完成次數分配表和直方圖。

![](https://raw.githubusercontent.com/meiyulee/pic001/master/histogram/histo_042.jpg)

# 2. 製作流程說明

當我們取得數據後，就可以為數據建立次數分配表。

<img src="https://raw.githubusercontent.com/meiyulee/pic001/master/histogram/histo_033.JPG" width="300">

很多人認為這是很基礎的方法，也確實如此。但之前在臉書粉專或推特上我曾經提到過Deep AI的檢驗也是使用到將數據畫成分布直方圖 [^1],[^2]，這對我們來說那樣的直方圖非常粗糙，無法趨近連續。若是單純的文字型數據分類，也就算了。非間斷的數字型數據理應趨近連續。若我們墨守在21~25組的分類組數，實在不恰當。

那麼我們可以怎麼做呢？數據的次數分配表編表是有其程序的。

- 第一步：先將數據從小排到大。這方便我們找出最大、最小值。

![](https://raw.githubusercontent.com/meiyulee/pic001/master/histogram/histo_034.JPG)

- 第二步：排序好的數列就可計算全距，亦即最大值-最小值。
- 第三步：組數可以使用上圖的公式。在600個樣本數可得到log值為10.643856189774725，加1後得到組數為11組。但如果我們要讓分布有連續型的感覺，就得有270組。我接下來將以200組為例做次數分配表。有興趣的朋友可以使用270組。
- 第四步：基於第二和第三步得到的全距及組數，就能計算出組寬，有的課本會稱為組距。這是組上限和組下限的距離。只要數據的值落於組上限和組下限內，就會被計為1。其它分組則會被計為0。

![](https://raw.githubusercontent.com/meiyulee/pic001/master/histogram/histo_035.JPG)

![](https://raw.githubusercontent.com/meiyulee/pic001/master/histogram/histo_036.JPG)

- 第五步：確定上下限。第一組的下限直接使用最小值。第一組的組上限為組下限加組寬。

![](https://raw.githubusercontent.com/meiyulee/pic001/master/histogram/histo_037.JPG)

第二組的組下限為第一組的組上限。將I2的公式複製到I3後，反白H2和I2，向下複製公式產生200組結果。

不過想畫次數分配表還需要一些計算。

- 第5.1步：計算組中點，做為次數分配表的各組代表。
- 第5.2步：計算每組的次數。這邊我使用【countifs】函數，為特定數據範圍加上計算的條件。

![](https://raw.githubusercontent.com/meiyulee/pic001/master/histogram/histo_038.JPG)

因為經排序後的數據要落在特定組的組下限和組上限之間，所以countifs是最合適的函數。那麼讓我延伸一下，如果你要做同時有兩欄數據的聯合機率呢？是的，你的countifs需要4個條件。

我現在只有一個欄位的數據，所以就只用兩個條件去計數，得到下圖的結果。

![](https://raw.githubusercontent.com/meiyulee/pic001/master/histogram/histo_039.JPG)

- 第5.3步：我還需要將次數轉為相對次數。所謂相對次數是指該組的次數占全體數據個數的比例。如L欄所示。同時也可以計算累積的相對次數，如M欄結果。

- 第六步：繪製直方圖。我喜歡先選擇空白的儲存格，先插入圖表，再使用圖表工具的選取資料，自訂選擇需要對應的數據位置。

![](https://raw.githubusercontent.com/meiyulee/pic001/master/histogram/histo_041.JPG)

上面的Excel檔案如果有需要的朋友，請電郵給我，我將會將檔案回傳給你。如果你在臉書粉絲專頁看到本文的貼文，可在貼文下方給我，我會私訊回覆你。

# 參考資料

[^1]: DeepAI的 [推特文](https://twitter.com/Deep__AI/status/1513427571005804545?s=20&t=tLSG0fo2j-XXAnu6CHcbjA)。這邊是在講機率分配，而且不敢使用隨機樣本打出直方圖或連續圖形，[原文](https://deepai.org/machine-learning-glossary-and-terms/probability-distribution)。

[^2]: DeepAI的 [推特文](https://twitter.com/Deep__AI/status/1510619319444467716?s=20&t=tLSG0fo2j-XXAnu6CHcbjA)。它這篇推特文在講t檢定，t分配是連續型分配，DeepAI用19組的直方圖去表示。