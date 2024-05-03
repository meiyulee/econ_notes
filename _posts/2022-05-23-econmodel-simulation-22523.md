---
title: 【經濟模型模擬系列】供需均衡模型
description: 
author: 李玫郁
date: 2022-05-23 16:23
categories:
 - 機率分配模擬器
tags: 供需模型
image: https://raw.githubusercontent.com/meiyulee/pic001/master/stat/exponential_dist_0001.jpg
layout: post
---

# 1. 前言

經濟學最基礎的模型為供給和需求模型。而存在市場均衡時，需求量=供給量=均衡量，此時價格不再是外生變數，並且消失在均衡量的公式。

那麼我們該如何為存在市場均衡的均衡量得到其機率模式呢？

# 2. 模型說明

給定市場價格為 $P$，適用於需求模型和供給模型。

## 2.1. 需求

假設需求量為 $Q_{d}$，非價格影響因素為 $X_{1}$，誤差為 $\delta_{d}$，我們可以列出需求模型為

$$
Q_{d} = \beta_{0} + \beta_{1} \, P + \beta_{2} \, X_{1} + \delta_{d}
\tag{1}
$$

式(1)中的 $\beta_{i}, i = 0, 1, 2$ 為需求模型的係數。 $\beta_{1}<0$。

## 2.2. 供給

假設需求量為 $Q_{s}$，非價格影響因素為 $X_{2}$，誤差為 $\delta_{s}$，我們可以列出需求模型為

$$
Q_{s} = \alpha_{0} + \alpha_{1} \, P + \alpha_{2} \, X_{2} + \delta_{s}
\tag{2}
$$

式(2)中的 $\alpha_{i}, i = 0, 1, 2$ 為需求模型的係數。

## 2.3. 市場均衡

根據市場均衡要求 $Q_{d}=Q_{s}$，可得到均衡價格為

$$
P^{e}=\frac{\beta_{0}-\alpha_{0}+\beta_{2}\,X_{1}-\alpha_{2}\,X_{2}+\delta_{d}-\delta_{s}}{\alpha_{1}-\beta_{1}}
\tag{3}
$$

將式(3)代入式(1)，得到均衡數量為

$$
Q^{e}=\frac{\big(\beta_{0} + \beta_{2} \, X_{1} + \delta_{d} \big) \,(\alpha_{1}-\beta_{1})+\beta_{1}\big(\beta_{0}-\alpha_{0}+\beta_{2}\,X_{1}-\alpha_{2}\,X_{2}+\delta_{d}-\delta_{s} \big)}{\alpha_{1}-\beta_{1}}
\tag{4}
$$

此時式(4)內沒有價格變數了。

# 3. 數值模擬

根據式(3)，我們需要4個隨機變數，分別是兩個誤差和兩個其他因素。其他係數則直接設定特定常數。

![](https://raw.githubusercontent.com/meiyulee/pic001/master/econ/DSmodel_0001.JPG)

接下來，讓我們開始分別在I,K,L,M欄，模擬這四個隨機變數。為什麼X1和X2要放置在I欄和K欄是為了使用Excel的迴歸分析函數。

![](https://raw.githubusercontent.com/meiyulee/pic001/master/econ/DSmodel_0002.JPG)

再來就是根據式(3)計算J欄的均衡價格。最後計算H欄的均衡數量。

這裡的均衡數量可由式(1)或式(2)計算出，而不是使用式(4)。

# 4. 計算線性迴歸係數

有了數據自然就能夠計算線性迴歸分析的各種係數。而此時我們有兩條方程式，分別是需求線方程式和供給線方程式。

利用模擬數據，使用[**LINEST**](https://support.microsoft.com/zh-tw/office/linest-%E5%87%BD%E6%95%B8-84d7d0d9-6e50-4101-977a-fa7abf772b6d)函數得到係數表如下圖。

![](https://raw.githubusercontent.com/meiyulee/pic001/master/econ/DSmodel_0003.JPG)

| $\hat{\beta_{1}}$ | $\hat{\beta_{2}}$ | $\hat{\beta_{0}}$ |
| :----: | :----: | :----: | 
| $se(\hat{\beta_{1}})$ | $se(\hat{\beta_{2}})$ | $se(\hat{\beta_{0}})$ |
| $R^{2}$ | $se(\hat{Y})$ |
| ANOVA的 F 值 | 自由度 |
| SSR | SSE | 

# 5. 繪圖

有了數據後，自然就可以繪圖了。理論上均衡數量和均衡價格未必會隨著供給曲線的價量正相關，或需求曲線的價量負相關運行。所以可繪製出均衡價量關係圖，如下圖。

![](https://raw.githubusercontent.com/meiyulee/pic001/master/econ/DSmodel_0004.JPG)

在Excel上的優勢就是可以按【**F9**】改變隨機模擬值。另外，如果X1是所得，還能畫出恩格爾曲線。

# 6. 結論

機率分配模擬器不只是可以模擬各種的分配，後續的應用才是其發揮的最大效力。本篇文章使用經濟學的供需模型，並求得均衡價格，使其內化，使得均衡數量的公式中不會出現價格的符號。而這樣的模型架構就能夠使用模擬數據的方式呈現出來。

另外，模型中的四個隨機變數都使用各自獨立的亂數生成模擬值，所以並不會有如實際情況發生相互干擾可能。

至於，迴歸分析的係數結果能體現出是否這樣的數據能夠使用一般的線性迴歸分析(OLS)，或者該改用2SLS法。

我提供的模型設計存在其他因素的X1和X2，想嘗試的朋友則可以簡化，只剩下誤差，並改變誤差的分配，觀察均衡價格和均衡數量的變化。

