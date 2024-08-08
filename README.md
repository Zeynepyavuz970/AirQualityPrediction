# AirQualityPrediction

Hava kalitesi, insan sağlığı ve çevre üzerinde büyük bir etkiye sahiptir. Hindistan'da hava kalitesini etkileyen başlıca faktörler şunlardır:

### Hava Kalitesini Etkileyen Faktörler

* **PM2.5 ve PM10**: Solunabilir partiküller
* **NO, NO2, NOx**: Azot oksitler
* **NH3**: Amonyak
* **CO**: Karbon monoksit
* **SO2**: Kükürt dioksit
* **O3**: Ozon
* **Benzene, Toluene, Xylene**: Uçucu organik bileşikler

Hava kalitesi tahmin modelimizin temel amacı, Hava Kalitesi İndeksini (AQI) doğru bir şekilde tahmin etmektir. AQI, hava kirliliği seviyesini ve bu seviyenin halk sağlığı üzerindeki etkilerini gösteren bir göstergedir.

Modelimiz, hava kalitesini etkileyen çeşitli kirleticilerin değerlerine göre gelecekteki AQI değerlerini tahmin etmektedir. Bu tahminler, karar vericilerin sağlık uyarıları yayınlamasına, çevresel politikalar oluşturmasına, trafik ve sanayi yönetimini optimize etmesine, genel halkın günlük aktivitelerini planlamasına yardımcı olur.

## Makine Öğrenimini Kullanarak Çözmeye Çalıştığınız İş Sorunu

Bu projede çözmeye çalıştığınız sorun, makine öğrenimi algoritmaları kullanarak hava kalitesi indeksini (AQI) etkileyen faktörleri analiz ederek gelecekteki AQI değerlerini tahmin etmektir. Bu tahminler, hava kalitesini izlemek ve iyileştirme stratejileri geliştirmek için kullanılabilir. Hedef, çeşitli kirletici parametrelerin (PM2.5, PM10, NO, NO2, NOx, NH3, CO, SO2, O3, Benzene, Toluene, Xylene) AQI üzerindeki etkilerini belirlemek ve bu parametrelerin gelecekteki değerlerine dayanarak AQI'yi öngörmektir.

## Neden Bu Sorunu Çözmekle İlgileniyoruz? Bunun İş Üzerinde Ne Gibi Bir Etkisi Olacak?

Bu sorunu çözmek, halk sağlığı, çevresel sürdürülebilirlik ve biyoçeşitliliği koruma açısından büyük önem taşır. Hava kalitesinin doğru bir şekilde tahmin edilmesi, yetkililerin ve halkın hava kirliliği ile ilgili önlemler almasına olanak tanır. Örneğin: sağlık uyarıları ve tedbirler alınabilir, hava kirliliği ile ilgili düzenlemeler ve politikalar oluşturulabilir, sanayi ve trafik yönetimi optimize edilebilir ve topluma daha temiz bir çevre sunularak yaşam kalitesi artırılabilir.

## Bu Sorun Şu Anda Herhangi Bir Makine Öğrenimi Aracı Olmadan Nasıl Çözülüyor?

Bu sorun genellikle temel istatistiksel yöntemler ve uzman tahminleri kullanılarak çözülür. Hava kalitesi izleme istasyonları tarafından toplanan veriler analiz edilerek günlük veya saatlik AQI değerleri raporlanır. Ancak, bu yöntemler çoğu zaman gelecekteki değerleri tahmin etmede sınırlıdır ve karmaşık ilişkileri anlamada yetersiz kalabilir.

## Bu Modelin Sonuçlarını Kim Kullanacak ve Diğer İş Süreçlerine Nasıl Uyum Sağlayacak?

- **Çevre ve Sağlık Bakanlıkları**: Hava kalitesi verilerini izleyip analiz ederek politika geliştirme ve halk sağlığını koruma amacıyla kullanacaklar. Bu, düzenlemeler ve mevzuatlar oluşturmak için gerekli olacaktır.
- **Çevre Ajansları**: Hava kalitesini izleyip düzenlemeler yapabilir.
- **Halk Sağlığı Yetkilileri**: Sağlık uyarıları yayınlayabilir ve halkı bilgilendirebilir.
- **Belediyeler**: Trafik yönetimi ve endüstriyel faaliyetler için kararlar alabilir.
- **Sanayi ve İşletmeler**: Hava kalitesini etkileyen faaliyetleri olan sanayi ve işletmeler, emisyonlarını azaltmak ve yasal düzenlemelere uyum sağlamak için bu modelin sonuçlarını kullanacaklar. Ayrıca, çevre dostu uygulamaları benimseyerek itibarlarını artırabilirler.
- **Akademik ve Araştırma Kuruluşları**: Hava kalitesi ve çevresel etki üzerine çalışmalar yürüten akademik ve araştırma kuruluşları, bu verileri araştırmalarında kullanacaklar. Bu, yeni teknolojilerin ve stratejilerin geliştirilmesine katkı sağlayabilir.
- **Genel Halk**: Günlük aktivitelerini planlamak için hava kalitesi tahminlerinden yararlanabilir.

## Ne Kadar Geçmiş Veriye Sahibiz ve Bunlar Nasıl Toplandı?

01-01-2015 ve 01-07-2020 tarihleri arasındaki ölçümleri içeriyor. Veriler günlük olarak ölçüm yapılmış ve tutulmuştur. Veri kaynağı Kaggle veri kümeleri içinden şudur: [Kaggle Dataset](https://www.kaggle.com/datasets/rohanrao/air-quality-data-in-india)

## Geçmiş Veriler Hangi Özellikleri İçerir? Tahmin Etmeye Çalıştığımız Şeyin Tarihsel Değerlerini İçeriyor Mu?

Evet, bu veriler AQI'nin tarihsel değerlerini içerir ve bu değerler modelin eğitilmesi ve tahmin yapması için kullanılır.

Geçmiş veriler, aşağıdaki özellikleri içerir:
- **City (Şehir)**: Ölçüm yapılan şehir adı.
- **Date (Tarih)**: Ölçüm tarihi.
- **PM2.5, PM10, NO, NO2, NOx, NH3, CO, SO2, O3, Benzene, Toluene, Xylene**: Kirletici parametrelerin ölçülen değerleri.
- **AQI**: Hedef değişken olan hava kalitesi indeksi.
- **AQI Bucket**: AQI değerine göre belirli aralıklarla sınıflandırılmış olan değerler.

## Verilerle İlgili Bilinen Bazı Sorunlar Nelerdir? (Veri Giriş Hataları, Eksik Veriler, Birim Farklılıkları vb.)

- **Eksik Veriler**: Hedef sütun da dahil olmak üzere birden fazla sütunda boş veriler mevcuttur.
- **Birim Farklılıkları**: Date sütunu başlangıçta veri tipi `object` olarak geldi, o sütunun veri tipini `Datetime` olarak dönüştürülmüştür.
- **Mevsimsel Değişiklikler**: Mevsimsel etkiler, veriler üzerinde değişkenlik yaratabilir.
