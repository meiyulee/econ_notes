---
title: 為什麼機器學習都把數據估計結果稱為預測值
description: 告訴你為什麼現在都把統計的估計值叫做預測值
author: 李玫郁
date: 2022-03-26
categories:
 - 大數據分析
tags: [圖解觀念, 機器學習]
image: 
layout: post
---

現階段大數據和人工智慧已經將統計學的估計值稱為預測值，讓人容易搞混預測的意義。

大數據和人工智慧所指的是基於有前後次序才能做下一個的預測。這是現階段主要在討論的數據類型。這類的數據在每個節點都可以被當作一個起點，產生下一個節點的預測。這是既有的數據變數找出來的通則，而非另一種有時間序特性的數據所需要的下一期預測(Forecasting or prediction)。

另一種數據類型是具有時間序特性，所以預測是指在樣本集之外的點，稱為預測值。

![](https://raw.githubusercontent.com/meiyulee/pic001/master/slog/ML_predicted_value_estimated_value.jpg)


