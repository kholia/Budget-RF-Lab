# Ev Yapımı Projeler
İngilizce sürüm: [Home-brew projects](Projects.md).
Lütfen bu projelere eklemek veya buna göre değiştirmek için özgürce ekleyin.

## Başlangıç Projeleri Listesi
Bu deneyebileceğiniz ev yapımı projelerin bir listesini içerir.

| Sıra No | Adı | Montaj Süresi (dakika) | Maliyet (... TL) | Nereden Alınır | Yorumlar | Bağlantılar |
|--------|--------------------------------------|------------------------|---------------|----------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 1 | Topraklama | 2 | ... TL | Yerel | Faz ve toprak arasında sıradan bir 220 V LED ampul ile hızlı bir kaçak kontrolü yapın. | |
| 2 | RF prob | 60 dakika | ... TL | LCSC, Robu, Project Point, Synergy Telecom - Delhi | Telsiz devrelerindeki RF noktalarını güvenle ölçmek için pasif prob. | [Bu makaleyi](https://n5ese.com/rfprobe1.htm) takip ederek bir tane yapın. |
| 3 | Frekans jeneratörü (VFO) | - | ... TL | Yerel / çevrimiçi | Kendi HF/VHF VFO'nuzu kurup telsiz testlerinde kullanın. | Detaylar: https://github.com/kholia/pico-hf-oscillator, Alternatif: Si5351 modülü ile https://github.com/kholia/EasyVFO ve Raspberry Pico 2 kullanarak kısa dalga için bir VFO |
| 4 | Frekans sayacı | 120 | ... TL | - | AF/RF sinyallerini doğrulamak için, osiloskop yoksa pratik. Pico 2'deki 5 V toleranslı pinler büyük kolaylık. | Raspberry Pi Pico 2 ile DIY: https://github.com/kholia/pico_ft8_xcvr/tree/main/PicoFrequencyCounter-v2, https://github.com/kholia/pico_ft8_xcvr/tree/main/PicoFrequencyCounter, https://github.com/richardjkendall/rp2040-freq-counter |
| 5 | Ticari frekans sayacı | - | ... TL | https://rees52.com/ | 9 V beslemeli, 500 MHz'e kadar yüksek hassasiyetli RF frekans sayacı. | İlgili: HF için frekans sayacı tamponu https://www.nutsvolts.com/magazine/article/build-an-rf-frequency-counter-buffer-for-hf |
| 6 | Frekans referansı | 15 | ... TL | - | Telsiz ölçümlerini ortak bir referansa bağlamak için kullanın. | DIY: https://github.com/kholia/uBlox7_TimePulse |
| 7 | 10 mW WSPR / FT8 / CW RF işaretçisi | 2 | ... TL | - | Yerel sahte/yedek telsiz test işaretçisi; laboratuvar içi denemeler için. | https://github.com/kholia/Easy-Digital-Beacons-v1, https://github.com/kholia/Pico-FT8-TX |
| 8 | Yerel SSB sinyal kaynağı | 15 | ... TL | - | Tek bir kablo lehimleyip bağlamak yeterli, düşük güçlü telsiz testleri için. | https://github.com/kholia/rpitx |
| 9 | RF sahte yük (dummy load) | 30 | ... TL | - | 50 ohm flanş direnç + alüminyum soğutucu ile düşük güç telsiz testleri. | |

## RF telsiz güvenliği genişletilmiş listesi

- **HackRF One**

- **CC1101 SPI modülü (iki)**

  - https://www.ktron.in/product/cc1101-433mhz-module/

- **Mantık analizörü seçenekleri**

  - DIY kullanarak Raspberry Pi Pico

    https://github.com/pico-coder/sigrok-pico

  - [Alternatif 1] DIY kullanarak Raspberry Pi Pico

    https://github.com/gusmanb/logicanalyzer

  - [Alternatif 2] https://robu.in/product/usb-logic-analyze-24m-8ch-mcu-arm-fpga-dsp-debug-tool/

- **Hata enjeksiyonu**

  - https://github.com/MKesenheimer/fault-injection-library

## Eğlenceli Aktiviteler

- **30 dakika içinde HF'ye başlamak istiyorum, nasıl yaparım?**

  Bir Raspberry Pi Pico 2 MCU kartı kullanarak 10m bandı için 10mW WSPR işaretçisi yapın.

  https://github.com/kholia/Easy-Beacons-STEM kullanın.

  Alternatif: Zaten bir Raspberry Pi SBC'ye mi sahipsiniz? O zaman https://github.com/JamesP6000/WsprryPi'yi deneyin.

- **Bugün HF trafiğini dinlemeye başlamak istiyorum, nasıl yaparım?**

  - RTL-SDR v3 + rastgele tel / aktif anten

  - CD2003 alıcı (< ... TL) + rastgele tel / aktif anten

    Daha fazla ayrıntı için bkz. https://github.com/kholia/ConsensusBasedTimeSync
