---
title: 如何找出一組數據的來源 - 一次45種機率分配
description: 讓我們找出數據的機率分配，而這個尋找方法必須連機率分配的參數一同找出來，才是完整的機率模型。
author: 李玫郁
date: 2022-03-29
categories:
 - 大數據分析
tags: [機率分配, 數據來源]
image: 
layout: post
---

# 1. 前言

很多人都想知道數據的機率分配是什麼。他們運用統計分析方法或現在主流的演算法找出數據的機率分配，不過，這些做法不是不完整，就是將數據轉換成log，變成常態分配，或變成準確度(accuracy)，試圖用一個母體比例形式來解讀。

我指的做法不完整是指機率分配檢定的方法。統計分析的適合度檢定或其他檢定數據的機率分配方法通常只檢定機率分配，不會顯示參數。這種統計分析結果讓我很疑惑，因為檢定分配時還要設定好參數，那如果那些檢定結果是正確的，就該顯示分配名稱和參數。

實際上，現行的主流軟體或程式檢定機率分配後並沒有顯示參數。參數的處理得到後面的統計分析，包含點估計、區間估計、假設檢定求得。因此，我才說這是不完整的方法，因為機率分配檢定需要連同參數一起進行檢定。

上面描述中，後者的數據轉換方法更得注意轉換後的數據能不能再轉回去，以及數據的機率分配是什麼也是轉換後的數據，而不是原始數據。甚至變成用新的數據(如準確度)去找機率分配也是很怪的。

那我們真的不能找出數據的機率分配嗎？其實是可以的！該怎麼做呢？

# 2. 適合度檢定+參數數值分析

想要找出數據的機率分配，除了機率分配檢定外，我們還要同時找出參數值。因為當我們執行機率分配檢定時，參數會影響機率分配的型態。所以機率分配檢定是檢定數據來自特定的「已先設定好參數的機率分配」。

機率分配的檢定是使用卡方檢定統計量的適合度檢定(Goodness of fit)。那我們怎麼同時做到參數設定呢？這時候需要數值分析生成參數的所有可能數值。接著，我們將所有可能的數值一個個做適合度檢定，

- 虛無假設：特定分配(參數值)
- 對立假設：虛無假設為假

得到卡方統計量值和P值。判斷方式為P值>0.05，無法拒絕虛無假設，我們即可認定數據來自特定參數的機率分配。

## 2.1. 你的機率分配檢定的分配種類足夠多嗎？

想要找出數據的機率分配需要足夠多的機率分配原型。因此我們需要「機率分配模擬器」獲得各種特定參數之機率分配的模擬值。之後會說明可以找出數據機率分配的軟體，內建45種機率分配的機率分配模擬器。

## 2.2. 人力無法計算完的特定參數之機率分配檢定

不過，每種機率分配需要同時設定好參數，所以每個分配的參數超過1萬個可能值。這些計算並無法人力完成，至於其他軟體，請讀者自行嘗試需要多久時間才能跑完。

# 3. 軟體操作

目前網上已經免費的軟體可以運算數據的機率分配，根據前述的適合度檢定應是檢定數據是否來自特定參數的機率分配的流程進行運算。

- [載點]()

## 3.1. 安裝方法

下載下來的是壓縮檔。解壓縮後，在C槽建立資料夾，命名為「建模軟體」。【注意】這邊都是繁體中文。如果你的Windows作業系統沒有支援繁體中文，那麼軟體跑的時候無法抓到這個繁體中文資料夾路徑。

解壓縮的檔案全部複製後，貼到 *C:\建模軟體* 資料夾內。資料夾內的執行檔為 *C:\建模軟體\改良式適合度檢定.exe*。

## 3.2. 執行過程

執行軟體前，數據需要先存成txt文字檔。如果原本數據在Excel，那就複製該欄數據，貼到txt文字檔。

點擊執行檔後，出現下圖。

<img src="https://raw.githubusercontent.com/meiyulee/pic001/master/stat/GOF_001.JPG" width="400">

能夠做機率分配檢定的數據量至少超過20個，可以達到1億筆。

點擊上圖下方的【確定】後，會跳出下圖，讓使用者選擇數據的檔案。這邊我的數據在 *Book1.txt*。
<img src="https://raw.githubusercontent.com/meiyulee/pic001/master/stat/GOF_002.jpg" width="400">

選好檔案後，按上圖的【開啟】後就會跳出下圖，確認你選擇的檔案。

<img src="https://raw.githubusercontent.com/meiyulee/pic001/master/stat/GOF_003.JPG" width="400">

點選上圖的【確定】後，跳出下圖告訴使用者，你的數據量有幾個。

<img src="https://raw.githubusercontent.com/meiyulee/pic001/master/stat/GOF_004.JPG" width="400">

點選上圖的【確定】後，跳出下圖，讓使用者選擇要運算的機率分配檢定。

1. 第一種是你對數據完全不知道來自哪種分配，在【selecting】右邊鍵入「**1**」。這個選項讓軟體為你的數據做45種機率分配的檢定。
2. 第二種適用已經知道數據來自哪種分配，但你不知道參數。
3. 第三種適用已經知道數據來自哪種分配和參數。

第二種和第三種可以參考圖片內的45種機率分配代號，下一步就會需要鍵入。

我在這邊選擇第一種適合度檢定，將檢定45種機率分配。

<img src="https://raw.githubusercontent.com/meiyulee/pic001/master/stat/GOF_005.JPG" width="400">

點擊上圖的【end】上方圓點後，就會跳出下方的數據敘述統計係數，先粗略了解數據特性。

<img src="https://raw.githubusercontent.com/meiyulee/pic001/master/stat/GOF_006.JPG" width="400">

點選上圖的【確定】後，軟體自行運算45種機率分配。

<img src="https://raw.githubusercontent.com/meiyulee/pic001/master/stat/GOF_007.JPG" width="400">

<img src="https://raw.githubusercontent.com/meiyulee/pic001/master/stat/GOF_008.JPG" width="400">

<img src="https://raw.githubusercontent.com/meiyulee/pic001/master/stat/GOF_009.JPG" width="400">

<img src="https://raw.githubusercontent.com/meiyulee/pic001/master/stat/GOF_011.jpg" width="400">

當軟體跑完後，會顯示如下圖的結果。我的1600個數據經過45個機率分配檢定後，P值=0.576996 > 0.05，無法拒絕虛無假設。可見數據為一般羅吉斯型I分配，並且參數分別為 $\mu=57.996188, \sigma=11.100309, \alpha=1.607195$。

<img src="https://raw.githubusercontent.com/meiyulee/pic001/master/stat/GOF_010.jpg" width="400">

跑完後會跳出通知軟體運算結束的提醒視窗。點擊【確定】後軟體就關閉。

<img src="https://raw.githubusercontent.com/meiyulee/pic001/master/stat/GOF_012.jpg" width="400">

那麼跑完的結果在哪呢？適合度檢定的結果儲存在*C:\建模軟體\輸出\statistic_output.txt*。

<img src="https://raw.githubusercontent.com/meiyulee/pic001/master/stat/GOF_013.jpg" width="400">

找到路徑位置後，開啟檔案，可得到下圖畫面。

<img src="https://raw.githubusercontent.com/meiyulee/pic001/master/stat/GOF_014.jpg" width="400">

跑出的結果會將45種機率分配的適合度檢定結果都儲存起來，任何一個結果都可以看得到。但45種機率分配顯示的都是該分配的所有可能參數中，最佳者。

<img src="https://raw.githubusercontent.com/meiyulee/pic001/master/stat/GOF_015.jpg" width="400">

上圖為捲動到txt檔最下方，可見到45種分配的最佳結果。

另外兩種適合度檢定，會在其他文說明操作過程。

