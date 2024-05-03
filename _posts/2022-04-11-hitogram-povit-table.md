---
title: 如何在Excel中畫直方圖 Part I
description: 樞紐分析是非常好用的工具，可以協助數據做分類，並且可形成行列的矩陣平面，無論是畫單一隨機變數的分布直方圖或是二隨機變數的聯合分布直方圖都很好用。
author: 李玫郁
date: 2022-04-11
categories:
 - 機率分配模擬器
tags: [直方圖,大數據分析,Excel]
image: https://raw.githubusercontent.com/meiyulee/pic001/master/histogram/histogram_032.JPG
layout: post
---

# 1. 前言

當我們能夠使用Excel生成出數據後，你有沒有工具可以幫助你繪圖呢？除了使用特殊的軟體幫助你快速弄出次數分配表外，還有一個在Excel中常用的工具，那就是「樞紐分析」。很多人認為要畫直方圖可以使用【資料】頁籤的【數據分析】工具，但使用前請先自己設定好「組界」，如下圖的M欄和N欄。

![](https://raw.githubusercontent.com/meiyulee/pic001/master/histogram/histogram_021.JPG)

圖1

# 2. 使用資料分析工具的直方圖功能

使用Excel內建的資料分析工具，位置在【資料】→【資料分析】的【資料分析】。點擊後會跳出新視窗，視窗畫面如圖2。

![](https://raw.githubusercontent.com/meiyulee/pic001/master/histogram/histogram_022.JPG)

圖2

可以選擇的分析工具選單，捲動向下後，可以找到中文直方圖，或英文的histogram。如圖3。點擊後出現藍色，再按【OK】。

![](https://raw.githubusercontent.com/meiyulee/pic001/master/histogram/histogram_023.JPG)

圖3

接著挑出新視窗準備設定輸入範圍、組界範圍。因為我在選擇時連同第一列的標籤都一起選擇，所以要勾選【Label】。

你可以將結果輸出到新的工作表或是如同圖3，直接選擇原工作表的空白儲存格。

我同時勾選了柏拉圖(經排序後的直方圖)，以及累計百分比率的結果。

圖3的畫面完成後，點擊【OK】，回到原工作表，並顯示結果，如圖4。

![](https://raw.githubusercontent.com/meiyulee/pic001/master/histogram/histogram_024.JPG)

圖4

動作到這邊基本上需要的數字都有了。不過直方圖的frequency(R欄)需要調整成百分比，所以你還需要另外加工後才可以畫出單一隨機變數的直方圖。

我個人不太喜歡用這個功能，因為太麻煩了。那我們可以改用樞紐分析。

# 3. 樞紐分析

樞紐分析按鈕的位置在【插入】。工具選單中的最左邊。

![](https://raw.githubusercontent.com/meiyulee/pic001/master/histogram/histogram_025.JPG)

圖5

建議在點選樞紐分析前，先將滑鼠點擊A1儲存格，這樣等下點選【樞紐分析】後，會自動選取數據。

![](https://raw.githubusercontent.com/meiyulee/pic001/master/histogram/histogram_026.JPG)

圖6

因為我先點選A1儲存格，在樞紐分析的設定視窗跳出後，數據範圍就被選定。這確實是我的原始數據範圍。

如果你想在原始數據的工作表繼續操作樞紐分析，請選擇Existing worksheet。我通常習慣創建新的工作表，所以不改原始設定，直接按【OK】。

我的版本為英文版，可以參考截圖畫面，中文版在相同位置，所以語言不影響我們的設定選擇。

![](https://raw.githubusercontent.com/meiyulee/pic001/master/histogram/histogram_027.JPG)

圖7

接下來請依照圖7的設定。在右下位置，行列各自拖曳X1和X2，數值位置則任意拖曳X1或X2都可以。請檢查確認是count(計數)。

這點非常重要。因為我們是計算有幾個，而不是讓數字相加，所以要用count。

另外在這個畫面一開始會非常慢。X1和X2各1百萬筆數字都會被拉進來作為行列的標籤。這需要耐心等待，別誤會軟體當了。

接著要如同圖7的行列標籤變成【群組】，我們得在行或列標籤上點擊右鍵，出現圖8畫面。

![](https://raw.githubusercontent.com/meiyulee/pic001/master/histogram/histogram_028.JPG)

圖8

點擊【group】後會跳出新視窗，如圖9。

![](https://raw.githubusercontent.com/meiyulee/pic001/master/histogram/histogram_029.JPG)

圖9

我沒有更改起始點和終點數值。你可以嘗試改為0和166。此處的【By】是每組的組距。這點和數據分析工具內的直方圖設定組界不同。

設定完成後按【OK】。

行列標籤都要設定。設定完成後就是圖7了。

## 3.1. 繪製3D立體直方圖

在選擇繪製圖形前，請先確定你已經選擇一個樞紐分析範圍的儲存格。這樣才會出現樞紐分析工具頁籤，如圖9。

![](https://raw.githubusercontent.com/meiyulee/pic001/master/histogram/histogram_030.JPG)

圖9

我們點選【樞紐分析圖】，然後如同圖10，選擇3D立體直方圖。

![](https://raw.githubusercontent.com/meiyulee/pic001/master/histogram/histogram_031.JPG)

圖10

點選下方的【OK】後，等待圖形出現。

以下你不一定要這樣做！圖形出現後，在圖形上按右鍵，選擇【移動圖表 move chart】。我是移動到新的工作表，出現圖11。

![](https://raw.githubusercontent.com/meiyulee/pic001/master/histogram/histogram_032.JPG)

圖11

圖11分組的組數不夠多，所以畫面就會像圖11一般。如果細緻點會怎樣？
如果分組到足夠細膩，我們就可以跑出如JAVA畫出的圖12

![](https://raw.githubusercontent.com/meiyulee/pic001/master/histogram/joint_001.JPG)

圖12

## 3.2. 比較圖11和圖12

使用樞紐分析繪圖的缺點就是分組的表示方式很醜，如圖11，不能用組中點表示。當然我們可以將樞紐分析的結果，複製後貼到新的工作表，再將組中點找到後覆蓋上去。

另外分組的過程中，組距設定非常重要，才能讓你得到200組以上的分組。當然這也可以做到270組[^1]，可趨近連續的分組組數。需要注意的是270*270的矩陣畫出3D立體圖時會更慢。

讓我們比對圖11和圖12，都是來自隨機樣本的數據，但C語言執行和JAVA繪圖可以讓圖形更為精細，並且還能展現出隨機性與底面積。即使圖11顯得比較粗造，我們一樣可以發現集中位置是一致的。

# 4. 小結

我們可以獲得比較好的軟體讓數據快速分組並計算好次數分配表，與此同時，我們還能得到如[二維常態分配介紹](https://meiyulee.github.io/leetalk/2022/04/08/bivariate-normal)一文中的3D立體圖繪製方法。

不過，在軟體學習成本高的情況下，辦公室人員如何從單調的行政業務，躍升到具備數據分析能力，Excel肯定是你最棒的工具。讓我在這臭屁一下Excel的威力：Excel可以讓你看到每個動作的過程，如何生成數據、如何轉換數據、如何處理數據等，再加上有限的繪圖工具就能夠讓你的數據分析基礎遠勝於那些使用「工科神器」那群人。

有需要此文的Excel檔，可在臉書下留言，我將會私訊回傳給你。如果是在網站上看到此文，可電郵給我，我將附上檔案回信。

# 參考資料

[^1]: 270組是由Keng-Wei Wang et. al. (2021)提出的直方圖趨近連續概念，突破過去蒙地卡羅模擬最高25組或21組限制。