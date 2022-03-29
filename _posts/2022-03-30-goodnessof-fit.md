---
title: 如何找出一組數據的來源 - 已知機率分配的適合度檢定
description: 讓我們找出數據的機率分配，而這個尋找方法必須連機率分配的參數一同找出來，才是完整的機率模型。
author: 李玫郁
date: 2022-03-30 01:24:50
categories:
 - 大數據分析
tags: [機率分配, 數據來源]
image: 
layout: post
---

# 1. 前言

我前面已經寫了如何做《[45種機率分配的適合度檢定]()》，這種方法可以讓我們的數據從45種機率分配中檢定出合適且知道參數的機率分配。不過，有時我們可能只需要知道數據的機率分配對應的參數為何，這篇文將說明第二種的適合度檢定：已知數據的機率分配，參數未知的情況。

<img src="https://raw.githubusercontent.com/meiyulee/pic001/master/stat/GOF_016.JPG" width="400">

準備好數據，打開軟體到上圖的選單畫面後，鍵入【**2**】後，點擊【end】上方的圓點。

<img src="https://raw.githubusercontent.com/meiyulee/pic001/master/stat/GOF_017.JPG" width="400">

點擊【是】後，繼續下一步。

<img src="https://raw.githubusercontent.com/meiyulee/pic001/master/stat/GOF_018.JPG" width="400">

此時，我們因為已知機率分配(前篇已經測定出是代號31的機率分配)，不過使用其他軟體檢定出來的機率分配可能沒有這些分配，所以我選擇代號2的機率分配。

鍵入【**2**】後，點擊【end】上方的圓點後會跳出下圖。

<img src="https://raw.githubusercontent.com/meiyulee/pic001/master/stat/GOF_019.JPG" width="400">

點擊上圖的【是】後，繼續下一步，運算適合度檢定。

<img src="https://raw.githubusercontent.com/meiyulee/pic001/master/stat/GOF_020.JPG" width="400">

運算適合度檢定完成後，跳出視窗顯示下圖的最佳結果。

<img src="https://raw.githubusercontent.com/meiyulee/pic001/master/stat/GOF_021.JPG" width="400">

完整的運算結果儲存在 *C:\建模軟體\輸出\statistic_output.txt*。

<img src="https://raw.githubusercontent.com/meiyulee/pic001/master/stat/GOF_023.JPG" width="400">

我們打開儲存的檔案就可看到上圖。由於我認定是常態分配，但參數未知，所以經過適合度檢定後，可以找出最小的卡方統計量數值對應之參數，分別為 $\mu = 65.846792$ 和 $\sigma = 17.367713$。

不過，一般羅吉斯型I分配的數據並不符合常態分配，P值 = 0.000131 < 0.05，拒絕虛無假設。我認定的常態分配，即使適合度檢定出最佳的參數也不是數據的機率分配。
