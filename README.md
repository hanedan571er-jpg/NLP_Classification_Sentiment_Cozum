Sonuç ve işletme önerileri
Temiz İngilizce analiz kümesi 10,343 yorumdur. Model yalnız metni kullanır; yıldızlar hedeftir. Doğrulama macro-F1 ile Count_ngram + LogisticRegression seçildi. Test doğruluğu %80.64, macro-F1 0.6693.

Nötr sınıf recall 0.3248; genel accuracy tek başına nötr yorum başarısını açıklamaz. Sınıf dengesizliği yüzünden macro-F1 ayrıca raporlanır. Yıldız etiketiyle sözlük duygu skorunun uyuşmaması her zaman yazılım hatası değildir; yorum aynı anda övgü ve eleştiri içerebilir.

İşletme için: düşük yıldızlı yorumlarda geçen bekleme, fiyat ve servis ifadeleri insan incelemesine alınmalı; doğrulanan konular için bekleme süresi ölçümü, fiyat/içerik açıklaması ve servis geri bildirim süreci tasarlanmalıdır. Tema CSV’si yalnız sözcük eşleşmesi sayar, gerçek şikâyet veya sağlık vakası saymaz. Başka işletmeye ait deneyimler bu restoranın olayı gibi aktarılmamalıdır.

Gelecek çalışma: zaman sıralı dış test, elle etiketlenmiş duygu örnekleri ve nötr sınıf hata incelemesi; test skorunu görüp bu deneyin parametreleri değiştirilmedi. Bu deney yeni kullanıcı gruplarına ayrılmış rastgele testtir, geleceğe dönük başarı kanıtı değildir.

Foursquare (26 Eylül 2026'da eklendi): Canlı sayfa giriş istediği için aynı mekân sayfasının Wayback Machine'deki 286 kamuya açık kopyası kazındı; 396 tekil ipucundan 316 İngilizce ipucu analiz edildi. Foursquare ipuçları Yelp yorumlarından çok daha kısadır (medyan 16 / 98 kelime). TextBlob pozitif oranı Yelp'te %90.3, Foursquare'de %78.8; fark büyük ölçüde nötr orandan gelir (%0.4 / %11.7), çünkü kısa ipuçlarında sözlük çoğu zaman duygu kelimesi bulamaz. Negatif oran iki platformda yakındır (%9.3 / %9.5). 30 negatif ipucunun 11 tanesi uzun kuyruk/beklemeden söz ediyor; bu, Yelp'teki bekleme temasıyla aynı yönde bir işarettir. Arşiv yalnız yakalanan sayfaları içerir; Foursquare'deki tüm ipuçlarının tamamı olduğu iddia edilmez.

Twitter: Tweet verisi elde edilemedi. X arama sayfası giriş istiyor, API ücretli; arşivdeki arama sayfaları yalnız JavaScript kabuğu içeriyor. Twitter duygu analizi ve üç platformun tam karşılaştırması bu nedenle yapılmadı; eski sunumdaki Twitter yüzdeleri kullanılmadı.

Kaynaklar
Asıl ders notebook’ları ve hücreler: DERS_KAYNAKLARI.json, ders_kaynaklari/.
Kullanıcı yönergesi ve görseller: kaynak/.
NLTK VADER: https://www.nltk.org/api/nltk.sentiment.SentimentIntensityAnalyzer.html
Vektörleştirici: https://scikit-learn.org/1.5/modules/generated/sklearn.feature_extraction.text.CountVectorizer.html
Foursquare arşiv kopyaları: Internet Archive Wayback Machine, https://web.archive.org/ (liste: kaynak/foursquare_arsiv/arsiv_kopyalari.csv).
Örnek sunumla ilişkili kaynak proje: https://github.com/yalinyener/NLPClassification . Başkasının sonuçları kendi ölçümümüz yerine kullanılmadı.
