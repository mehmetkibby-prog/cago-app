# Müzik Sınavı Android V26.26

Bu paket yalnız Android projesidir; `ios` klasörü içermez.

## V26.26

- 2026 Gerçek Sınav bölümünde 5-10 soru tek hızlı AI çağrısında hazırlanır; büyük denemeler 10'ar soruluk paketlere ayrılır.
- Geçen her paket cihazda taslak olarak saklanır; uygulama kapanırsa yalnız eksik sorulardan devam edilir.
- Bir paket denetimden geçmezse sağlam sorular korunur ve eksik bölüm küçültülerek yeniden hazırlanır.
- Tek kalan soru tekrar filtresine takılırsa aynı konu yeniden istenmez; aynı sınav alanından kullanılmamış başka bir konu otomatik seçilir.
- Konu değiştirme yalnız içerik veya tekrar denetimi hatasında çalışır; ağ, zaman aşımı ve API hesabı hatalarında gereksiz döngü oluşturmaz.
- V26.25'te kaydedilmiş yarım 2026 denemeleri korunur ve güncellemeden sonra kaldığı yerden devam eder.
- Tekrar hafızası, doğru cevap dengesi ve Divan sazı, ritardando, Rast makamı ve armoni tarihi bilgi korumaları korunmuştur.
- Android tablet görünümü, renkler, soru bankaları ve diğer özellikler değiştirilmemiştir.

## GitHub ile APK oluşturma

1. Bu klasörün içindeki bütün dosya ve klasörleri GitHub deposunun ana dizinine yükleyin. `.github` klasörü de yüklenmelidir.
2. GitHub'da **Actions → APK oluştur** bölümünü açın.
3. Çalışma tamamlanınca **Muzik-Sinavi-Android-V26.26-Debug-APK** çıktısını indirin.
4. ZIP'in içindeki `app-debug.apk` dosyasını Android cihaza kurun.

## Bilgisayarda yerel derleme

```bash
npm install
npx cap sync android
cd android
./gradlew assembleDebug
```

APK, `android/app/build/outputs/apk/debug/app-debug.apk` konumunda oluşur.
