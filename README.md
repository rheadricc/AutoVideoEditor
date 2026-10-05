# Auto Video Editor

A free Windows program that **converts DJI Osmo Action videos to AV1 / HEVC on an NVIDIA GPU** and
**cuts short reels from the most interesting moments**, found from the camera's motion data.

<p align="center">
  <a href="https://github.com/rheadricc/AutoVideoEditor/releases/download/v1.1.0/AutoVideoEditor-v1.1.0-win64.zip"><img height="40" alt="Download Auto Video Editor 1.1.0 for Windows" src="https://img.shields.io/badge/Download-v1.1.0%20%7C%20Windows%2010%20%2F%2011-2ea44f?style=for-the-badge"></a>
</p>

## Download

**The program is right here in this repository:** `AutoVideoEditor.exe` is the program,
`Uninstall.exe` removes it. Get it either way:

1. the green **Download** button above →
   [`AutoVideoEditor-v1.1.0-win64.zip`](https://github.com/rheadricc/AutoVideoEditor/releases/download/v1.1.0/AutoVideoEditor-v1.1.0-win64.zip) (~29 MB), or
2. the green **`<> Code`** button at the top of this page → **Download ZIP**.

Then **extract the zip** (right-click → *Extract All…*) and open **`AutoVideoEditor.exe`**.
No installation. Older versions and release notes: [Releases](https://github.com/rheadricc/AutoVideoEditor/releases).

*Türkçe aşağıda.*

## What it does

**Convert**
- Converts the videos in a folder to AV1 or HEVC one by one. In our test 59.6 GB → 9.7 GB
  (~84% smaller) with no visible difference. Quality presets were measured with VMAF.
- Time estimate (elapsed / expected / remaining), reordering, removing from the list, stop now.
- Every output is verified (does it open, same duration, has a video stream); the camera's
  motion data is kept as a separate CSV.
- Deleting the originals is only **offered** when a job finishes; the default answer is No, and
  if you confirm they go to the Recycle Bin.

**Trim**
- Scores moments from lean angle, G-force, shake, turning and audio.
- Preview, reordering, limits (max clips / reel length), one-click reel.
- Optional HUD (lean + G) and caption; automatic batch reels.

**Settings**
- English / Türkçe interface, default output folder, delete mode.
- Performance profiles: Performance / Balanced / Background (half the resources, for gaming or
  streaming), advanced options and parallel jobs.

## Requirements
- Windows 10 / 11 (64-bit)
- An **NVIDIA** GPU with an up-to-date driver (NVENC). AV1 needs an RTX 40 series card or newer;
  choose HEVC on older cards.
- The Trim tab uses the motion data DJI embeds in the video (tested with Osmo Action 4).
- Internet once on first launch: if ffmpeg is missing, the program shows a **"Downloading missing
  components"** window, downloads it from its official publisher
  ([gyan.dev](https://www.gyan.dev/ffmpeg/builds/), ~101 MB) and verifies its SHA-256.

## First launch
The program starts in English; for Turkish open **Settings** (gear, top right) → **General** →
**DİL / LANGUAGE** → **Türkçe**.

If Windows says *"Windows protected your PC"*: **More info → Run anyway** (the exe is not signed yet).

Settings are stored in `%APPDATA%\auto_video_editor`, ffmpeg in `%LOCALAPPDATA%\auto_video_editor\ffmpeg`.

## Uninstall
Run **`Uninstall.exe`** in the program folder. It removes the program files, the settings, the
downloaded ffmpeg and leftover temporary files, then deletes itself. Your converted videos and
reels are not deleted.

---

## Türkçe

DJI Osmo Action videolarını **NVIDIA ekran kartıyla AV1 / HEVC'ye dönüştüren** ve videodaki
hareket verisinden **en ilginç anları bulup kısa reel'ler kesen** ücretsiz Windows programı.

**İndir:** program bu repoda: `AutoVideoEditor.exe` program, `Uninstall.exe` kaldırıcı. Yukarıdaki
yeşil **Download** düğmesi
([`AutoVideoEditor-v1.1.0-win64.zip`](https://github.com/rheadricc/AutoVideoEditor/releases/download/v1.1.0/AutoVideoEditor-v1.1.0-win64.zip),
~29 MB) ya da sayfanın üstündeki yeşil **`<> Code`** düğmesi → **Download ZIP**. Zip'i çıkar
(sağ tık → *Tümünü ayıkla…*), **`AutoVideoEditor.exe`**'yi aç. Kurulum yok. Eski sürümler ve sürüm
notları: [Releases](https://github.com/rheadricc/AutoVideoEditor/releases).

- **Dönüştür:** toplu AV1 / HEVC (testte ~%84 küçük, gözle fark yok), süre tahmini, doğrulanmış
  çıktı, hareket verisi CSV olarak saklanır. Orijinalleri silmek iş bitince sadece *teklif edilir*
  (varsayılan Hayır; varsayılan olarak Geri Dönüşüm Kutusu).
- **Kırp:** yatış açısı, G kuvveti, sarsıntı, dönüş ve sesten anları puanlar; önizleme, limitler,
  tek tıkla reel, isteğe bağlı HUD ve köşe yazısı, toplu mod.
- **Ayarlar:** English / Türkçe arayüz, varsayılan çıktı klasörü, performans profilleri
  (Performans / Dengeli / Arka plan), gelişmiş ayarlar ve paralel iş.

**Gereksinim:** Windows 10 / 11 (64-bit); güncel sürücülü NVIDIA ekran kartı (AV1 için RTX 40 serisi
ve sonrası, değilse HEVC); ilk açılışta bir kez internet — ffmpeg yoksa program onu resmi
yayıncısından (gyan.dev, ~101 MB) indirir ve SHA-256 ile doğrular.

**Dil:** program İngilizce açılır; Türkçe için **Settings** (sağ üstteki dişli) → **General** →
**DİL / LANGUAGE** → **Türkçe**.

Windows *"Bilgisayarınız korundu"* derse: **Ek bilgi → Yine de çalıştır** (exe henüz imzalı değil).

**Kaldırma:** program klasöründeki **`Uninstall.exe`**'yi çalıştır; program dosyalarını, ayarları,
indirilen ffmpeg'i ve geçici dosyaları siler, sonra kendini siler. Videoların silinmez.

---

DJI and Osmo are trademarks of SZ DJI Technology Co., Ltd.; NVIDIA and NVENC are trademarks of
NVIDIA Corporation. This project is not affiliated with DJI or NVIDIA.

© 2026 Batuhan Çakır (Rheadric) — see [LICENSE.txt](LICENSE.txt) and
[THIRD-PARTY-NOTICES.txt](THIRD-PARTY-NOTICES.txt).
