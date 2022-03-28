---
title: 大數據分析軟件介紹
description: 
author: 李玫郁
date: 2017-08-06
categories:
 - 大數據分析
tags: [軟體]
image: 
layout: post
---


大數據這個詞彙包含兩個部份，一個是『蒐集資料』的平台。這是目前大數據的主軸，用平台建立的方式蒐集資料，然後平台公司就可以將資料進行商業行為。現在的大數據一詞也是只這一塊領域。

至於，另一部份是指大數據分析。當資料蒐集完成後，資料必須要分析，才能有價值。而想要分析就需要有方法，現階段最常聽到的就是『數據用統計來分析』，以及『因為量大到趨近母體，所以可以只顯示而不檢測』，於是，使用視覺化展現，或是敘述性統計的係數顯示即可。抑或是採用歸納分類就能夠展現出來。
事實上，統計學從來就沒有處理過大量資料，因為統計學就是以少看多，用樣本看母體的概念。因此，統計學分析方法就是建立一些檢測的方式，由樣本去推估母體的特性。

既然要產生檢測方法，就需要一個標準，才能產生公式，方便使用，甚至寫入軟件，讓使用者運用電腦來進行分析與產生報表，解讀報表內容。這個標準就是『常態分配』！統計學所使用的樣本具有累加性，在經過數學組合後，就會有常態分配的特性，所以樣本在符合三個假設下，經過數學組合而有常態分配特性，進而產生公式，這包含估計與檢定。

對於大數據分析而言，其理論基礎與公式可以由統計學的理論開始，但是在量大時，將會產生其規則，甚至資料可以是來自於任何一種機率分配，不受到任何限制。因此，對於大數據的資料來說就會有以下的特性：

- 量大且雜亂，所以不需要符合常態分配，任何分配皆可。
- 大數據資料同樣需要被檢測，而檢測方法亦可根據統計學方法進行。
- 大數據資料具有規則性，可以由資料進行探勘後得到數學模式或規律。

就因為大數據分析具有上述特性，所以想要使用統計學方法進行驗證時，需要了解當資料量由少變多時的統計公式規律為何，進而推估，了解資料的機率分配為何，然後再由進行資料規律的模擬與預測。

目前大數據分析軟件已經免費上架在Github，而不使用DLL的套裝軟件則是放在package_software.md。

免費版的軟件包含說明文件、程式、源碼；套裝軟件則是包含說明文件與程式。免費版的軟件僅能輸出報表結果，並未有圖形顯示，讓使用者了解資料的機率分配模式，以及規律模式。圖形才能真正讓使用者知道資料的特性，而非特定一兩個係數的檢測來確定資料的機率分配。若有需要購買完整版大數據軟件，可關注『Psccc_機率與統計』紛絲專頁。