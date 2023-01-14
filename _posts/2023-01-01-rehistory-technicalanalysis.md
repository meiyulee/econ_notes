---
title: 如何驗證技術分析說過去歷史會重演
description: 技術分析的理論基礎是股價趨勢歷史會重演，但股價趨勢如何找，又如何表現呢？難道平滑化折線圖就能代表股價趨勢嗎？事實不然。在現有的趨勢成像上存在一些問題，這篇文章將主要的問題一一做說明。
categories:
 - 股票分析
date: 2023-01-01 00:57
tags: 股價趨勢
thumbnail: https://blogger.googleusercontent.com/img/a/AVvXsEjoio6xpxZln365URw0TozCZckbz4fNlqOYFjasOYk50uGmoOOaF6ksr8a6JXgzUX046D5wLfhaSO1xTv-O93Jd2-At1cOG7FuUYqV9LeJTw1MlLPDTfSxvjVK8eKfMym3zEMsc-obHW71xMPFmsPYd6U5UpiM9HeOlM9KcianBXXKWuUtCCXhK_tIg
layout: post
---

技術分析是股市分析當中唯一依靠股價進行分析後，提供投資人的決策資訊。其基本信仰是建立在「歷史會不斷重演」的概念上，並試圖使用大量的統計資料來預測行情走勢。但是，技術分析主要所用的K線圖以分類方式，展現每日開高低收價的位置資訊。然而，這樣的「被動式」圖像方式並不能生成出「趨勢線」。

下面的Google簡報，在所有版面呈現台股指數開高低收價的趨勢。每增加一點就能生成一條新的趨勢線。讀者可以發現趨勢線新舊的比較，還能和過去的趨勢線做比較，發現軌跡改變。而右側呈現K棒。

## K棒不會有趨勢

你會發現，K棒呈現的開高低收資訊就只是當日的開高低收的位置，並且是一個垂直線的表現方式，也就是所謂的扁平化。但你沒辦法看到股價趨勢，同時你也看不到過去的情況。如果你要看到過去的開高低收，就是現在所見的K線圖。而這樣的K線圖並沒有「趨勢」。

<iframe allowfullscreen="true" frameborder="0" height="389" mozallowfullscreen="true" src="https://docs.google.com/presentation/d/e/2PACX-1vTLGbn3Jshws4yhMRD_SqQhcmC3HMnbN61dEUI0xp6_Ihc3NtEdUOfDE8n1nGHmrYx7SnOLxZbI1tzR/embed?start=true&amp;loop=true&amp;delayms=3000" webkitallowfullscreen="true" width="640"></iframe>

## K線圖如何呈現趨勢呢？

它是藉由轉換數字的方法，產生所謂的技術指標，特別是指移動平均(Moving average, MA)。換句話說，K線圖的K棒並不能呈現任何趨勢，自然也沒有預測性。但為了達到技術分析的目標，從18世紀開發並使用迄今的K線圖上可發現，所謂使用大量統計資料是指對收盤價進行轉換，也就是產生各種的技術指標。如此達到技術分析師的辨別金融市場上非隨機價格圖樣和趨勢。但究其根本，還是收盤價根據數學計算公式或統計學的計算公式得到的數字轉換。

多數的技術指標其實是靠比對或者時間差計算的數字**進行比對**，產生訊號。例如，MA10和MA20在特定一日比較，如果MA20 > MA10，稱為黃金交叉，成為買進訊號。這樣的比對方式並不是趨勢。

實際所見的MA20線，也只是將每日的MA20值用平滑線段連起來。但這樣的連線方式並未產生任何「趨勢」，而是透過圖像的線感，讓人類視覺發生看到趨勢的感覺。換句話說，該產生的趨勢或預測並沒有出現。而上述的比對方式只是決定買賣點的比對方法，同樣也沒有趨勢和預測。

## 趨勢從哪來

從過去我們所學的數學到大學的統計學，迴歸分析方法才能產生趨勢，也就是方程式加上誤差，不過，這方程式是由數字在最小誤差的條件下所產生。我們可以發現100%通過所有點，稱為方程式。如果是最小誤差得到的方程式，裡頭存在差距，可用R2表示趨勢的可解釋程度。

![](https://blogger.googleusercontent.com/img/a/AVvXsEgmbXZshmTYhCze57wbyhiJAbpYZY14g3QzHG70H-7kVRM18RbmOAnlSu1TufZxWJlUXqxoOELxqJCWAV4FMp-4Q8YMPusoGx7H5oSI2LC4cFATsjUpfd2uqTKm8htwOF2TWN3z7KLekIuxdD9IsbwkEOnEyRed7Om4PtU-rx9JcD4Uk_rpa0WH2fwD=w320-h194)

新加坡通貨膨脹率

一般來說，使用迴歸分析的慣性如上圖。由人決定好時間期間後，所有資料直接找出一條估計線。而我們看到這條估計線時，會認為在這段期間內，平均增長0.06%。但這條估計線是否最小誤差呢？當然，只要是由OLS得到的直線迴歸就滿足最小誤差特徵。然而，真如此嗎？
觀察上圖就能發現，藍色的直線估計線和實際值很多都有著很大的差距，而且實際值的趨勢未必可以用此直線估計線完全解釋，反而可能有「結構改變」。當然，此時可以使用Chow test測定是否存在結構改變。

### 直接由數字得到「結構改變」的最佳趨勢

如果我們能夠將數據配出最佳的趨勢線，那麼誤差必然小，對建模和預測都有好處。不過，我們得改變一個想法：「趨勢對應的數據量該由趨勢線自己決定」。我稱之為「<font color='red'>數據主動式</font>」，藉此區別前述的迴歸分析。前述常用的迴歸分析法稱為「<font color='red'>數據被動式</font>」。

於是，我們將上圖數據重新運算每增加一筆數據的估計線。如果估計線的可解釋程度變高，代表這新增加的數據就屬於這條估計線，反之，此新增加的數據就屬於新的估計線。

![](https://blogger.googleusercontent.com/img/a/AVvXsEjoio6xpxZln365URw0TozCZckbz4fNlqOYFjasOYk50uGmoOOaF6ksr8a6JXgzUX046D5wLfhaSO1xTv-O93Jd2-At1cOG7FuUYqV9LeJTw1MlLPDTfSxvjVK8eKfMym3zEMsc-obHW71xMPFmsPYd6U5UpiM9HeOlM9KcianBXXKWuUtCCXhK_tIg)

如此做就能得到上圖。上圖的趨勢線將此時間期間分成四個子時間區間。而斷點位置對應的日期代表當時發生足以影響趨勢改變的事件。

當我們能做到上圖的趨勢，並應用在股價/股價指數上，就成為技術分析想要找出的「趨勢」，同時因為這是迴歸分析的估計線，估計線是能計算預測值。

請注意，這邊的預測值是指未來時間的數字，也能是既有時間的估計值。這不同於目前常用的機器學習等所用的預測值概念。

## 趨勢也能從靜態走到動態

當我們能夠運算出最佳的趨勢後，自然能從上方的靜態圖，轉為動態圖。因為是時間的數據，自然能變成動態圖。然而，若只是表現出實際值的動態，這一點意思都沒有。若能同時展示趨勢，甚至是每增加一個新數據，產生一條新的趨勢線，那麼，我們就能做到「一點對應一條線」。從此，我們就能從「分類比對」的境地晉升為「數字趨勢」的精準程度。

![](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEiqSZOS1VHPdxAivAUac2xckCfXXBegE8wTIOgEpeLQgpzhpOGMJjfzWpEE_y-M_UbPw46tv_-02DHTIeObNe_i7UcYWis4fwRvBwfuLPVME9Gq2LhZxwMgirazrDFXx8SwdB1lI_mZqiDhVpUf8RbX1hHKwqloC5PEVT2HSvUBPlnLHqWEQ0NWcfhe/w640-h360/%E5%8F%B0%E8%82%A1%E5%85%A9%E6%99%82%E6%AE%B5%E8%B6%A8%E5%8B%A2%E5%8B%95%E6%85%8B%E6%AF%94%E5%B0%8D_%E5%A0%86%E7%96%8A%E5%BC%8F.gif)

## 歷史重演或者相似？

讓我使用趨勢動態模式和「趨勢+自相關」動態模式說明歷史股價/股價指數是否重演或相似。

29秒快速看完👉台股指數👈和👉台積電👈股價的趨勢動態情況📣只是相似趨勢💰直線多線段 + RNN核心的自相關技術

https://youtube.com/shorts/6dqbbBlaH40
30秒快速看完👉台股指數👈和👉台積電👈股價的趨勢動態情況📣只是相似趨勢💰非直線多線段 + RNN核心的自相關技術

https://youtube.com/shorts/TBLwfnOgNic

31秒快速看完👉台股指數👈和👉台積電👈股價的趨勢動態情況📣只是相似趨勢💰Curvilinear多線段 + RNN核心的自相關技術
https://youtube.com/shorts/lOL-43Gnhq4






