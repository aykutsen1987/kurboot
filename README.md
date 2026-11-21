<div align="center">

<img src="kurboot.png" width="120" alt="KurBoot">

# KurBoot

### USB belleği birkaç adımda önyüklenebilir hale getir

![Platform](https://img.shields.io/badge/platform-Windows%2010%2F11-0ea5e9?style=for-the-badge)
![Sürüm](https://img.shields.io/github/v/release/aykutsen1987/kurboot?style=for-the-badge&color=10b981&label=s%C3%BCr%C3%BCm)
![İndirme](https://img.shields.io/github/downloads/aykutsen1987/kurboot/total?style=for-the-badge&color=8b5cf6&label=indirme)

**[⬇️ Son sürümü indir](https://github.com/aykutsen1987/kurboot/releases/latest)**

</div>

---

## ✨ KurBoot nedir?

KurBoot; Windows, Linux ve diğer ISO dosyalarını USB belleğe yazan, **Türkçe, sade ve tıklamalı** bir araçtır.

| Mod | Ne yapar? | Ne zaman kullan? |
|---|---|---|
| 🟦 **Doğrudan Yazma** | Tek bir ISO'yu USB'ye hazırlar | Sadece Windows **veya** sadece bir Linux kuracaksan |
| 🟪 **KurBoot Hibrit** | Birden çok ISO'yu aynı USB'ye koyar; açılışta **KurBoot menüsünden** seçersin | Hem Windows hem Linux, hatta birkaç sistemi tek bellekte taşımak istiyorsan |
| 🟧 **Biçimlendir** | USB'yi temizler ve yeniden biçimlendirir | Belleği boşaltmak / sıfırlamak istiyorsan |

KurBoot Hibrit'te USB iki gruba ayrılır: **Linux ve Diğerleri** ile **Windows**. Bilgisayar USB'den açılınca renkli bir KurBoot menüsü gelir (BIOS ve UEFI desteklenir).

---

## ⬇️ İndirme

[**Releases (Sürümler) sayfasına**](https://github.com/aykutsen1987/kurboot/releases/latest) git ve **Assets** bölümünden birini seç:

| Dosya | Ne işe yarar? |
|---|---|
| 🟢 **`KurBoot_Setup.exe`** *(önerilir)* | Kurulum sihirbazı. Program Files'a kurar, Başlat menüsü / masaüstü kısayolu ekler. |
| 🔵 **`KurBoot.exe`** | Taşınabilir tek dosya. Kurulum yok, çift tıkla çalışır. |
| ⚪ `*.sha256` | Dosyanın bozulmadığını doğrulamak için (isteğe bağlı). |

> [!NOTE]
> Kaynak kodu zip'i (`Source code`) **çalıştırmak için gerekmez**; sadece geliştiriciler içindir.

---

## 🛡️ Windows uyarıları (lütfen oku)

> [!IMPORTANT]
> **"Windows bilgisayarınızı korudu" (SmartScreen) uyarısı çıkabilir.**
> KurBoot yeni ve imzasız bir uygulamadır, bu yüzden Windows tanımıyor. Dosyayı yalnızca bu GitHub sayfasından indirdiysen:
> **Ek bilgi → Yine de çalıştır** de.

> [!IMPORTANT]
> **Yönetici izni ister.** USB diske yazabilmek için gereklidir. Çıkan pencerede **Evet** de.

> [!WARNING]
> **Antivirüs yanlış alarm verebilir.** Disk yazan programlar bazen şüpheli sanılır. Dosyanın `.sha256` değerini karşılaştırabilir, gerekirse KurBoot'u antivirüsünde güvenilen olarak ekleyebilirsin.

---

## 🚀 Kullanım (adım adım)

> [!CAUTION]
> ### ⛔ SEÇTİĞİN USB'DEKİ TÜM VERİLER SİLİNİR!
> Önemli dosyalarını **önceden yedekle**. Doğru diski seçtiğinden emin ol. KurBoot sistem disklerini seçtirmez, ama dikkat senin elinde.

1. **USB'yi tak.** (En az 8 GB önerilir; Hibrit için ISO'ların toplamından büyük olmalı.)
2. **KurBoot'u aç** → yönetici izni isteyince *Evet*.
3. **① Hedef USB'yi seç.** Listede doğru belleği (boyutuna bakarak) işaretle. Görünmüyorsa **Yenile**'ye bas.
4. **② ISO ekle.** ISO dosyalarını kutuya **sürükle-bırak** ya da kutuya tıklayıp seç. İstersen menüde görünecek adı ve türünü (Windows / Linux / Diğer) değiştir.
5. **③ Modu seç:**
   - 🟦 **Doğrudan Yazma** → tek ISO için
   - 🟪 **KurBoot Hibrit** → birden fazla ISO için
   - **Şema:** yeni bilgisayarlar için **GPT (UEFI)**, çok eski bilgisayarlar için **MBR (BIOS)**. KurBoot Hibrit her ikisinde de açılır.
6. **④ BAŞLAT'a bas** ve onay penceresini oku. İşlem bitene kadar USB'yi **çıkarma**.

> [!TIP]
> Önce **Deneme modu** (üstteki turuncu kutu) açıkken çalıştırırsan KurBoot diske **hiçbir şey yazmaz**, sadece neler yapacağını gösterir. Gerçek işlem için deneme modunu kapat.

### 💾 Hibrit USB'ye sonradan ISO eklemek

KurBoot Hibrit USB'sinde büyük bölümün içindeki `KurBoot\ISO` klasörü ISO'larını tutar. Linux ISO'larını bu klasöre kopyalayabilirsin.

---

## 🖥️ USB'den bilgisayarı açmak

1. USB takılıyken bilgisayarı **yeniden başlat**.
2. Açılırken boot menüsü tuşuna art arda bas: **F12**, **F11**, **F10**, **F9**, **Esc** ya da **F8** *(markaya göre değişir)*.
3. Listeden USB'yi (UEFI için "UEFI: …" olanı) seç.
4. **KurBoot menüsü** gelir → ok tuşlarıyla seç, **Enter** ile başlat.

> [!WARNING]
> **Secure Boot (Güvenli Önyükleme) KAPALI olmalı** — KurBoot Hibrit menüsü Microsoft imzalı değildir. Açıksa USB "güvenlik ihlali" hatası verir ya da hiç görünmez. BIOS/UEFI ayarlarından *Secure Boot → Disabled* yapın. İşiniz bitince tekrar açabilirsiniz.

---

## 🔄 Otomatik güncelleme

KurBoot her açıldığında GitHub'daki en yeni sürümü sessizce denetler (internet yoksa sorun çıkarmaz).

- 🟢 Yeni sürüm varsa üstte yeşil bir şerit çıkar: **Güncelle · Neler yeni · Sonra**.
- **Güncelle**'ye basarsan sürüm **arka planda indirilir** (bu sırada KurBoot'u kullanmaya devam edebilirsin), doğrulanır, sonra program kendini yeniler.
- **Sonra** dersen şerit kapanır ama **bir sonraki açılışta yine sorulur**, sen onaylayana kadar.
- Elle denetlemek için altta **Güncellemeyi denetle** düğmesi var.
- Eğer KurBoot'u yalnızca Python dosyası olarak çalıştırıyorsan (EXE değil), güncelleme sayfası tarayıcıda açılır.

> [!NOTE]
> Güncelleme yalnızca **Windows EXE/Setup** sürümünde kendini kurar. İşlem sürerken (USB yazılırken) güncelleme **uygulanmaz**, işlem bitince uygulanır.

---

## 🧰 Sorun giderme

| Sorun | Çözüm |
|---|---|
| USB listede yok | **Yenile**'ye bas; "Dahili diskler" kutusu kapalıysa sistem disklerini zaten gizler. Başka USB portu dene. |
| ISO sürüklenmiyor | Kutuya **tıklayıp** dosyayı seç. KurBoot'u yönetici çalıştırdıysan Gezgin'den bırakma desteklenir, yine de olmazsa tıklayarak ekle. |
| USB'den açılmıyor | Secure Boot'u **kapat**; boot menüsünde "UEFI:" ile başlayan girdiyi dene; şemayı MBR/GPT olarak değiştirip tekrar yaz. |
| Windows kurulumu "4 GB üstü dosya" diyor | KurBoot `install.wim` dosyasını otomatik böler; Doğrudan Yazma kipini kullan. |
| Hata kodu (KUR-xxx) çıktı | **Günlüğü kaydet** düğmesiyle günlüğü kaydet ve [Issues](https://github.com/aykutsen1987/kurboot/issues) sayfasına ekle. |

---

## ⚠️ Bilinen sınırlar

- Yalnızca **Windows 10/11** için hazırlanmıştır (Linux'ta çalıştırma geliştirme amaçlıdır).
- Hibrit menüdeki **Linux ISO'ları** için uyumluluk dağıtıma göre değişir; çoğu canlı (live) ISO açılır, hepsi garanti değildir.
- ISO'lar Hibrit USB'nin **exFAT** bölümünde durur; çok eski BIOS'lar bazen USB'den açmayı reddedebilir.
- Secure Boot açıkken Hibrit USB açılmaz (yukarıya bak).

---

## 👩‍💻 Geliştiriciler için

**Gereken:** Python 3.9+ ([python.org](https://www.python.org/downloads/), kurulumda *Add Python to PATH*) ve isteğe bağlı [Inno Setup 6](https://jrsoftware.org/isdl.php) (Setup için).

```text
Çalıştırmak (geliştirme):   run_kurboot.bat        (Linux: ./run_kurboot.sh)
EXE + Setup üretmek:        build_all.bat
Sadece EXE üretmek:         build_exe.bat
```

### 📦 Yeni sürüm yayınlama

1. **`kur_version.py`** dosyasında `__version__` değerini yükselt (ör. `"0.4.1"`). *Sürüm numarası sadece burada.*
2. **`build_all.bat`** çalıştır → `release\` klasöründe şunlar oluşur:
   `KurBoot.exe`, `KurBoot.exe.sha256`, `KurBoot_Setup.exe`, `KurBoot_Setup.exe.sha256`
3. GitHub → **Releases → Draft a new release** → etiket: **`v0.4.1`** (başında `v`).
4. Dosyaları **Assets**'e sürükle ve **Publish release** de.

> [!IMPORTANT]
> Güncellemenin çalışması için: etiket sürüm numarasından büyük olmalı (`v0.4.1`), dosya adı **tam** `KurBoot.exe` / `KurBoot_Setup.exe` olmalı ve release **taslak/ön sürüm (pre-release) olmamalı**. `.sha256` dosyası eklenirse KurBoot indirileni otomatik doğrular.

İstersen `.github/workflows/release.yml` sayesinde `git tag v0.4.1 && git push --tags` ile GitHub EXE'yi senin yerine derler.

---

## 📜 Lisans ve teşekkür

- KurBoot'un lisansı: depodaki `LICENSE` dosyasına bakın.
- Hibrit menü **GNU GRUB** (GPL-3.0+) ve **wimboot** (GPL-2.0+) kullanır. Ayrıntı: [NOTICE.md](NOTICE.md).
- Windows, Linux ve adı geçen tüm markalar sahiplerinin tescilli markalarıdır.

<div align="center">

Geliştirici: [@aykutsen1987](https://github.com/aykutsen1987)

</div>
