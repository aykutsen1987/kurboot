<a id="top"></a>
<div align="center">

<img src="kurboot.png" width="120" alt="KurBoot">

# KurBoot

### USB belleği birkaç adımda önyüklenebilir hale getir

![Platform](https://img.shields.io/badge/platform-Windows%2010%2F11-0ea5e9?style=for-the-badge)
![Sürüm](https://img.shields.io/github/v/release/aykutsen1987/kurboot?style=for-the-badge&color=10b981&label=s%C3%BCr%C3%BCm)
![İndirme](https://img.shields.io/github/downloads/aykutsen1987/kurboot/total?style=for-the-badge&color=8b5cf6&label=indirme)

**[⬇️ Son sürümü indir / Download latest](https://github.com/aykutsen1987/kurboot/releases/latest)**

**🇹🇷 Türkçe (aşağıda) · [🇬🇧 English](#english)**

</div>

---

# 🇹🇷 Türkçe

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

## 🩹 Setup sonrası hata verirse (EXE'yi elle kopyalama)

`KurBoot_Setup.exe` ile kurulumdan sonra program **açılmıyor ya da hata veriyorsa**, kurulumu atlayıp `KurBoot.exe` dosyasını kurulum klasörüne kendin kopyalayabilirsin:

1. [Releases](https://github.com/aykutsen1987/kurboot/releases/latest) sayfasından **`KurBoot.exe`** dosyasını indir.
2. KurBoot açıksa kapat (sağ alttaki görev çubuğuna da bak).
3. Dosya Gezgini'nde kurulum klasörünü aç. Varsayılan konum:
   ```text
   C:\Program Files\KurBoot
   ```
   *(Kurulumda başka klasör seçtiysen orayı aç. Başlat menüsündeki **KurBoot** kısayoluna sağ tıklayıp **Dosya konumunu aç** diyerek de bulabilirsin.)*
4. İndirdiğin `KurBoot.exe` dosyasını bu klasöre **kopyala** ve aynı adlı dosya varsa **Hedefteki dosyanın üzerine yaz** de. *(Yönetici izni sorarsa **Devam** de.)*
5. Kısayoldan ya da doğrudan `KurBoot.exe`'ye çift tıklayarak aç.

> [!TIP]
> Kurulum klasörüne kopyalamak istemezsen `KurBoot.exe` zaten **taşınabilirdir**: masaüstü gibi herhangi bir klasörden çift tıklayıp çalıştırabilirsin.

> [!NOTE]
> Yine açılmıyorsa SmartScreen/antivirüs dosyayı engellemiş olabilir. `KurBoot.exe`'ye sağ tıkla → **Özellikler** → en altta **Engellemeyi kaldır** kutusunu işaretle → **Tamam**. Sonra tekrar dene.

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

---

<a id="english"></a>

# 🇬🇧 English

<div align="right"><a href="#top">🇹🇷 Türkçe'ye git ↑</a></div>

## ✨ What is KurBoot?

KurBoot writes Windows, Linux and other ISO files to a USB drive with a **simple, clickable interface** (Turkish UI).

| Mode | What it does | When to use it |
|---|---|---|
| 🟦 **Direct Write** | Prepares a single ISO on the USB | You only need Windows **or** one Linux |
| 🟪 **KurBoot Hybrid** | Puts several ISOs on one USB; you pick from the **KurBoot boot menu** at startup | You want Windows and Linux (or several systems) on one drive |
| 🟧 **Format** | Wipes and reformats the USB | You want to empty / reset the drive |

With KurBoot Hybrid the USB is split into two groups: **Linux & Others** and **Windows**. When the PC boots from the USB, a colourful KurBoot menu appears (BIOS and UEFI supported).

---

## ⬇️ Download

Go to the [**Releases page**](https://github.com/aykutsen1987/kurboot/releases/latest) and pick one file under **Assets**:

| File | Purpose |
|---|---|
| 🟢 **`KurBoot_Setup.exe`** *(recommended)* | Installer wizard. Installs to Program Files, adds Start menu / desktop shortcuts. |
| 🔵 **`KurBoot.exe`** | Portable single file. No installation, just double-click. |
| ⚪ `*.sha256` | Checksum to verify the file is intact (optional). |

> [!NOTE]
> The `Source code` zip is **not needed to run the app**; it is for developers only.

---

## 🛡️ Windows warnings (please read)

> [!IMPORTANT]
> **A "Windows protected your PC" (SmartScreen) warning may appear.**
> KurBoot is new and unsigned, so Windows does not recognise it. If you downloaded it from this GitHub page only, click **More info → Run anyway**.

> [!IMPORTANT]
> **It asks for administrator permission.** This is required to write to a USB disk. Click **Yes**.

> [!WARNING]
> **Antivirus software may raise a false alarm.** Programs that write to disks are sometimes flagged. You can compare the `.sha256` value and, if needed, mark KurBoot as trusted in your antivirus.

---

## 🚀 Usage (step by step)

> [!CAUTION]
> ### ⛔ ALL DATA ON THE SELECTED USB WILL BE ERASED!
> **Back up** important files first. Make sure you select the right disk. KurBoot does not let you pick system disks, but the responsibility is yours.

1. **Plug in the USB** (8 GB or more recommended; for Hybrid it must be larger than all ISOs combined).
2. **Open KurBoot** → click *Yes* on the administrator prompt.
3. **① Select the target USB.** Tick the correct drive (check its size). Press **Refresh** if it is not listed.
4. **② Add ISOs.** **Drag and drop** ISO files into the box, or click the box to pick them. You can change the menu name and type (Windows / Linux / Other).
5. **③ Choose the mode:**
   - 🟦 **Direct Write** → for a single ISO
   - 🟪 **KurBoot Hybrid** → for multiple ISOs
   - **Scheme:** **GPT (UEFI)** for newer PCs, **MBR (BIOS)** for very old PCs. KurBoot Hybrid boots on both.
6. **④ Press START** and read the confirmation window. **Do not unplug** the USB until it finishes.

> [!TIP]
> If **Test mode** (orange box at the top) is on, KurBoot writes **nothing** to the disk and only shows what it would do. Turn it off for the real run.

### 💾 Adding ISOs to a Hybrid USB later

On a KurBoot Hybrid USB, the `KurBoot\ISO` folder on the large partition holds your ISOs. You can copy more Linux ISOs into it.

---

## 🖥️ Booting a PC from the USB

1. With the USB plugged in, **restart** the PC.
2. While it starts, tap the boot-menu key repeatedly: **F12**, **F11**, **F10**, **F9**, **Esc** or **F8** *(depends on the brand)*.
3. Choose the USB in the list (the "UEFI: …" entry for UEFI).
4. The **KurBoot menu** appears → use the arrow keys, press **Enter** to start.

> [!WARNING]
> **Secure Boot must be OFF** — the KurBoot Hybrid menu is not signed by Microsoft. If it is on, the USB gives a "security violation" error or does not show up. Set *Secure Boot → Disabled* in your BIOS/UEFI settings; you can turn it back on afterwards.

---

## 🔄 Automatic updates

Every time KurBoot starts, it quietly checks GitHub for the latest version (no problem if you are offline).

- 🟢 If a new version exists, a green bar appears at the top: **Update · What's new · Later**.
- Press **Update** and the version is **downloaded in the background** (you can keep using KurBoot), verified, and then the program refreshes itself.
- If you choose **Later**, the bar closes but **you are asked again at the next start**, until you approve.
- You can also check manually with the **Check for updates** button at the bottom.
- If you run KurBoot as plain Python files (not the EXE), the release page opens in your browser instead.

> [!NOTE]
> Updates install themselves only for the **Windows EXE/Setup** build. While a job is running (writing a USB), the update is **not applied**; it is applied when the job ends.

---

## 🩹 If you get an error after Setup (copy the EXE manually)

If the program **does not open or shows an error** after installing with `KurBoot_Setup.exe`, you can skip the installer and copy `KurBoot.exe` into the installation folder yourself:

1. Download **`KurBoot.exe`** from the [Releases](https://github.com/aykutsen1987/kurboot/releases/latest) page.
2. Close KurBoot if it is open (also check the system tray).
3. Open the installation folder in File Explorer. Default location:
   ```text
   C:\Program Files\KurBoot
   ```
   *(If you chose another folder during setup, open that one. You can also right-click the **KurBoot** shortcut in the Start menu and choose **Open file location**.)*
4. **Copy** the downloaded `KurBoot.exe` into this folder and choose **Replace the file in the destination** if a file with the same name exists. *(Click **Continue** if asked for administrator permission.)*
5. Start it from the shortcut or by double-clicking `KurBoot.exe`.

> [!TIP]
> If you prefer not to copy it, `KurBoot.exe` is **portable** anyway: double-click it from any folder, such as the desktop.

> [!NOTE]
> If it still does not open, SmartScreen/antivirus may have blocked the file. Right-click `KurBoot.exe` → **Properties** → tick **Unblock** at the bottom → **OK**, then try again.

---

## 🧰 Troubleshooting

| Problem | Solution |
|---|---|
| USB not listed | Press **Refresh**; if "Internal disks" is unticked, system disks are hidden by design. Try another USB port. |
| ISO cannot be dragged in | **Click** the box and pick the file. Drag-and-drop from Explorer is supported when KurBoot runs as administrator, but if it still fails, add the ISO by clicking. |
| Will not boot from USB | Turn **Secure Boot off**; try the "UEFI:" entry in the boot menu; switch the scheme between MBR/GPT and write again. |
| Windows setup complains about a file over 4 GB | KurBoot splits `install.wim` automatically; use Direct Write mode. |
| An error code (KUR-xxx) appears | Save the log with **Save log** and attach it on the [Issues](https://github.com/aykutsen1987/kurboot/issues) page. |

---

## ⚠️ Known limitations

- Made for **Windows 10/11** only (running on Linux is for development).
- **Linux ISOs** in the Hybrid menu: compatibility varies by distribution; most live ISOs boot, but not all are guaranteed.
- ISOs live on the Hybrid USB's **exFAT** partition; some very old BIOSes may refuse to boot from the USB.
- The Hybrid USB does not boot while Secure Boot is on (see above).

---

## 👩‍💻 For developers

**Needed:** Python 3.9+ ([python.org](https://www.python.org/downloads/), tick *Add Python to PATH*) and optionally [Inno Setup 6](https://jrsoftware.org/isdl.php) (for the Setup).

```text
Run (development):        run_kurboot.bat        (Linux: ./run_kurboot.sh)
Build EXE + Setup:        build_all.bat
Build EXE only:           build_exe.bat
```

### 📦 Publishing a new version

1. In **`kur_version.py`** raise `__version__` (e.g. `"0.4.1"`). *The version number lives only here.*
2. Run **`build_all.bat`** → the `release\` folder gets:
   `KurBoot.exe`, `KurBoot.exe.sha256`, `KurBoot_Setup.exe`, `KurBoot_Setup.exe.sha256`
3. On GitHub → **Releases → Draft a new release** → tag: **`v0.4.1`** (with the leading `v`).
4. Drag the files into **Assets** and click **Publish release**.

> [!IMPORTANT]
> For updates to work: the tag must be higher than the current version (`v0.4.1`), file names must be **exactly** `KurBoot.exe` / `KurBoot_Setup.exe`, and the release must **not be a draft or pre-release**. If a `.sha256` file is attached, KurBoot verifies the download automatically.

With `.github/workflows/release.yml`, `git tag v0.4.1 && git push --tags` makes GitHub build the EXE for you.

---

## 📜 License and credits

- KurBoot's own license: see the `LICENSE` file in the repository.
- The Hybrid menu uses **GNU GRUB** (GPL-3.0+) and **wimboot** (GPL-2.0+). Details: [NOTICE.md](NOTICE.md).
- Windows, Linux and all other names mentioned are trademarks of their respective owners.

<div align="center">

Developer: [@aykutsen1987](https://github.com/aykutsen1987)

</div>
## 👤 Geliştirici

**@aykutsen1987**
[YouTube](https://www.youtube.com/@aykutsen1987) · [Play Store uygulamaları](https://play.google.com/store/search?q=pub%3A%20%40aykutsen1987&c=apps)
