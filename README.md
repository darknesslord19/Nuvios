# Nuvios

Android ve Android TV için, [CloudStream](https://github.com/recloudstream/cloudstream) tabanlı bir medya oynatıcı.
CloudStream (CS3) eklenti depolarını ve Nuvio JS eklenti depolarını (manifest.json) destekler.
İçerik barındırmaz; depoları uygulama içinden sen eklersin.

## Depo ekleme
**Ayarlar › Eklentiler › Depo ekle** ekranına adresi yapıştır. Uygulama türünü kendisi algılar:
- CloudStream deposu (`repo.json`) → eklentiler her zamanki gibi listelenir.
- Nuvio deposu (`manifest.json`) → eklentiler indirilir, ana sayfadaki kaynak seçicide **Nuvio Eklentileri** belirir.
  Katalog TMDB'den gelir; bir film/bölüm açtığında tüm Nuvio eklentileri çalıştırılıp bağlantılar listelenir.

## Farkları
- Koyu tema ve turkuaz vurgu rengi
- Uygulama adı **Nuvios**, paket adı `com.darknesslord19.nuvios.debug` (orijinal CloudStream ile yan yana kurulabilir)

## APK nasıl alınır
Her `main` güncellemesinde GitHub Actions APK'yı derler.
**Releases** sayfasındaki en son `Nuvios-*.apk` dosyasını indirip kurman yeterli.
Elle derlemek için: **Actions › APK derle › Run workflow**.

## Nasıl çalışır
Depo, CloudStream'in kaynak kodunu değil, sadece `patches/nuvios.patch` yamasını tutar.
Derleme sırasında CloudStream'in sabitlenmiş sürümü indirilir, yama uygulanır ve APK üretilir.

## Nuvio motoru
Nuvio eklentileri, [NuvioTV](https://github.com/tapframe/NuvioTV) (GPL-3.0) projesinden uyarlanan QuickJS tabanlı çalıştırıcıyla
çalışır (`app/src/main/java/com/lagradost/cloudstream3/nuvio/`). QuickJS kütüphanesi CloudStream içindeki zipline ile çakışmaması
için `libquickjz.so` olarak yeniden adlandırılmıştır.

## Lisans
CloudStream GPL-3.0 lisanslıdır; bu çalışma da GPL-3.0 altındadır.
