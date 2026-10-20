# Nuvios

Android ve Android TV için, [CloudStream](https://github.com/recloudstream/cloudstream) tabanlı bir medya oynatıcı.
CloudStream (CS3) eklenti depolarını destekler. İçerik barındırmaz; depoları uygulama içinden sen eklersin.

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

## Lisans
CloudStream GPL-3.0 lisanslıdır; bu çalışma da GPL-3.0 altındadır.
