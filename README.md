# Auto Video Editor

DJI Osmo Action videolarını **NVIDIA ekran kartıyla AV1 / HEVC'ye dönüştüren** ve
videodaki hareket verisinden **en ilginç anları bulup kısa reel'ler kesen** Windows programı.

**[⬇ En son sürümü indir](https://github.com/rheadricc/AutoVideoEditor/releases/latest)** —
`AutoVideoEditor-vX.Y.Z-win64.zip` dosyasını çıkar, `AutoVideoEditor.exe`'yi aç. Kurulum yok.

*English below.*

## Neler yapar

**Dönüştür**
- Klasördeki videoları sırayla AV1 ya da HEVC'ye çevirir. Testte 59,6 GB → 9,7 GB (~%84 küçük),
  gözle fark yok. Kalite ön ayarları VMAF ile ölçüldü.
- Süre tahmini (geçen / öngörülen / kalan), sıralama, listeden çıkarma, hemen durdurma.
- Her çıktı doğrulanır (okunuyor mu, süre aynı mı, video akışı var mı); kamera hareket verisi
  ayrı CSV olarak saklanır.
- Orijinalleri silmeyi iş bitince sadece **teklif eder**; varsayılan cevap Hayır, onaylarsan
  Geri Dönüşüm Kutusu'na gider.

**Kırp**
- Yatış açısı, G kuvveti, sarsıntı, dönüş ve sesten ilginç anları puanlar.
- Önizleme, sıralama, limitler (en fazla kesit / reel süresi), tek tıkla reel.
- İsteğe bağlı HUD (yatış + G) ve köşe yazısı; toplu otomatik reel.

**Ayarlar**
- Türkçe / English arayüz, varsayılan çıktı klasörü, silme şekli.
- Performans profilleri: Performans / Dengeli / Arka plan (oyun ya da yayın sırasında yarı kaynak),
  Gelişmiş ayarlar ve paralel iş.

## Gereksinim
- Windows 10 / 11 (64-bit)
- Güncel sürücülü **NVIDIA** ekran kartı (NVENC). AV1 için RTX 40 serisi ve sonrası;
  daha eski kartlarda HEVC seç.
- Kırp sekmesi DJI'ın videoya gömdüğü hareket verisini kullanır (Osmo Action 4 ile test edildi).
- İlk açılışta bir kez internet: ffmpeg yoksa program **"Eksik paketler indiriliyor"** penceresiyle
  onu resmi yayıncısından ([gyan.dev](https://www.gyan.dev/ffmpeg/builds/), ~101 MB) indirir ve
  SHA-256 ile doğrular.

## İlk açılış
Windows *"Bilgisayarınız korundu"* uyarısı verirse **Ek bilgi → Yine de çalıştır**
(exe dijital imzalı değil).

Ayarlar `%APPDATA%\auto_video_editor`, ffmpeg `%LOCALAPPDATA%\auto_video_editor\ffmpeg` içinde.
Kaldırmak için program klasörünü ve bu iki klasörü silmen yeterli.

---

## English

A Windows program that **converts DJI Osmo Action videos to AV1 / HEVC on an NVIDIA GPU** and
**cuts short reels from the most interesting moments**, found from the camera's motion data.

**[⬇ Download the latest release](https://github.com/rheadricc/AutoVideoEditor/releases/latest)** —
extract `AutoVideoEditor-vX.Y.Z-win64.zip` and open `AutoVideoEditor.exe`. No installation.

- **Convert:** batch AV1 / HEVC (~84% smaller in our test, no visible difference), time estimate,
  verified output, motion data kept as CSV. Deleting originals is only *offered* at the end
  (default: No; Recycle Bin by default).
- **Trim:** scores moments from lean angle, G-force, shake, turning and audio; preview, limits,
  one-click reel, optional HUD and caption, batch mode.
- **Settings:** Turkish / English UI, default output folder, performance profiles
  (Performance / Balanced / Background), advanced options and parallel jobs.

**Requirements:** Windows 10 / 11 (64-bit); an NVIDIA GPU with an up-to-date driver (AV1 needs
RTX 40 series or newer, otherwise use HEVC); internet once on first launch — if ffmpeg is missing
the program downloads it from its official publisher (gyan.dev, ~101 MB) and verifies its SHA-256.

If Windows says *"Windows protected your PC"*: **More info → Run anyway** (the exe is not signed).

---

DJI and Osmo are trademarks of SZ DJI Technology Co., Ltd.; NVIDIA and NVENC are trademarks of
NVIDIA Corporation. This project is not affiliated with DJI or NVIDIA.

© 2026 Batuhan Çakır (Rheadric) — see [LICENSE](LICENSE) and
[THIRD-PARTY-NOTICES.txt](THIRD-PARTY-NOTICES.txt).
