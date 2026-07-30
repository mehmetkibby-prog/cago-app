# Müzik Sınavı V26.12 — Kaynak Hatası Düzeltilmiş Tam Android ve GitHub Paketi

V26.6 çalışan Android sürümünü koruyan; bütün müzik alanlarında kaynak
doğrulamalı AI soruları üreten ve soru kökünü doğal AI kadın sesiyle
ayarlanabilir hızda okuyan eksiksiz Android projesidir.

## İçerik

- 14 bölümde toplam 834 soru
- A–D ve A–E cevap desteği
- Zor Sorular listesi ve ayrı çözme modu
- Cihazda kalıcı başarı geçmişi
- AI Eğitim Bilimleri denemesi
- Tüm dönemler, Türk müziği, çalgılar, teori ve formlar için AI Müzik Soru Oluşturucu
- Üniversite, konservatuvar ve güvenilir kurum kaynaklarını önceleyen web doğrulaması
- Yalnız soru kökünü okuyan doğal AI kadın sesi ve 0,65×–1,40× hız ayarı
- OpenAI Realtime AI Voice
- Tablet ekranına uyumlu yatay/dikey arayüz

API anahtarı uygulamanın Ayarlar ekranına girilir ve yalnızca cihazdaki
uygulama depolama alanında saklanır.

## APK oluşturma

Android Studio ile `android` klasörünü açın. Gradle eşitlemesi tamamlandıktan
sonra **Build > Build APK(s)** komutunu kullanın. Debug APK şu konumda oluşur:

`android/app/build/outputs/apk/debug/app-debug.apk`

Komut satırı alternatifi:

```bash
npm install
npx cap sync android
cd android
./gradlew assembleDebug
```

Android Studio ilk açılışta gerekli Android SDK ve Gradle bileşenlerini
internet üzerinden indirir.
