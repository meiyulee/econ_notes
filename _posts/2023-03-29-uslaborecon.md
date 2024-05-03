---
title: 趨勢圖解美國勞動市場指標
description: 如何做到圖解趨勢？趨勢建立需要精準的數字建模，所以使用MathGPT for numerical modelling (lines combined method)軟體幫助使用者的數字能夠建立精準的數學模式。方法優勢來自多線段法的使用。多線段法源於傳統迴歸分析，但不同之處在於多線段法將迴歸線的樣本數內化決定，自然能為數字配適出最優解。為美國勞動市場指標建立趨勢有什麼意義呢？原先美國的時薪和勞動產出率數據被經濟專家以時間序列方式做比對和解說，但作者認為兩數據皆為美國勞動指標，應該直接分析兩者的關係，至於各自的時間趨勢，則可互相告知我們美國勞動市場的情況。
categories:
 - 經濟趨勢
date: 2023-03-29 10:29
tags: [圖解觀念,勞動市場]
thumbnail: https://raw.githubusercontent.com/meiyulee/pic001/master/econ/laborecon_1.png

---

# 數據來源

價格指標：Nonfarm Business Sector: Hourly Compensation for All Workers  (COMPNFB)

數量指標：Nonfarm Business Sector: Labor Productivity (Output per Hour) for All Workers  (OPHNFB)


# 數據說明

|名稱 | 時薪(Y) | 勞動產出率(X) |
| ---- | ---- | ---- |
| 代號 | COMPNFB | OPHNFB |
| 頻率 | 季資料 | 季資料 |
| 單位 | 數字 | 數字 |
| 季節 | 有季節調整 | 有季節調整 |
| 期間 | 1947年第一季到2022年第四季 | 1947年第一季到2022年第四季 |
| 筆數 | 304 | 304 |

# 趨勢圖

![](https://raw.githubusercontent.com/meiyulee/pic001/master/econ/laborecon_1.png)

![](https://raw.githubusercontent.com/meiyulee/pic001/master/econ/laborecon_3.png)

![](https://raw.githubusercontent.com/meiyulee/pic001/master/econ/laborecon_2.png)


# 趨勢說明

- 方法  
  直線多線段法。每條趨勢線保持最佳解釋，每條直線函數配適得到解釋力，直到額外增加之數字導致解釋力下降，即重新新的趨勢線。

## 勞動產出率對時薪的關係 

- 每條趨勢線訊號
  - 共34條趨勢線


line 1, 23.258000<=X<=24.919000, sorting order= 1 ~ 10, data number=10,
> The estimated line Y=-4.661619+0.362887*X, R2=0.701479,

line 2, 25.377000<=X<=27.747000, sorting order= 11 ~ 19, data number=9,
> The estimated line Y=-3.155610+0.293345*X, R2=0.845043,

line 3, 27.777000<=X<=28.956000, sorting order= 20 ~ 30, data number=11,
> The estimated line Y=-7.850796+0.468835*X, R2=0.906840,

line 4, 29.479000<=X<=30.399000, sorting order= 31 ~ 36, data number=6,
> The estimated line Y=-8.199839+0.474070*X, R2=0.401639,

line 5, 30.502000<=X<=30.940000, sorting order= 37 ~ 42, data number=6,
> The estimated line Y=-51.285346+1.878931*X, R2=0.806484,

line 6, 30.954000<=X<=32.710000, sorting order= 43 ~ 49, data number=7,
> The estimated line Y=-1.912080+0.277275*X, R2=0.916467,

line 7, 32.964000<=X<=33.407000, sorting order= 50 ~ 56, data number=7,
> The estimated line Y=-12.145122+0.591233*X, R2=0.371633,

line 8, 33.734000<=X<=37.703000, sorting order= 57 ~ 67, data number=11,
> The estimated line Y=-0.705567+0.245085*X, R2=0.974159,

line 9, 37.730000<=X<=40.778000, sorting order= 68 ~ 78, data number=11,
> The estimated line Y=-2.779574+0.298096*X, R2=0.920134,

line 10, 40.928000<=X<=41.839000, sorting order= 79 ~ 84, data number=6,
> The estimated line Y=-27.501779+0.901342*X, R2=0.911912,

line 11, 42.774000<=X<=43.122000, sorting order= 85 ~ 90, data number=6,
> The estimated line Y=-75.624703+2.023253*X, R2=0.239249,

line 12, 43.173000<=X<=44.351000, sorting order= 91 ~ 96, data number=6,
> The estimated line Y=-59.868611+1.638825*X, R2=0.815477,

line 13, 45.245000<=X<=47.027000, sorting order= 97 ~ 102, data number=6,
> The estimated line Y=-9.798558+0.502709*X, R2=0.809972,

line 14, 47.289000<=X<=47.925000, sorting order= 103 ~ 108, data number=6,
> The estimated line Y=-30.472965+0.967217*X, R2=0.040818,

line 15, 48.041000<=X<=51.492000, sorting order= 109 ~ 124, data number=16,
> The estimated line Y=-66.662705+1.706005*X, R2=0.802138,

line 16, 51.770000<=X<=52.297000, sorting order= 125 ~ 131, data number=7,
> The estimated line Y=343.587250+-6.113771*X, R2=0.213917,

line 17, 52.303000<=X<=52.435000, sorting order= 132 ~ 137, data number=6,
> The estimated line Y=2443.475906+-46.125172*X, R2=0.315941,

line 18, 52.502000<=X<=53.117000, sorting order= 138 ~ 143, data number=6,
> The estimated line Y=-56.576636+1.634044*X, R2=0.012659,

line 19, 53.310000<=X<=60.520000, sorting order= 144 ~ 172, data number=29,
> The estimated line Y=-65.178602+1.804011*X, R2=0.968135,

line 20, 61.061000<=X<=65.433000, sorting order= 173 ~ 187, data number=15,
> The estimated line Y=-41.101027+1.439681*X, R2=0.953633,

line 21, 65.454000<=X<=67.122000, sorting order= 188 ~ 197, data number=10,
> The estimated line Y=-82.884764+2.069099*X, R2=0.937299,

line 22, 67.775000<=X<=74.312000, sorting order= 198 ~ 211, data number=14,
> The estimated line Y=-32.663519+1.321055*X, R2=0.979244,

line 23, 75.130000<=X<=79.661000, sorting order= 212 ~ 220, data number=9,
> The estimated line Y=-32.628609+1.336335*X, R2=0.765764,

line 24, 81.304000<=X<=86.513000, sorting order= 221 ~ 229, data number=9,
> The estimated line Y=-1.130231+0.921706*X, R2=0.988097,

line 25, 87.173000<=X<=89.430000, sorting order= 230 ~ 236, data number=7,
> The estimated line Y=-56.223003+1.566870*X, R2=0.894493,

line 26, 89.737000<=X<=90.730000, sorting order= 237 ~ 242, data number=6,
> The estimated line Y=-294.305602+4.233201*X, R2=0.794051,

line 27, 91.661000<=X<=93.079000, sorting order= 243 ~ 248, data number=6,
> The estimated line Y=-82.285515+1.887280*X, R2=0.534014,

line 28, 93.670000<=X<=99.036000, sorting order= 249 ~ 254, data number=6,
> The estimated line Y=16.792951+0.804110*X, R2=0.681308,

line 29, 99.055000<=X<=100.026000, sorting order= 255 ~ 262, data number=8,
> The estimated line Y=-339.716869+4.398153*X, R2=0.443286,

line 30, 100.036000<=X<=101.126000, sorting order= 263 ~ 269, data number=7,
> The estimated line Y=-338.601085+4.374138*X, R2=0.370713,

line 31, 101.309000<=X<=103.537000, sorting order= 270 ~ 280, data number=11,
> The estimated line Y=-271.535003+3.698636*X, R2=0.863639,

line 32, 103.571000<=X<=106.823000, sorting order= 281 ~ 289, data number=9,
> The estimated line Y=-191.111419+2.909995*X, R2=0.982317,

line 33, 107.492000<=X<=112.785000, sorting order= 290 ~ 295, data number=6,
> The estimated line Y=-381.705259+4.656591*X, R2=0.980611,

line 34, 112.978000<=X<=115.372000, sorting order= 296 ~ 304, data number=9,
> The estimated line Y=272.501494+-1.188696*X, R2=0.048221,

- 整體估計結果
  - 時間序 1 ~ 304
  - R2 = 0.999018
  - 整體資料分割成34線,
  - 每條分割線樣本至少6資料個數

## 時薪趨勢

- 每條趨勢線訊號
  - 共37條趨勢線

## 勞動產出率趨勢

- 每條趨勢線訊號
  - 共34條趨勢線

詳細的方程式，請參考 [連結](https://github.com/meiyulee/leetalk/blob/master/_files/OPHNFB_20230320.xls)

# 觀點

由於時薪和勞動產出率皆為勞動市場的指標，各自為價格和數量指標。如此一來就能對二指標尋找其關係。而美國的勞動產出率介於112.978000到115.372000的最高區間時，對應的時薪反而是下降的，並且平均每季下降-1.188696單位的時薪指數。

讓我對應勞動產出率的季度，發現都落在2020年第四季後。而美國高科技的裁員潮並非對勞動市場沒有影響，可以說美國看似失業率下降，但就業人員恐怕以普通薪資為主，導致高薪的裁員讓勞動產出率和時薪發生負斜率的趨勢情況。

從時薪的時間走勢來看，最新趨勢從2020年第二季開始，並且上升的斜率代表平均每季增加1.478591單位時薪。雖說美國因新冠肺炎的勞動運用上不如疫情前，隨著疫情緩和並不再被認為是「疫情」，而讓勞動力回到市場上。然而，同樣依賴國際貿易的美國也不免有物資的匱乏，導致物價上漲，和名目薪資需要上漲。

時薪的殘差更是呈現了愈接近現在，波動愈大。這代表美國的時薪數據隨著時間愈發不穩定。或許我們可以視為虛假的膨脹。

勞動產出率的時間走勢同樣也能得到高配適結果，最新趨勢從2020年第二季開始，但下降的斜率已然說明美國的勞動產出率並沒有因新冠疫情而復原!!!

