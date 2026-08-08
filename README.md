# Müzik Sınavı V26.18 — Android ve iOS

## V26.18 yeniliği

- 2026 Gerçek Müzik Sınavı Tarzı bölümünde 5–100 arasında serbest soru sayısı seçilebilir.
- AI soruları A4 yazdırılabilir PDF olarak hazırlar.
- Cevap anahtarı ve kısa açıklamalar sorulardan ayrı son sayfalarda bulunur.
- Aynı deneme ekranda çözülebilir veya gerçek kalemle çözmek için yazdırılabilir.

## V26.17 yeniliği

**2026 Gerçek Müzik Sınavı Tarzı** bölümü, adayın gerçek sınavdan hatırladığı soru türlerini bir üretim profili olarak kullanır. AI her çalışmada beş seçenekli yeni sorular hazırlar; hatırlanan soru metinlerini kopyalamaz. 10, 20, 35 veya 70 soruluk deneme üretilebilir.

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
- KHK 2025 Müzik Öğretmenliği çalışma sınavının 70 soruluk konu, uzunluk ve zorluk profilinde; beş seçenekli özgün deneme üreticisi
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

## iPhone / TestFlight

Gerekenler: macOS, güncel Xcode, aktif Apple Developer Program üyeliği ve
App Store Connect erişimi.

1. Terminal'de proje klasörünü açın ve aşağıdaki komutları çalıştırın:

```bash
npm install
npx cap sync ios
npx cap open ios
```

2. Xcode'da soldan **App** projesini, ardından **TARGETS > App** hedefini seçin.
3. **Signing & Capabilities** bölümünde **Automatically manage signing** açık
   olsun ve **Team** alanından Apple Developer hesabınızı seçin.
4. Bundle Identifier olarak `com.caglar.muziksinavi` kullanılır. Apple hesabınızda
   daha önce alınmışsa sonuna benzersiz bir ek koyun; örneğin
   `com.caglar.muziksinavi.caglar`.
5. **General** bölümünde Version `26.18`, Build `3` olarak ayarlanabilir.
6. Üst cihaz listesinden **Any iOS Device (arm64)** seçin.
7. **Product > Archive** komutunu çalıştırın.
8. Organizer açılınca **Distribute App > App Store Connect > Upload** yolunu izleyin.
9. App Store Connect'te aynı Bundle ID ile uygulama kaydı oluşturun. Yüklenen
   derleme işlendikten sonra **TestFlight > Internal Testing** bölümünden kendi
   Apple hesabınızı test kullanıcısı olarak ekleyin.
10. iPhone'da TestFlight uygulamasını açıp daveti kabul ederek uygulamayı kurun.

Her web kodu güncellemesinden sonra Xcode'u açmadan önce `npm run ios:sync`
çalıştırın. Yeni TestFlight yüklemesinde Build numarasını mutlaka artırın.
