---
title: 趨勢圖解美國和英國菲利普曲線
description: 以1960年到2022年的失業率和通貨膨脹率(年資料)進行多線段法的直線模式，AI自主決定最佳的每線段最少數據量，得到美國和英國的菲利普曲線差異甚大。
categories:
 - 經濟觀點
date: 2023-03-19 12:23
tags: [圖解觀念]
thumbnail: https://raw.githubusercontent.com/meiyulee/pic001/master/econ/phillipscurve_US_UK_2022_year.png

---

# 數據來源

## 美國

- 失業率 Unemployment Rate: Aged 15-64: All Persons for the United States
- 消費者物價指數 Consumer Price Index for All Urban Consumers: All Items in U.S. City Average

通貨膨脹率由消費者物價指數與去年同期相比計算得到

## 英國

- 失業率 
  - Unemployment Rate in the United Kingdom (只到2016年)
  - Harmonized Unemployment Rate: Total: All Persons for the United Kingdom 
- 通貨膨脹率 Consumer Price Index: Total All Items for the United Kingdom, Growth rate previous period, Annual, Not Seasonally Adjusted

# 數據說明

|名稱 | US失業率 | US CPI | UK 失業率 | UK 通貨膨脹率 |
| ---- | ---- | ---- | ---- | ---- |
| 代號 | UNRATENSA | CPIAUCNS | UNRTUKA<br>LRHUTTTTGBA156N | CPALTT01GBA657N |
| 頻率 | 年資料 | 年資料 | 年資料 | 年資料 |
| 單位 | 百分比 | 百分比 | 百分比 | 百分比 | 
| 季節 | 沒有季節調整 | 沒有季節調整 | 季節調整 | 季節調整 |
| 期間 | 1960年到2022年 | 1960年到2022年 | 1960年到2022年 | 1960年到2022年 | 
| 筆數 | 63 | 63 | 63 | 63 |

# 趨勢圖

![](https://raw.githubusercontent.com/meiyulee/pic001/master/econ/phillipscurve_US_UK_2022_year.png)

# 趨勢說明

- 方法  
  直線多線段法。每條趨勢線保持最佳解釋，每條直線函數配適得到解釋力，直到額外增加之數字導致解釋力下降，即重新新的趨勢線。

## 每條趨勢線訊號

### 美國

| 線代號 | 失業率範圍 | 資料個數 | 估計線 | R2 | 
| :----: | ---- | ---- | ---- | ---- | 
| 1 | 3.56 ~ 4.93 | 16 | Y = 11.771861 - 2.078887 \* X | 0.323487 | 
| 2 | 4.95 ~ 5.67 | 15 | Y = 14.848165 - 2.151588 \* X | 0.087432 | 
| 3 | 5.68 ~ 7.10 | 16 | Y = 17.627767 - 2.186336 \* X | 0.107220 | 
| 4 | 7.13 ~ 9.86 | 16 | Y = 15.614765 - 1.320170 \* X | 0.118620 | 

- 整體估計結果
  - 時間序 1 ~ 63
  - R2 = 0.177806
  - MSE = 7.186833
  - 整體資料分割成4線,
  - 每條分割線樣本至少15資料個數

### 英國

| 線代號 | 失業率範圍 | 資料個數 | 估計線 | R2 | 
| :----: | ---- | ---- | ---- | ---- | 
| 1 | 2.07 ~ 4.5 | 21 | Y = -3.052813 + 2.623043 \* X | 0.151666 | 
| 2 | 4.56 ~ 6.81 | 20 | Y = -19.003168 + 4.388513 \* X | 0.165625 | 
| 3 | 6.98 ~ 11.77 | 22 | Y = 1.162819 + 0.367037 \* X | 0.050557 | 

- 整體估計結果
  - 時間序 1 ~ 63
  - R2 = 0.162338
  - MSE = 21.028132
  - 整體資料分割成3線,
  - 每條分割線樣本至少20資料個數
