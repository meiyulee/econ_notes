---
title: 從巨量資料分析方法找台日韓兌美元匯率機率密度函數
date: 2015-07-20 19:18
layout: post
tags: [匯率, 機率分配,強大數法則]
thumbnail: http://images.wisegeek.com/currency-exchange-rate-board.jpg
published: true
description: 
categories:
 - 大數據分析
---


<div style="text-align: justify;">
話說台灣是以出口為導向的國家，新台幣匯率的穩定與否與國際情勢深深地影響台灣出口狀況。所以在匯率相關文獻上，例如，王泓仁(<a href="http://www.cbc.gov.tw/public/Attachment/831211391271.pdf" target="_blank">2005</a>)使用結構式自我迴歸模型探討央行持有國外資產淨額變動率、銀行隔夜拆款利率、M2變動率、自然對數下之CPI、自然對數下之工業生產指數、新台幣兌美元匯率、外貿比例、貿易條件為內生變數進行匯率與其他變數關係討論，另外使用GARCH討論新台幣匯率成長率之波動。<br />
<br />

<!--more-->

蔡聰勇(<a href="http://nccur.lib.nccu.edu.tw/handle/140.119/35127" target="_blank">2006</a>)以ARCH模型分析日本央行干預日元兌美元匯率對新台幣匯率波動影響。何棟欽(<a href="http://www.cbc.gov.tw/public/Attachment/831818323571.pdf" target="_blank">2001</a>)則是建立誤差校正模型(ECM)，使用隔夜拆款利率、基本放款利率、存款利率與10年期中央公債次級市場利率，發現台灣央行的存放款利率調整無僵固性，短期利率傳遞至公債利率效果不佳，但長天期存款利率則較為理想。傅澤偉、黃國安、林曼莉(<a href="http://www.mnd.gov.tw/Upload/201412/06-3_%E6%96%B0%E5%8F%B0%E5%B9%A3%E5%85%8C%E7%BE%8E%E5%85%83%E5%8C%AF%E7%8E%87%E4%B9%8B%E6%A8%A1%E5%BC%8F.pdf" target="_blank">2014</a>)比較僵固型價格貨幣理論模型、資產組合平衡模型與行為均衡匯率模型，認為僵固型價格貨幣理論模型為佳。</div>
<br />
不過這些分析匯率之模型多仍建構在<br />
<ol>
<li>線性模型上，即使是GARCH模型也是一樣。</li>
<li>誤差是常態分配上。</li>
</ol>
<br />
事實上，在資料定序的基礎上，各國匯率不太可能是常態分配，即使解釋變數放入後的迴歸模型也是一樣。這不只是假迴歸問題，而需要從根本討論起。<br />
<br />
在巨量資料分析下，若選擇1779/1/1至2015/04/17期間的日資料，可發現新台幣匯率之機率密度函數是可以被找到的。<br />
<br />
<div class="separator" style="clear: both; text-align: center;">
<a href="http://1.bp.blogspot.com/-Hq9KrssdjUU/VazwRkXHtUI/AAAAAAAABLo/xJNwIFdp_74/s1600/%25E8%259E%25A2%25E5%25B9%2595%25E5%25BF%25AB%25E7%2585%25A7%2B2015-07-20%2B%25E4%25B8%258B%25E5%258D%25888.57.08.png" imageanchor="1" style="margin-left: 1em; margin-right: 1em;"><img border="0" src="https://1.bp.blogspot.com/-Hq9KrssdjUU/VazwRkXHtUI/AAAAAAAABLo/xJNwIFdp_74/s1600/%25E8%259E%25A2%25E5%25B9%2595%25E5%25BF%25AB%25E7%2585%25A7%2B2015-07-20%2B%25E4%25B8%258B%25E5%258D%25888.57.08.png" /></a></div>
<br />
左圖為日元兌美元匯率之機率密度函數圖、中間圖為韓元兌美元匯率之機率密度函數圖、右圖為新台幣兌美元匯率之機率密度函數圖。觀察圖形可知，<br />
<br />
<ol>
<li>從全距與變異數來看，新台幣兌美元匯率 &lt; 日元兌美元匯率 &lt; 韓元兌美元匯率</li>
<li>從偏態、峰態與變異係數來看，新台幣兌美元匯率 &lt; 韓元兌美元匯率 &lt; 日元兌美元匯率</li>
<li>從機率密度函數圖來看，台日韓匯率都有雙峰傾向</li>
<li>從特定匯率值出現機率來說，台灣有39.83%最大機率盯住特定匯率值、日本有3.87%最大機率盯住特定匯率值、南韓僅有0.58%最大機率盯住特定匯率值</li>
</ol>
<br />
南韓在外匯市場上的干預是最少的，這是起源於1997年南韓為了度過東南亞金融風暴而向IMF借款救經濟時，要求依據國際組織之外匯管制規範，不再高度干預外匯市場。因此，在匯率的機率密度函數圖表當中特別明顯可以看到這樣的結果。<br />
<br />
