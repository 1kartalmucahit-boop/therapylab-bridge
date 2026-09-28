# TherapyLab Bridge — dağıtım deposu

Bu depo **yalnızca derlenmiş TherapyLab Bridge sürümlerini barındırır**. Kaynak kod burada değildir.

## Nedir?

TherapyLab Bridge, klinik akustik analiz için ham PCM ses köprüsüdür. Tarayıcının erişemediği düşük gecikmeli, işlenmemiş mikrofon verisini TherapyLab web uygulamasına güvenli bir yerel bağlantı üzerinden aktarır.

- Windows x64, kendine yeten tek dosya (ayrıca .NET kurulumu gerekmez)
- Yerel bağlantı TLS ile şifrelenir; sertifika ilk açılışta cihazda üretilir
- Eşleşme token'ı her açılışta rastgele üretilir (256-bit), hiçbir yere gönderilmez

## İndirme

En güncel sürüm: **[Releases](../../releases/latest)**

Uygulama içindeki "Bridge'i indir" düğmesi de buraya yönlendirir.

## Kurulum

1. `TherapyLabBridge.exe` dosyasını indirin ve çalıştırın
2. Bridge sistem tepsisinde açılır ve size bir token gösterir
3. TherapyLab'de Akustik Analiz → Klinik Mod ekranına token'ı yapıştırın

> Windows SmartScreen uyarısı verebilir (imzasız yürütülebilir). "Ek bilgi" → "Yine de çalıştır" ile devam edin.

## Gizlilik

Bridge yalnızca `localhost` üzerinde dinler. Ses verisi cihazdan çıkmaz; yalnızca aynı bilgisayardaki tarayıcı sekmesine aktarılır. Bağlantı, `therapylab.online` kaynağıyla sınırlıdır.

## Sürümler

Sürümler TherapyLab ana deposundaki CI tarafından otomatik yayımlanır. Sürüm numarası `bridge/bridge.csproj` içindeki `<Version>` etiketinden gelir.

---

TherapyLab — DKT için klinik değerlendirme platformu
