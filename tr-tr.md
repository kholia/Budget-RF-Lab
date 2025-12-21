# Bütçe RF Laboratuvarı
İngilizce sürüm: [Budget RF Lab](README.md).

Ev yapımı radyo frekansı (RF) laboratuvarı için bütçe dostu bir rehber. Bu depo, bir `Bilgi Sistemleştirme (SoK)` seti olarak tasarlanmıştır.

Aşağıdaki gibi organize edilmiştir:
- Ekipman listesi: Coğrafyanız veya diliniz için katkıda bulunmak istiyorsanız lütfen uygun markdown dosyasını oluşturun. Örnek olarak [Türkiye için Türkçe versiyon](tr-tr.md) mevcuttur.
- [FLOSS Araçları](FLOSS_Tools.md): Kullanabileceğiniz tüm araçları içerir.
- [Projeler](Projects.md): Başlamanız için bir proje listesi.
- [RF Parçaları](RFParts.md): RF iletişim projeleri için kullanışlı hacker parçalarının bir listesi.

## Ülkeniz için Kontrol Edin

| Coğrafya | Dil | Bağlantı |
|----------|-----|----------|
| Hindistan | İngilizce | [en_in](en_in.md) |
| Türkiye  | Türkçe  | [tr-tr](tr-tr.md) |

## Ev Yapımı Projeler
Lütfen bu projelere eklemek veya buna göre değiştirmek için özgürce ekleyin.

### Başlangıç Projeleri Listesi
Bu deneyebileceğiniz ev yapımı projelerin bir listesini içerir.

| Sıra No | Adı                                 | Montaj Süresi (dakika) | Maliyet (... TL) | Nereden Alınır                                       | Yorumlar                                                                                                                                                               | Bağlantılar                                                                                                                                                                                                                                                           |
|--------|--------------------------------------|------------------------|---------------|----------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 1      | Topraklama                             | 2                      | ... TL            | Yerel                                              | Faz ve toprak arasında sıradan bir 220 V LED ampul ile hızlı kaçak testi yapın.                                                                          |                                                                                                                                                                                                                                                                 |
| 2      | RF prob                              | 60 dakika             | ... TL          | LCSC, Robu, Project Point, Synergy Telecom - Delhi | Telsiz devrelerindeki RF noktalarını güvenle ölçmek için pasif prob.                                                                                                                                                                        | [Bu makaleyi](https://n5ese.com/rfprobe1.htm) takip ederek bir tane yapın.                                                                                                                                                                                          |
| 3      | Frekans jeneratörü (VFO)            | -                      | ... TL       | Yerel / çevrimiçi                                                 | HF/VHF için kendi VFO'nuzu kurup telsiz testlerinde kullanın.                                                                                                                                                                        | Detaylar: https://github.com/kholia/pico-hf-oscillator, Alternatif: Si5351 modülü kullanarak https://github.com/kholia/EasyVFO ve Raspberry Pico 2 ile kısa dalga VFO                                                 |
| 4      | Frekans sayacı                    | 120                      | ... TL       |                                                    | Osiloskop yoksa AF/RF sinyallerini doğrulamak için pratik. Pico 2'deki 5 V toleranslı pinler büyük kolaylık. | DIY: Raspberry Pi Pico 2 ile https://github.com/kholia/pico_ft8_xcvr/tree/main/PicoFrequencyCounter-v2, https://github.com/kholia/pico_ft8_xcvr/tree/main/PicoFrequencyCounter, https://github.com/richardjkendall/rp2040-freq-counter |
| 5      | Ticari frekans sayacı         | -                      | ... TL          | https://rees52.com/                                | 9 V beslemeli, 500 MHz'e kadar yüksek hassasiyetli RF frekans sayacı.                                                                                                                    | İlgili: HF için bir RF frekans sayacı tamponu yapın https://www.nutsvolts.com/magazine/article/build-an-rf-frequency-counter-buffer-for-hf                                                                                                                      |
| 6      | Frekans referansı                  | 15                     | ... TL               |                                                    | Telsiz ölçümlerini ortak bir referansa bağlamak için kullanın.                                                                                                                                                                        | DIY: https://github.com/kholia/uBlox7_TimePulse projesi                                                                                                                                                                                                    |
| 7      | 10 mW WSPR / FT8 / CW RF işaretçisi | 2                      | ... TL          |                                                    | Laboratuvar içi denemeler için düşük güçlü yerel işaret kaynağı.                                                                                                                                                                        | https://github.com/kholia/Easy-Digital-Beacons-v1, https://github.com/kholia/Pico-FT8-TX                                                                                                                                                                        |
| 8      | Yerel SSB sinyal kaynağı              | 15                     | ... TL               |                                                    | Tek bir tel lehimleyip takmak yeterli; düşük güçlü telsiz testleri için uygun.                                                                                                                           | https://github.com/kholia/rpitx                                                                                                                                                                                                                                 |
| 9      | RF sahte yük (dummy load)                        | 30                     | ... TL       |                                                    | 50 ohm RF flanş direnci + uygun bir alüminyum soğutucu ile kendi sahte yükünüzü yapın.                                                                                                |                                                                                                                                                                                                                                                                 |

## RF telsiz güvenliği genişletilmiş liste

- HackRF One

- CC1101 SPI modülü (iki)

  - https://www.ktron.in/product/cc1101-433mhz-module/

- Mantık analizörü seçenekleri

  - DIY kullanarak Raspberry Pi Pico

    https://github.com/pico-coder/sigrok-pico

  - [Alternatif 1] DIY kullanarak Raspberry Pi Pico

    https://github.com/gusmanb/logicanalyzer

  - [Alternatif 2] https://robu.in/product/usb-logic-analyze-24m-8ch-mcu-arm-fpga-dsp-debug-tool/

- Hata enjeksiyonu

  - https://github.com/MKesenheimer/fault-injection-library

## Eğlenceli Aktiviteler

- 30 dakika içinde HF'ye başlamak istiyorum, nasıl yaparım?

  Bir Raspberry Pi Pico 2 MCU kartı kullanarak 10m bandı için 10mW WSPR işaretçisi yapın.

  https://github.com/kholia/Easy-Beacons-STEM kullanın.

  Alternatif: Zaten bir Raspberry Pi SBC'ye mi sahipsiniz? O zaman https://github.com/JamesP6000/WsprryPi'yi deneyin.

- Bugün HF trafiğini dinlemeye başlamak istiyorum, nasıl yaparım?

  - RTL-SDR v3 + rastgele tel / aktif anten

  - CD2003 alıcı (< ... TL) + rastgele tel / aktif anten

    Daha fazla ayrıntı için bkz. https://github.com/kholia/ConsensusBasedTimeSync

## Yazılım (FLOSS)

- LTspice - Fikirlerinizi LTspice kullanarak kontrol edin

- Elsie (https://tonnesoftware.com/elsie.html) filtre tasarımı için yaygın kullanılan bir araç.

- http://www.ke5fx.com/aadeflt.htm - AADE Filtre Tasarımı V4.5

- https://www.dl0hst.de/mini-ringkern-rechner.htm#en

- https://coil32.net/ - bobin endüktans hesaplama uygulaması

- KiCad EDA (https://www.kicad.org/) (EAGLE durduruldu; açık kaynak EDA tercihimizdir.)

- LibrePCB (https://librepcb.org/) Açık kaynaklı PCB tasarım yazılımı

- FreeCAD (https://www.freecad.org/) Katı modelleme, 3-D baskılı parçalar yapmak için kullanışlı

- Verilator (https://www.veripool.org/verilator/) Verilog simülatörü

- Icarus (https://steveicarus.github.io/iverilog/) Verilog simülatörü

- Ngspice (https://ngspice.sourceforge.io/) SPICE devre simülasyon motoru

- Epsilon Forge (https://www.epsilonforge.com/post/open-source-electromagnetics/) Elektromanyetik modelleyici

- OpenEMS (https://www.openems.de/) Açık kaynaklı FDTD modelleyici

- GNU Octave (https://octave.org/) MATLAB benzeri sayısal işleme dili ve ortamı

- Anaconda (https://www.anaconda.com/) Python tabanlı sayısal hesaplama ortamı

## Katkıda Bulunanlar

- [Telegram'daki HAMBREWERS grubundan](https://t.me/+TwzGyKGe8_QI_B3y) kişiler

- https://voidstarsec.com/hw-hacking-lab/vss-lab-guide

- VU2ESE - Ashhar Farhan LARC 2024'te ev yapımı radyoya başlamak hakkında konuştu.

- R2BDY - Roman

- VU2TNA - Sanal Kumar G

- TA1JS - Buğra

## Katkı Sağlayanlar

- VU3CER - Dhiru

- VU3GLJ - Bharath

- TA1JS - Buğra

## Referanslar

- https://github.com/kholia/HF-Balcony-Antenna-System

- https://github.com/kholia/talks/

- https://www.kk5jy.net/three-wire-gp/

- https://www.pa0fri.com/ (aktif alan anten)

## Ekipman Listesi

*Lütfen bu listenin yardımcı olmak amacıyla derlendiğini ve bu makalede yer alan herhangi bir satıcı veya bağlantının ticari bir onayı olmadığını unutmayın.*

| Sıra No | Adı                                                                                 | Maliyet (... TL)                                                                                                 | Nereden Alınır                                                              | Yorumlar                                                                                                                                                               | Bağlantılar                                                                                                                                                                                                                                                           |
|--------|--------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 1      | Havya                                                                     | BABA i12 havya ... TL; IKO mikro havya istasyonu– 12V ... TL; Soldron 25W ... TL           |                                                                            | Profesyonel ipucu: İyi havya uçlarına ve seramik uçlara yatırım yapın; düşük fiyatlı olanlar ısınmak için zaman alır ama bu genelde sorun değildir.                      |                                                                                                                                                                                                                                                                 |
| 2      | Multimetre                                                                           | UNI-T UT33D+ ... TL; Mastech MAS830L Dijital Multimetre ... TL                                                  | https://www.toolworld.in, https://robu.in/                                 |                                                                                                                                                                        |                                                                                                                                                                                                                                                                 |
| 3      | Doğrusal güç kaynağı seçenekleri                                                     | SUGON 3005D Ayarlanabilir DC Güç Kaynağı (30V~5A) ... TL; SUGON 3010PM Ayarlanabilir Güç Kaynağı (30V~10A) ... TL |                                                                            | CC CV işlevselliği, deneyleri güvenli bir şekilde yürütmek için gereklidir!                                                                                          |                                                                                                                                                                                                                                                                 |
| 4      | Kapasitans metre                                                                     | MS8910 Mastech SMD Ölçüm Cımbızları ... TL                                                                  |                                                                            | VU2ESE de Mastech MS8910 kullanıyor                                                                                                                                         |                                                                                                                                                                                                                                                                 |
| 5      | Osiloskop                                                                           | ~... TL                                                                                          |                                                                            | Herhangi bir >= 100 MHz Siglent osiloskop bütçenize uygundur. En azından bir DSO alın. Rigol osiloskoplar da iyidir. Owon osiloskoplar düşük bütçe için uygundur.                  |                                                                                                                                                                                                                                                                 |
| 6      | NanoVNA                                                                              | ... TL                                                                                                              | https://www.banggood.in/                                                   |                                                                                                                                                                        |                                                                                                                                                                                                                                                                 |
| 7      | TinySA (Ultra)                                                                       | ... TL                                                                                                              | https://www.banggood.in/                                                   | Zayıflatıcıları 3/6/10 dB seti olarak edinin; RF telsiz ölçümleri için yeterlidir.                                                                                    |                                                                                                                                                                                                                                                                 |
| 8      | RF güç + SWR metre                                                                   | Diamond SX20C Güç Metre ... TL                                                                                     | https://www.sanchartelesystems.com/                                        | RF çalışmaları için çapraz iğne güç ve swr metre çok kullanışlıdır.                                                                                        |                                                                                                                                                                                                                                                                 |
| 9      | Sıcak hava istasyonu seçenekleri                                                    | ... TL                                                                                                              | https://g2mark.com/ ve https://babaocamachine.com/ çeşitli seçeneklere sahip.  |                                                                                                                                                                        |                                                                                                                                                                                                                                                                 |
| 10     | SDR Seçenekleri                                                                      | ... TL                                                                                                   | https://www.rtl-sdr.com/buy-rtl-sdr-dvb-t-dongles/                         | Önerilen modeller: RTL-SDR v3/v4, Airspy HF+ Discovery; Airspy HF+ Discovery, HF bandı dinlemede oldukça başarılıdır.                                                                                                   |                                                                                                                                                                                                                                                                 |
| 11     | Jumper kabloları                                                                     | ... TL                                                                                                              | Project Point                                                              | Yüksek kaliteli olanları satın alın, zaman kazandırır.                                                                                                                     |                                                                                                                                                                                                                                                                 |
| 12     | Lehim sökme örgüsü (wick)                                                           | ... TL                                                                                                              |                                                                            | Chemtronics markalı olanları Otovon satıcısından satın alın                                                                                                        |                                                                                                                                                                                                                                                                 |
| 13     | Büyütme                                                                             | ... TL                                                                                                              | https://g2mark.com/ ve https://babaocamachine.com/ çeşitli seçeneklere sahip.  | Sıkışık bir durumda, LED aydınlatmalı temel bir büyütme düzeni yaklaşık ... TL civarı başlar ve ihtiyaçlarınıza göre yükseltebilirsiniz.               |                                                                                                                                                                                                                                                                 |
| 14     | Lehim teli                                                                          | ... TL                                                                                                              |                                                                            | İhtiyacımız olan şey 22 SWG "60/40" karışımı rosin çekirdekli lehim teli, daha ince SMD bileşenleri lehimlemek için 0.3mm lehim teli (2UUL veya Mechanic markalı)             |                                                                                                                                                                                                                                                                 |
| 15     | Hat Test Cihazı                                                                      | ~... TL                                                                                                           |                                                                            | 400V'a kadar ölçüm aralığı                                                                                                                                           |                                                                                                                                                                                                                                                                 |
| 16     | Mengene / PCB Mengenesi                                                              | ... TL                                                                                                       |                                                                            | Taparia vb. markaların temel mengeneleri yerel hırdavatçılarda bulunur.                                                                                               |                                                                                                                                                                                                                                                                 |
| 17     | Donanım araçları                                                                     | ... TL                                                                                                              |                                                                            | ESD güvenli cımbızlar, burun pense, tornavida seti, yan kesiciler, küçük kıskaçlar; Taparia, Stanley, Miniso vb. setler iş görür.   |                                                                                                                                                                                                                                                                 |
| 18     | LCR metre DE-5000                                                                    | ... TL (eBay, ithalat vergileri eklenir)                                                                        |                                                                            | Oldukça iyi incelenmiş ve güvenilir                                                                                                                    |                                                                                                                                                                                                                                                                 |
| 19     | Lehim Akısı                                                                          | ... TL                                                                                                           |                                                                            |                                                                                                                                                                        |

## RF telsiz güvenliği genişletilmiş liste

- HackRF One

- CC1101 SPI modülü (iki)

- Mantık analizörü seçenekleri

  - DIY kullanarak Raspberry Pi Pico

    https://github.com/pico-coder/sigrok-pico

  - [Alternatif 1] DIY kullanarak Raspberry Pi Pico

    https://github.com/gusmanb/logicanalyzer

  - [Alternatif 2] https://robu.in/product/usb-logic-analyze-24m-8ch-mcu-arm-fpga-dsp-debug-tool/

- Hata enjeksiyonu

  - https://github.com/MKesenheimer/fault-injection-library

## Yazılım (Ücretsiz / FOSS)

- LTspice - Fikirlerinizi LTspice kullanarak kontrol edin

- Elsie (https://tonnesoftware.com/elsie.html) filtre tasarımı için yaygın kullanılan bir araç.

- http://www.ke5fx.com/aadeflt.htm - AADE Filtre Tasarımı V4.5

- https://www.dl0hst.de/mini-ringkern-rechner.htm#en

- https://coil32.net/ - bobin endüktans hesaplama uygulaması

- KiCad EDA (EAGLE durduruldu; açık kaynak EDA tercihimizdir.)

## Eğlenceli Aktiviteler

- 30 dakika içinde HF'ye başlamak istiyorum, nasıl yaparım?

  Bir Raspberry Pi Pico 2 MCU kartı kullanarak 10m bandı için 10mW WSPR işaretçisi yapın.

  https://github.com/kholia/Easy-Beacons-STEM kullanın.

  Alternatif: Zaten bir Raspberry Pi SBC'ye mi sahipsiniz? O zaman https://github.com/JamesP6000/WsprryPi'yi deneyin.

- Bugün HF trafiğini dinlemeye başlamak istiyorum, nasıl yaparım?

  - RTL-SDR v3 + rastgele tel / aktif anten

  - CD2003 alıcı (< ... TL) + rastgele tel / aktif anten

    Daha fazla ayrıntı için bkz. https://github.com/kholia/ConsensusBasedTimeSync
