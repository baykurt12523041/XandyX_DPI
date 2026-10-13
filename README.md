# XandyX DPI

Tek tuşla DPI (Derin Paket İnceleme) atlatma. VPN yok, sürücü yok, yönetici yetkisi yok.

## Özellikler

- 🛡️ **Tek tuş koruma** — SNI split + TLS record split + şifreli DNS (DoH)
- 🟢 **Canlı çevrimiçi sayacı** — Nostr üzerinden, merkezi sunucu yok, tamamen anonim
- ⚙️ Bilgisayar açılışında başlatma, tepsiye küçültme
- ✨ Modern animasyonlu arayüz + sistem tepsisi menüsü
- 🔌 Yönetici yetkisi **istemez**, sürücü **kurmaz**, proxy ayarlarınızı kapatınca **geri alır**

## Kurulum

1. Aşağıdan `XandyX DPI Setup 0.4.0.exe` dosyasını indirin.
2. Çift tıklayıp kurun. Windows SmartScreen *"bilgisayarınızı korudu"* derse:
   **Ek bilgi → Yine de çalıştır** (nedeni: [ANTIVIRUS.md](ANTIVIRUS.md)).
3. Uygulamada **BAŞLAT**'a basın, ardından Discord / tarayıcınızı yeniden başlatın.

> Gereksinim: Windows 10+ (x64). Kurulum ve çalıştırma için yönetici yetkisi gerekmez.

## Dosya doğrulama

İndirdiğiniz dosyanın bozulmadığını / değiştirilmediğini doğrulayın:

```powershell
Get-FileHash "XandyX DPI Setup 0.4.0.exe" -Algorithm SHA256
```

Çıkan özeti [SHA256SUMS.txt](SHA256SUMS.txt) içindekiyle karşılaştırın.
Ekstra için dosyayı [VirusTotal](https://www.virustotal.com/)'de taratabilirsiniz.

## Gizlilik

- Trafiğiniz bizim sunucularımızdan geçmez — **sunucumuz yok**. Proxy yalnızca
  kendi bilgisayarınızda (`yerel`) çalışır, sitelere doğrudan bağlanılır.
- Üstteki çevrimiçi sayısı için Nostr'a **anonim nabız** gönderilir (rastgele kimlik,
  hesap yok, konum yok). Ayarlar → *Çevrimiçi sayacını paylaş* ile kapatılabilir.
- Alan adı istekleri şifreli DNS (DoH) ile çözülür; sahte DNS cevapları reddedilir.

## Yasal ve sorumlu kullanım

XandyX DPI, haksız sansür uygulanan yerlerde özgür internete erişim içindir.
Bulunduğunuz ülkenin yasalarına uymak sizin sorumluluğunuzdur.

## Sürüm

**v0.4.0** — Windows 10+ (x64)
