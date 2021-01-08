---
title: "Türk - Amerikan Kamuoyu Gündem Araştırması"
date: 2020-12-30T12:52:36+06:00
image_webp: images/blog/blog-post-3.webp
image: images/blog/blog-post-3.jpg
author: Burak Özturan; Yunus Emre Tapan
description : "This is meta description"
---

Amerika Birleşik Devletleri German Marshall Fonu (GMF) tarafından finanse edilen bu araştırma, hem Türkçe hem de İngilizce konuşan kullanıcıların Twitter'daki kamuoyu eğilimlerini analiz etmeyi amaçlamaktadır. Özellikle yeni teknikler kullanarak, Twitter kullanıcıları arasında Türk-Amerikan ilişkilerine dair hakim görüş ve algı değişimlerini incelenmektedir.



Projenin interaktif dashboardu için lütfen [tıklayın](http://tfpbarometer.com/interactive-dashboard/)





## Bu Projenin altı aşaması vardır;

* Sistem altyapısı kurulumu ve depolama
* Veri setlerinin, raporların ve veri toplama protokollerinin belirlenmesi
* Veri toplama ve güncelleme - ETL (Çıkar-Dönüştür-Yükle)
* Modelleme ve Veri Görselleştirme
* Veri Analizi ve Yorumlama
* Yayınlama


>Burada şu ana kadar yaptıklarımızın bir özeti verilecektir:

## Sistem altyapısı kurulumu ve depolama

Öncelikle Twitter'dan alınan verilerin depolanması için Amazon Web Servisleri kullanıldı. Veriler, ilgili bilimsel ve etik standartlara uygun olarak anonim olarak saklanmıştır. Verilerin sürekli olarak beslenmesi ve verilerde güncel tutulması amaçlanırken, bugüne kadar sadece ayrık veri toplama sağlandı.

## Veri setlerinin, raporların ve veri toplama protokollerinin belirlenmesi

Twitter'daki elit kamuoyunu ölçmek için 1411 gerçek twitter hesabı tespit edildi. Hedeflenen twitter kullanıcılarını belirlemek için bu projeye özel yeni bir twitter hesabı oluşturulmuştur. Twitter kullanıcıları milliyetleri, meslekleri, cinsiyetleri, tartışma konuları ve kullanıcı türlerine göre sınıflandırıldı. Milliyetler için Türk, Amerikan ve diğerleri üç seçenektir. İşgal için siyasetçiler, akademisyenler, diplomat, gazeteci ve serbest çalışanlar kümelenme süreci için belirlendi. Tartışma konuları Türk Dış Politikası, Amerikan Dış Politikası ve Uluslararası İlişkiler olmak üzere üç ana başlıktır. Kullanıcı tipine göre kullanıcılar bireysel ve kurumsal hesap olarak sınıflandırılmıştır. Ayrıca konu ile ilgili olarak hem Türkçe hem de İngilizce dilleri için yaklaşık yüz kelimelik bir liste belirlenmiştir. Bu liste, veri kümemizi filtrelememize ve daraltmamıza yardımcı oldu. Nihai olarak üç farklı tweet veri dosyası elde ettik. Birincisi filtresiz, ikincisi yukarıda belirtilen listedeki kelimeleri içeren tweetler  ve üçüncüsü sadece Türk ve Amerikan kelimelerini içeren filtreli tweetler. Bu sınıflandırma, ana veri setimizdeki üç farklı alt grubu karşılaştırmamıza yardımcı oldu.


## Veri toplama ve güncelleme - ETL (Çıkar-Dönüştür-Yükle)

Bu çalışma belirli aralıklara tekrarlanıp kamuoyundaki değişiklikler tesbit edilecektir.

## Modelleme ve Veri Görselleştirme

Veri modellemesi  denetimli öğrenme yöntemi olarak (supervised learning) duyarlılık analizi, denetimsiz bir öğrenme yöntemi (unsupervised learning) olarak konu modellemesi ve istatistiksel bir çıktı olarak metin frekans analizi  yapılarak gerçekleştirildi.

## Veri toplama ve güncelleme - ETL (Çıkar-Dönüştür-Yükle)

Modelleme aşamasında ön analizler yapılmıştır. Duygu analizi bize gelecekte odaklanmamız gereken önemli tarihleri belirlemeizde yardımcı oldu. Konu modelleme (topic modelling) bize ana tartışma konularını verdi. Frekans analizi ayrıca bize ana isimler, konularda tartışılan konuları belirlemize yardımcı oldu.

## Yayınlama

Projemizin çıktılarına buradan ulaşabilirsiniz




