# Üçüncü taraf bileşenler · Third-party components

[🇹🇷 Türkçe](#türkçe) · [🇬🇧 English](#english)

---

## Türkçe

KurBoot Hibrit USB'sinin açılış menüsü şu özgür yazılımları kullanır; lisansları kendilerine aittir.

| Bileşen | Lisans | Kaynak |
|---|---|---|
| GNU GRUB 2 (önyükleyici, `kurboot_boot/`) | GPL-3.0-or-later | https://www.gnu.org/software/grub/ |
| wimboot (Windows WIM önyükleme) | GPL-2.0-or-later | https://github.com/ipxe/wimboot |

GRUB ve wimboot, KurBoot'tan bağımsız programlardır ve kendi lisans koşullarıyla dağıtılır.
Kaynak kodlarına yukarıdaki adreslerden ulaşılabilir. Bu depoya GRUB/wimboot'u yeniden dağıtan bir sürüm
yüklenirse bu koşullar (kaynak koda erişim bilgisi, lisans metni) korunmalıdır.

KurBoot'un kendi kodunun lisansını depo sahibi belirler (`LICENSE` dosyası ekleyin).

Windows, Linux ve adı geçen diğer markalar sahiplerinin tescilli markalarıdır; KurBoot bu kuruluşlarla bağlantılı veya onlar tarafından onaylanmış değildir.

---

## English

The KurBoot Hybrid USB boot menu uses the following free software; their licenses belong to their respective authors.

| Component | License | Source |
|---|---|---|
| GNU GRUB 2 (bootloader, in `kurboot_boot/`) | GPL-3.0-or-later | https://www.gnu.org/software/grub/ |
| wimboot (Windows WIM boot) | GPL-2.0-or-later | https://github.com/ipxe/wimboot |

GRUB and wimboot are separate programs from KurBoot and are distributed under their own license terms.
Their source code is available at the addresses above. If a release that redistributes GRUB/wimboot is
uploaded to this repository, these terms (source-code availability information, license text) must be kept.

The license of KurBoot's own code is chosen by the repository owner (add a `LICENSE` file).

Windows, Linux and other names mentioned are trademarks of their respective owners; KurBoot is not affiliated with or endorsed by them.
