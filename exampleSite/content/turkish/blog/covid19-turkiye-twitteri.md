---
title: "COVID-19 Pandemisi Sürecinde Türkiye Twitter Analizi"
date: 2018-09-12T14:51:12+06:00
image_webp: images/blog/blog-post-2.webp
image: images/blog/blog-post-2.jpg
author: Burak Özturan
description : "This is meta description"
---



bir şeyler bir şeyler oldu sonra böyle böyle böyle

> Design is not just what it looks like and feels like. Design is how it works.

# COVID-19 Twitter Veritabanı: Türkiye Örneklemi

## Araştırmanın Amacı ve İçeriği

Bu veri seti çalışması, 2020 yılının ilk aylarından beri dünyada etkisini gösteren COVID-19 virüsünün Türkçe konuşan Twitter kullanıcılarının gündemine tesirini tespit etmek amacıyla kurulmuştur.  Bu çalışma halihazırda birçok dilde hazırlanan kapsamlı bir Twitter veri setinin [#COVID-19: The First Public Coronavirus Twitter Dataset](https://github.com/echen102/COVID-19-TweetIDs) tamamlayacısı olarak görülebilir. Böyle bir çalışmanın şimdiye kadar yapılmamış olması bizi motive eden önemli bir nedendir. Yukarıda belirtilen çalışmada ise kelime havuzunun dar olması ve temalara göre ayrılmaması, Türkçe tweet sayısının az olması, Türkçe tweetleri ayıklamaktaki zorluklar yeni bir veri seti çıkarmayı zorunlu hale getirmiştir. 

"COVID-19 Twitter Veritabanı: Türkiye Örneklemi" adlı bu çalışmada tweetler hem temalara göre ayrı ayrı elde edilmiş hem de açıklanan ilk vakanın öncesi ve sonrasındaki gündemler ayrı ayrı tespit edilmiştir. Araştırma, aynı zamanda, Türkçe yazan Twitter kullanıcılarının Ortadoğu ve Avrupa'da vakaların artmasıyla beraber koronavirüsü gündemlerine aldıklarını ve Türkiye'de ilk vakanın açıklanmasıyla birlikte hem dini hem ekonomik hem politik hem de dış ülkeler hakkındaki gündemlerinde kırılmalar olduğunu varsaymaktadır. Bu raporda, bahsi geçen kırılmaları göstermek için en çok geçen kelimeler üzerinden bir ön analiz sunulacaktır. 

## Araştırmanın Dizaynı

Aşağıda bu araştırmanın dizaynı, içeriği ve kullanılan kodlar özetlenecektir. Aynı zamanda, bu veri setini kullanarak yürütülebilecek gelecek çalışmalara bazı tavsiyeler sıralanacaktır. İlk olarak, anahtar kelimeler temalara göre çıkartılmıştır. Daha sonra, tarih aralığı belirlenip tweetler çekilmiştir. Elde edilen tweetler, Twitter'ın [Terms of Service](https://developer.twitter.com/en/developer-terms/agreement-and-policy) ile uyumlu olarak ID'ler halinde herkese açık olarak depolanmıştır. En sonunda ise programlamalı metin analizi teknikleri kullanılarak tweetler üzerinden temel çıktılar alınıp takdim edilmiştir. 

### Anahtar kelimelerin çıkarılması ve temalara bölünmesi

Temalar, COVID-19 tartışmaları döneminde muhtemel olarak etkilenen veya etkilenebilecek alanlar olan politika, ekonomi, din, dezenformasyon, dış ülkeler hakkındaki algılar, ve virüsün kendisi olarak belirlenmiştir. Bu 6 başlık altındaki anahtar kelimeler rastgele tweet araması yapılıp okuma yapılarak çıkarılmıştır:

  * COVID-19: Covid-19, Covid 19, Kovid-19, korona, koronavirus, virüs, corona 
  * Politika: Bilim Kurulu, Bakan, Başkan, Sağlık Bakanlığı, Savaş, Seferberlik, Barış Pınarı, Fahreddin Koca, Cumhurbaşkanı
  * Ülkeler: Çin, Avrupa, Amerika, İngiltere, İtalya, İspanya, Almanya, Fransa, Japonya, Güney Kore, İran, Türkiye, DSÖ (WHO), Nato, İsrail
  * Dezenformasyon: Asılsız, provakatif, sahte, provakasyon, palavra, komplo, oyun, büyük oyun,  siyonizm
  * Din: Diyanet, cami, Cuma, muska, din, ezan, sela, sabır, müsibet, musibet, 
  * Ekonomi: Kredi, burs, işsiz, işsizlik, nakit, destek, dayanışma, gıda, mücadele, memur, şirket, gümrük
  
### Verilerin Tarih Aralığının Belirlenmesi

  * Yukarıda belirtilen kelime havuzları iki tarih aralığı belirlenerek ayrı ayrı depolanmıştır. 
  * Türkiye'de ilan edilen ilk vaka 11 Mart tarihindedir. 
  * Verileri önce ve sonra diye iki ayrı şekilde ayırmamızın amacı, gündemlerdeki süreklilik ve kırılımların belirlenmesini kolaylaştırmaktır.
  * 11 Mart öncesi gündem, İran'da açıklanan ilk vaka tarihi olan 19 Şubat ile sınırlandırılmıştır. Buradaki amaç, Ortadoğu ve Avrupa bölgelerinde ilk vakaların açıklanmasını bir dönüm noktası olarak belirlemektir. 
  * Veriler 7 Nisan tarihine kadar çekilmiştir. Bu tarih Türkiye'de ilk vakanın açıklanmasından yaklaşık olarak bir ay sonrasına denk gelmektedir. 
  * Bu açılardan, bu dosyadaki veri seti ilk vakanın açıklanmasından önce ve sonraki gündem değişimlerini ve sürekliliklerini incelemeye imkan tanımaktadır.

### Verilerin Depolanması ve ID'lerin Çıkarılması

  * Twitter'ın [Terms of Service](https://developer.twitter.com/en/developer-terms/agreement-and-policy) ile uyumlu olarak toplanılan tweetlerin sadece Tweet ID'leri temalara bölünerek dosyalar halinde depolanmıştır. ID'ler çıkarılırken tekrar eden  tweetler temizlenerek her tema için özgün tweetlerden oluşan veri setleri oluşturulmuştur.
  * Bu ID'leri kullanarak çalışma yapmak isteyenler için [Hydrator](https://github.com/DocNow/hydrator) and [Twarc](https://github.com/DocNow/twarc) gibi araçları kullanmayı tavsiye ediyoruz. Detaylı talimatlar için linklerdeki açıklamalara bakılabilir. 

### Kullanılan Kodlar

Bu çalışma, temel olarak üç kod setine dayanarak yapılmıştır.
 * İlk olarak Twitter'dan veri çekebilmek için Python dilinde yazılmış [Twint](https://github.com/twintproject/twint) paketinden yararlanılmıştır.
 * Daha sonra, elde edilen verileri düzenlemek ve ID'lerini çıkarıp kamusallaştırmak işlemleri gerekli [kodlar](https://github.com/burakozturan/tria-covid19/blob/master/kodlar%20(codes)/data/data_birlestirme.ipynb) kullanılarak gerçekleştirilmiştir.
 * En son olarak, içeriğe dair ilk fikirlerimizi elde etmek için [programlamalı metin analizi kodları](https://github.com/burakozturan/tria-covid19/blob/master/kodlar%20(codes)/analiz/Covid_quantitative_text_analysis.ipynb)
kullanılmıştır.

## Temel Çıktılar

Bu bölümde ilk olarak tweetlerin temel istatistikleri sunulacaktır. Daha sonra, elde edilen tweetler üzerinden, ilk vakanın açıklanmasının öncesi ve sonrasında en çok geçen kelimeler veya anahtar kelimeler [tablolar](https://github.com/burakozturan/tria-covid19/tree/master/sonuç%20tabloları) halinde görselleştirilecektir. Önemli görülen devamlılık ve kırılmalar kısaca not edilecektir. Daha detaylı analizler bir sonraki çalışmanın araştırma konusu olacaktır.

### Temel İstatistikler
6 farklı temanın iki farklı zaman diliminde twitlerinin temel istatistikleri aşağıdaki gibidir:

Toplam Twit Sayısı : **4,369,870**

| **Tema**        | Önce          | Sonra            | **Toplam**         |
|-------------    |-----          |------------      |----------------    |
| COVID           | 161,109       | 1,427,569        | 1,588,678          |
| Politika        | 355,992       | 367,992          | 723,984            |
| Dezenformasyon  | 51,521        | 88,007           | 139,528            |
| Din             | 215,699       | 436,309          | 652,008            |
| Ekonomi         | 19,532        | 74,682           | 94,214             |
| Ülkeler         | 326,030       | 845,428          | 1,171,458          |
| **Toplam**      | 1,129,883     | 3,239,987        | **4,369,870**      |


### Temel Görseller

**Tablo 1: COVID hakkındaki en çok geçen kelimeler**


<img src="/images/blog/covid/covid.png" width="200" height="200" />
<img src="https://github.com/burakozturan/css_covid19/blob/master/sonuç%20tabloları/Covid_karşılaştırma.png)" width="50" height="50" />






* Öncesinde, İran, İtalya ve Çin gibi vakaların yoğunlukla görüldüğü yerlere sıkça referans verilmiştir. Bu bize, Türkiye'deki ilk vakanın açıklanmasından önce de dış ülkelere yönelik gündemin virüs yoğunluklu olduğunu göstermektedir. Vaka açıklandıktan sonra ise Allah ve sağlık gibi kelimeler öne çıkmaktadır. Bu durum bize Türkçe yazan twitter kullanıcılarının süreci dini argümanlar ile açıkladığına dair bir fikir sunmaktadır. 

