# Antivirüs / SmartScreen Bilgilendirmesi

XandyX DPI'yi ilk kez kurarken Windows veya antivirüsünüz uyarı verebilir.
Bu, bu tür araçlarda **beklenen ve normal** bir durumdur — aşağıda nedenini
ve güvenli olduğunu nasıl doğrulayacağınızı anlatıyoruz.

## Neden uyarı veriyor?

1. **İmza sertifikası henüz yok.** Microsoft, tanımadığı yeni dosyaları
   SmartScreen ile durdurur. Sertifika + indirme sayısı + zamanla bu uyarı
   kaybolur (itibar sistemi).
2. **Sezgisel tarama.** Uygulama yerel proxy çalıştırıp sistem proxy ayarını
   değiştirir; antivirüsler bu *davranış kalıbını* genel olarak şüpheli sayar.
3. **Yeni dosya.** Hiçbir itibar veritabanında kaydı olmayan her yeni exe
   ilk haftalarda daha sık işaretlenir.

## Neden güvenli taraftayız?

- 📦 **Sürücü (driver) yok.** Alarm veren araçların çoğu kernel sürücüsü
  kullanır (örn. WinDivert); XandyX DPI yalnızca normal kullanıcı programıdır.
- 🔑 **Yönetici yetkisi istemez.** Kurulum da çalıştırma da onaysız yapılır.
- 🏠 Yalnızca kendi bilgisayarınızı dinler (`yerel adres`), dışarıya port açmaz.
- ↩️ Proxy ayarınızı kapatınca / çıkınca **otomatik geri alır**; internetiniz
  bozuk kalmaz.
- 📡 Trafiğinizi toplayan bir sunucumuz yok; çevrimiçi sayacı anonim Nostr
  nabzıdır ve kapatılabilir.

## Nasıl doğrularsınız?

1. `Get-FileHash` ile SHA256 özetini [SHA256SUMS.txt](SHA256SUMS.txt) ile
   karşılaştırın (bkz. README).
2. Dosyayı [VirusTotal](https://www.virustotal.com/)'e yükleyin. 1-2 motordan
   gelen `PUA / Heuristic / Generic` türü sonuçlar, yukarıdaki sebeplerden
   ötürü bu tür araçlarda tipiktir.
3. SmartScreen çıkarsa: **Ek bilgi → Yine de çalıştır**.

## Yanlış alarm bildirimi (uyarı alanlar için)

Kullandığınız antivirüs dosyayı karantinaya alırsa, ilgili üreticiye
"yanlış pozitif (false positive)" bildirimi yapabilirsiniz:

- Microsoft Defender: https://www.microsoft.com/en-us/wdsi/filesubmission
- Avast / AVG: https://www.avast.com/false-positive-file-form.php
- Kaspersky: https://opentip.kaspersky.com/
- ESET: https://www.eset.com/int/support/contact/
- Malwarebytes: https://www.malwarebytes.com/false-positive-form
- Norton: https://submit.norton.com/

Her bildirim, tüm kullanıcılar için uyarıların kalkmasını hızlandırır. 🙏
