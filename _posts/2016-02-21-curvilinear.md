---
layout: post
tags: [Curvilinear]
date: 2016-02-21 19:18
thumbnail: http://art.nmu.edu/groups/cognates/wiki/244d1/images/8d922.jpg
title: 為何使用曲線化線性模型
published: true
categories:
 - 大數據分析
---


當我們想知道資料特性或規律性時，傳統做法是根據統計學概念，認為資料=樣本，必然帶有母體特性。藉由資料找到母體參數即可確認母體特性，從而知道資料特性或規律性為何。

然而，受限在使用資料找到的母體參數卻是有限，例如，一定要找到一、二階動差，即平均數與變異數，如此就能配合樣本數找到極限分配，知道母體特性。在大數法則下，無論是p.或a.s.，都趨近為常態分配。

問題是多少資料點才能算大數？

這如同我們在問大數據多少才算？

如果4,000筆已經達到，那何必4,000,000,000筆資料。

這想法並非正確！

因為每筆資料都有存在的意義，而且，大數據資料下，未必真成為常態分配或極限常態分配。

<!--more-->

這點更明顯地顯示在時間序列資料，因為這種資料會破壞迴歸分析的三個基本假設：

- 常態分配
- 齊質變異數
- 兩兩無線性相關

為了解決這些問題，特別是像變數之走勢，無法用線性模式去估計的序列資料，計量經濟學發展出多種的檢定公式，檢定上面的三個基本假設，並且希望更能準確地找出資料問題，試圖解決。

縱使如此，我們卻發現

1. 分配的檢定方法無法控制誤差，資料的殘差幾乎可以滿足常態分配
2. 變異數的齊一性建立在線性迴歸上，誰能保證資料一定是線性，特別是工業工程。若是用非線性迴歸模型，或許變異數就齊質了。
3. 架構在線性迴歸模型上，序列相關運用差分方式，試圖找出差分到幾階才能踢除序列相關。可是，差分後的資料，部分特性將會消失。

更有趣的是，[Silverman (1985)](http://www.fasebj.org/content/1/5/365.full.pdf) 提出無母數版本的曲線配適法，觀察範例後可以發現其轉折點不能超過兩點，也可以從他的數學式看出，僅有二階微分。Motulsky and Ransnas (1987) 則是提到需要資料點來自於常態分配(進入迴圈：如何確定資料點滿足常態分配)，以及非線性迴歸模型很容易經過多次的電腦運算後配適得到(問題：怎麼進行誤差控制？多次的運算需要多少次？)。

無論如何，使用曲線化線性模型或曲線配適法都是比線性迴歸模型來得好，特別是現在的經濟環境在科技進步到一定的程度後，必須提高精準度，才能夠突破現況。這不是工業4.0(要求精密)、金融3.0(要求跨平台與安全)，而是分析技術的創新與提升。

於是，我們需要更新兩個思維：

**第一、一般而言，我們認為線性之外就是屬於變異(波動)。**

<table align="center" cellpadding="0" cellspacing="0" class="tr-caption-container" style="margin-left: auto; margin-right: auto; text-align: center;"><tbody>
<tr><td style="text-align: center;"><a href="http://i.stack.imgur.com/8RlJk.png" imageanchor="1" style="margin-left: auto; margin-right: auto;"><img border="0" src="http://i.stack.imgur.com/8RlJk.png" height="133" width="320" /></a></td></tr>
<tr><td class="tr-caption" style="text-align: center;">圖片來源:http://stats.stackexchange.com/questions/19102/is-there-a-graphical-representation-of-bias-variance-tradeoff-in-linear-regressi</td></tr>
</tbody></table>
<div dir="ltr">
<br /></div>


但是，當我們從非線性迴歸角度來看的時候，每一點進來模型時，就需要重新計算調整模型係數與次方數，降低均方差。每一點都是在學習，只是，這樣的學習方式比下方的學習模式好。
<div dir="ltr">
<br /></div>
<div class="separator" style="clear: both; text-align: center;">
<a href="http://4.bp.blogspot.com/--WWoxH4nUyc/TvQf64GO0dI/AAAAAAAADWY/MhulcDMTZfs/s400/hypothesis.png" imageanchor="1" style="margin-left: 1em; margin-right: 1em;"><img border="0" height="300" src="https://4.bp.blogspot.com/--WWoxH4nUyc/TvQf64GO0dI/AAAAAAAADWY/MhulcDMTZfs/s400/hypothesis.png" width="320" /></a></div>
<div dir="ltr">
<br /></div>
<div class="separator" style="clear: both; text-align: center;">
<a href="http://3.bp.blogspot.com/-UbXALHInZAc/TvQf7LG406I/AAAAAAAADWw/uxoTRaTOQEo/s400/learning_curve_variance.png" imageanchor="1" style="margin-left: 1em; margin-right: 1em;"><img border="0" height="137" src="https://3.bp.blogspot.com/-UbXALHInZAc/TvQf7LG406I/AAAAAAAADWw/uxoTRaTOQEo/s400/learning_curve_variance.png" width="200" /></a>&nbsp;&nbsp;<a href="http://2.bp.blogspot.com/-_SPyaixmkZo/TvQf7Ea3hgI/AAAAAAAADWg/1j1EEkMTlWA/s1600/learning_curve_bias.png" imageanchor="1" style="margin-left: 1em; margin-right: 1em;"><img border="0" height="103" src="https://2.bp.blogspot.com/-_SPyaixmkZo/TvQf7Ea3hgI/AAAAAAAADWg/1j1EEkMTlWA/s1600/learning_curve_bias.png" width="200" /></a></div>
<div dir="ltr">
<span style="font-size: xx-small;">圖片來源:&nbsp;http://digitheadslabnotebook.blogspot.tw/2011_12_01_archive.html</span></div>
<div dir="ltr">
<br /></div>
<div dir="ltr">

上方的學習模式是運用多次的假設檢定方法(決策法)得到演算公式，也就是迴歸方程式。而非線性迴歸模型應該是每加入新的資料點就要重新跑一次，得到的最小均方差才是此時最佳的迴歸方程式。這時，我們不需要特別去估計(或尋找)線性以外的波動程度，因為大部分的波動程度已經由曲線給捕捉了。

所以，線性 + 部分的變異 會形成曲線，剩下的變異則是來自於估計誤差所致。

**第二、趨近需要明確的誤差值代表。**

讓我們舉個最簡單的例子，有誰可以說出Z檢定表內每個臨界值的估計誤差？小數點後二位或後三位的臨界值有多準？

事實上，我們都是直接使用了，而誤差只是顯著水準為代表，查表的誤差卻沒有被考慮在其中，而將此視為系統性誤差(大家都使用，所以都存在這樣的誤差)。想想這樣的方式套用在經濟政策與財務策略上，真可謂差之毫釐失之千里。

於是，我們遭遇了次級房貸危機、全球金融海嘯、歐債危機、貨幣貶值，以及現在的歐、日負名目利率的情況。金融商品特別容易產生高槓桿效果，也就是高乘數效果。當初的一點小錯誤，在高乘數的加成後，形成了目前的金融情勢，帶動實體經濟的萎縮。所以，能夠解決這樣問題的方法就是提高精準度，明確表現誤差會發生在哪幾處，以及誤差有多大。

這些都是風險！我們沒道理去忽略，特別是財務、金融、經濟這些領域。這些領域的高層決策對整體環境影響非常大，今日沒發生，不代表未來不發生。看看雷曼兄弟的連動債，當初的設計是多麼完美，到最後，讓一間傳承百年的老字號就這麼倒了。

因此，當我們可以將變異數轉為平均時(由線性轉為非線性)，風險降低，同時精準度提高。

那麼，我們該怎麼進行呢？

過去，我們都認為趨勢是長期的結果，趨勢的表現方式就是直線。但是，在數學上，兩點連成一直線，這直線要精準的話，請問，兩點之間的距離應該是愈近愈好？還是愈遠愈好？

答案當然是愈近愈好，所以，當我們想用直線去估計眾多資料點形成的曲線時，最好的方式就是資料點距離愈短愈好，兩點連出來的直線就會愈往曲線去逼近(Silverman, 1985)。這也是微積分的觀念，兩點間的距離如果可以趨近於0，那麼找到的斜率就會愈準(微分法)。而積分就是在找規則，將所有斜率連起來就會形成軌跡。

所以，曲線化線性迴歸模型的特性有

1. 基於微積分的泰勒展開式觀念進行估計
2. 可解決線性迴歸問題，配適較好的凹折的資料
3. 可解決時間序列問題，用等差級數配適較好的曲線
4. 可以捉到起始點
5. 可以捉到最終點

限制則有

1. 無法解決序列相關問題
2. 樣本數最好超過4,000個
3. 沒有數學版的係數估計量
4. 只能用電腦運算(Motulsky and Ransnas, 1987) 



