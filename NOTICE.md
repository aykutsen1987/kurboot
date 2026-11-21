# Üçüncü taraf bileşenler

KurBoot Hibrit USB'sinin açılış menüsü şu özgür yazılımları kullanır; lisansları kendilerine aittir.

| Bileşen | Lisans | Kaynak |
|---|---|---|
| GNU GRUB 2 (önyükleyici, `kurboot_boot/`) | GPL-3.0-or-later | https://www.gnu.org/software/grub/ |
| wimboot (Windows WIM önyükleme) | GPL-2.0-or-later | https://github.com/ipxe/wimboot |

GRUB ve wimboot, KurBoot'tan bağımsız programlardır ve kendi lisans koşullarıyla dağıtılır.
Kaynak kodlarına yukarıdaki adreslerden ulaşılabilir. Bu depoya GRUB/wimboot'u yeniden dağıtan bir sürüm
yüklenirse bu koşullar (kaynak koda erişim bilgisi, lisans metni) korunmalıdır.

KurBoot'un kendi kodunun lisansını depo sahibi belirler (`LICENSE` dosyası ekleyin).
