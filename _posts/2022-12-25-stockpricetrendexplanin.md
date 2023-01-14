---
title: 如何解讀股價趨勢
description: 當你看到真正的股價趨勢時，該怎麼解讀呢?對背後的數學，或者跑出來的數學結果，多數人都沒什麼興趣。最感興趣的是圖出來後怎麼解讀。今天就用臉書股價做出趨勢逐一解釋。
categories:
 - 股票分析
date: 2022-12-25 18:16
tags: [股價趨勢]
thumbnail: https://blogger.googleusercontent.com/img/a/AVvXsEjBgvomBbasUdy1RaH16q9UDfSeMkxsMx0PSPlzZJD_tpU1CkH9sAMzE4juXKuhC3Qr8BduTsrrtVZ9P3ZXg6mpYj5labY5WVjIS-J__o4sd-SfZFuQLxUsmtRAm0dQIyajXEtDTcLuZw7nXQlnEc7vQm9O1-ZtBV4bCy5q1HwTkvsxGqlmBCm694MO=w640-h388
layout: post
---

*你有想過看到趨勢後，該怎麼解讀呢？*

我們最簡單的趨勢表現法，就是直線。不過，人為習慣使得在認定某段時間內的數據後，就以全體數據進行估計。然而，這樣認定的數據範圍所得到的估計結果，未必是數據最合適的結果。

你們會認為數據怎麼會有最合適的結果，還不到是人為在決定的。然而在大數據和人工智慧時代卻非如此。人力難以處理龐大、雜且亂的數據，甚至少量、雜且亂的數據都難以處理。那麼問題出在哪呢？

讓我們重新回到人類處理數據時的過程，在對待數據的範圍時總由人決定，而非**數據自己決定**。我想這點是非常重要的，甚至是當我們踏上大數據和人工智慧時代時，對待數據該有的態度，那就是：該還權給數據，由數據自己決定，由數據自己說話。不加入過多的人為因素在其中主導數據該呈現的特徵。

這篇文章延續近期的分享內容，從高中所學的數學方程式、大學所學的統計學迴歸分析和微積分，到大數據和人工智慧的數據建模，讓我們重新看待所學的知識，和其應用。

數字說話的趨勢線是指由數字自己如同人類一樣，增加數字時，重新計算估計式，直到最佳條件達到，即代表最適合這數字群的估計式。

如此一來，我們就會看到每個估計式都會有一段趨勢線，並且兩個估計式造成的數字群在時間數列上就會有斷點。

我們需要認真對待這個斷點的位置，因為它代表前一個趨勢的結束，新的趨勢開始。數字無法告訴我們原因，但能顯示就那時間點！而我們依賴這樣的訊號，進行決策。

## 臉書META股價趨勢

![](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEixzp8BC0sFiEfozpWhgYAE79LqcZR0L68gZ1C1cjDId7aZNiNd4lBV6_bWtejsA7H-hedpWE_aHV59H4lw8Wfmc5WDndlBAQqu7rbmEFbWlMPV8ZCwa-8W33h-9x4WsBNaMQqVM1SjjwliXPvRCqnodexsp5jE_epmE0D45pKuX9zLhzXWrlcjvj04/w640-h360/%E8%87%89%E6%9B%B8-%E5%B0%81%E9%9D%A2.jpg)

圖一 

上圖是更新至2022年12月23日的一個月臉書每日股價。由每日股價建立最佳的趨勢線。因為需要至少10日數據進行估計，所以第一條線發生在13筆數字，最後一筆數字為11月23日(時間代號=254)。請看下方圖，紅色點為估計點，紅線為估計線，藍點為實際收盤價。水平軸是時間序，縱軸是價格，正上方顯示加入的點和收盤價數字。

![](https://blogger.googleusercontent.com/img/a/AVvXsEjBgvomBbasUdy1RaH16q9UDfSeMkxsMx0PSPlzZJD_tpU1CkH9sAMzE4juXKuhC3Qr8BduTsrrtVZ9P3ZXg6mpYj5labY5WVjIS-J__o4sd-SfZFuQLxUsmtRAm0dQIyajXEtDTcLuZw7nXQlnEc7vQm9O1-ZtBV4bCy5q1HwTkvsxGqlmBCm694MO=w640-h388)

圖二

圖三顯示繼續加入新的數字，11月25日的收盤價，計算估計式，得到估計線。單看圖三，你會認為和圖二差不多。但我們堆疊起來(見圖一)後，你可以看到第二條線的斜率變平了。

![](https://blogger.googleusercontent.com/img/a/AVvXsEgBNVgolkIOsR3a3S8QkR-YwyGnyKD1IGjYsnGiABLGXZiDJwZvd4A61yUVeu73MAzE72QWazs5Hk-D_-Lm7e_QW2zlbYj-s2JQrUHCfvDQsAPYXkbuvvnrKXiLYOzNS68XCxNopq88cvnC3SNUEPxBurdxqqlt_ua5Kevyi9mOtTr1Hza2H8T9dMhE=w640-h388)

圖三

![](https://blogger.googleusercontent.com/img/a/AVvXsEgjKWtQ9pB4cg0n7zdsw_S_iQytPBtYtl_mnN8pnLnk3nEJDY7Sl_S6t8EFHhbHggYhIR6silRnd8D2XJFVQNU6xmvq--pncXpZpbTDdtWvsfLSjlWZe3YBtdG4LWa6ycsZn7Cn42e8HMfnYnpxKm87FPjP626VlQxFAfaFOA-Bb9kFUrVwB0pS1P73=w640-h388)

圖四

加入第三個新數字(11月28日，週一，圖四)後，我們看到了整個趨勢重新開始，還就以11月28日為最後點，往前推4個數字，建立出最佳的估計線。而且你還看到這條估計線變成向下趨勢。這代表著11月28日的臉書股價正式破壞了前面的趨勢，重新起算，至於能維持多久就得看未來的數字。

![](https://blogger.googleusercontent.com/img/a/AVvXsEjjq21hxC60vhDOnJgoJl8mf9h8Oemk7gvaPnCjmnMqq6zy5oLte2-9a82pjA-VhtdaLq69FXY1o3sDbPjPlI8qnPYChL2J8r4TYlLmcnVwx2E_TFMfa8gbSCms7rUX6kSNq63eTPGa-_e8PF_fCR-WjWj3sm2SnEC02db_9LR_PEAwV3VOfRIqmExq=w640-h388)

圖五

到了11月29日的臉書收盤價出爐後，這條趨勢線並沒有改變趨勢(圖五)。但11月30日(圖六)的臉書收盤價加入後，再次扭轉趨勢線，重新開始。並且後續持續向上趨勢。

![](https://blogger.googleusercontent.com/img/a/AVvXsEhY-4r39N0phBIs8wkloI-6PdBPiQogTCrTNE63ryhkvbAP7SWD96y5__3GiJNl9wnn0GYq4demLbfwH5zyo_EbTa7SagkBR9E-UJKIrrbcskWYnhZDCOWwhl-ddN2RYKKwANiKSxhWlkSw2DZyxbjy28g3nhM-sanbNg3pNohqvMBS8J_fnoKPHsSD)

圖六

其實觀察圖一時，你會發現加入特定點的數字後，趨勢會改變，此時就是投資策略可能需要重新思考。再次趨勢改變時，又是另一個開始。

## NASDAQ指數趨勢

通過相同期間內的股價指數數字，可以發現個股的股價趨勢變化和股價指數很像，但股價指數反轉的速度非常快，也更快反應整體的美國科技股情況。

![](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEjVg5zlOW03H2Sn__uYzO2XZwYXDqByuu1-tWSVchM6WYcbRfgZA8SHRYJXRXQwNQuQcWZ8yP2iBS-XGDRvqJPM9QqWc2n-hvahe8i-8N-euLEhcugTICq-E6vIEFMlCjQlwcUJ6l9_6XofrhrOMwkhxsCv4RENOKbkCpXop_0MkBDwmWZWahe7hIsd/w640-h360/%E9%82%A3%E6%96%AF%E9%81%94%E5%85%8B-%E5%B0%81%E9%9D%A2.jpg)

納斯達克指數的第一條趨勢線含17日的收盤指數。11月25日收盤指數加入後形成斜率變緩的上升線。11月28日收盤指數加入後，重新開始新的趨勢線，並且變得更加水平。11月29日收盤指數又產生新的趨勢線，同時變成向下趨勢。
11月30日收盤指數加入後再次改變成向上趨勢。12月05日收盤指數加入後，上升趨勢卻趨緩，即使12月06日收盤指數雖然也是上升趨勢，更讓趨勢線變平緩。12月07日呈現水平線，12月08日轉為向下趨勢。即使12月12日再次改變成向上趨勢，但可預見是高檔下降的暫時性上升。其後變向下趨勢。

## 小結

觀察趨勢是持有股票期間成為買賣點的重要訊號。而投資過程中，多數投資課程或達人在談的都是如何選股。但當你確定要某檔股票後，持續觀察就需要了解股價趨勢。至於如何看股價趨勢，從過去高中和大學的學習知識中建立了解直線代表趨勢的意義和方法，並從其直線改變的斜率和時間斷點，了解股價趨勢變化和規律。
