---
title: Milletvekilleri Network Analizi 
date: 2020-06-20T14:51:12+06:00
image_webp: images/blog/mv.webp
image: images/blog/mv.jpg
author: Burak Özturan
description : "Burasi meta description"

---


Burak Özturan Dr. Onur Varol'la birlikte milletvekillerinin Twitter hesaplarının network haritasını çıkarttı. İttifaklar ve partiler arası ayrım sosyal medyaya da yansımış durumda.



## Araştırmanın Dizaynı 

1. 27.dönem milletvekillerinin listesi TBMM'nin sitesinden  ağ-kazıma (web-scraping) yordamıyla çıkartıldı. 

2. Ardından yine ağ-kazıma  kullanılarak milletvekillerinin twitter hesap adları, partileri, şehirleri ve takipçi sayılarıyla birlikte kaydedildi.

3. Milletvekillerinin (mv) twitter adları doğrulandıktan sonra, Twitter API ile MV'lerin takipçileri kaydedildi.

4. Takipçiler arası benzerlik (jaccard similarity) ile network haritasını çıkarttık.

## Sonuç

Görselde görülebileceği üzere partiler arası ittifak ayrımları (millet-cumhur ittifakı) sosyal medyadaki milletvekillerinin takipçilerine de yansımış durumda. Görselin sol tarafında turuncu renkte AKP'li ve mavi renkte MHP MV'leri; sağ tarafta ise açık mavi (cyan) renginde İYİP, kırmızı olarak CHP ve mor renkte HDP vekilleri görülebilmektedir. 


## Gelecek Çalışmalar

Bundan sonraki aşamada, network haritasını daha detaylı inceleyerek anomalileri ve  stratejik noktalara konumlarda olan vekilleri tespit etmeye çalışacağız. Ayrıca sosyal medyadaki bot hesapları tespit etmeye yarayan  "Botometer" kullanılarak yeni bir network haritasi çıkartıp burada çıkartmış olduğumuz network hariyasıyla karşılaştıracağız. Buradaki amaç sosyal bot kullanım pratiklerinin partiler arası değişip değişmedini incelemek olacaktır. 
