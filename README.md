# ⚔️ İnsan İmparatorluğu vs Ork Lejyonu - Savaş Simülasyonu

Bu proje, **C programlama dili** kullanılarak geliştirilmiş, web tabanlı senaryo yönetimi ve **Raylib** görselleştirme altyapısına sahip stratejik bir savaş simülasyonudur.

Proje, İnsan İmparatorluğu ve Ork Lejyonu arasındaki savaşları; birim istatistikleri, kahraman bonusları, yaratık etkileri ve teknoloji araştırmalarını hesaba katarak tur tabanlı olarak simüle eder.

![Dil](https://img.shields.io/badge/Dil-C-blue)
![Kütüphane](https://img.shields.io/badge/Görselleştirme-Raylib-red)
![Kütüphane](https://img.shields.io/badge/Ağ-libcurl-orange)
![Lisans](https://img.shields.io/badge/Lisans-MIT-green)

## 📋 Proje Özellikleri

* **🌐 Dinamik Senaryo Yönetimi:** `libcurl` entegrasyonu sayesinde, sunucu üzerinden (örn: yapbenzet.org.tr) güncel savaş senaryoları (JSON formatında) anlık olarak çekilir.
* **📊 Detaylı Veri Ayrıştırma:**
    * **Birimler:** Piyadeler, Okçular, Süvariler, Kuşatma Makineleri, Troller, Varg Binicileri vb.
    * **Kahramanlar:** Fatih Sultan Mehmet, Mete Han, Goruk Vahşi gibi tarihi ve kurgusal karakterlerin orduya etkileri.
    * **Yaratıklar:** Ejderhalar, Gölge Kurtları gibi mitolojik unsurların savaşın seyrine etkisi.
* **🎨 Raylib Görselleştirme:** Savaş öncesi ve sonrası orduların durumu, birim sayıları ve sağlık barları grafiksel arayüzde (GUI) canlı olarak gösterilir.
* **⚔️ Savaş Mekaniği:**
    * Saldırı/Savunma bonusları hesaplaması.
    * Kritik vuruş şansları.
    * Araştırma seviyelerinin (Saldırı, Savunma, Elit Eğitim) etkileri.
    * Tur bazlı hasar dağılımı ve "net hasar" hesaplamaları.
* **📝 Raporlama:** Tüm savaş süreci `savas_sim.txt` dosyasına detaylı loglar halinde kaydedilir.

## 🛠️ Gereksinimler

Projeyi derlemek ve çalıştırmak için sisteminizde aşağıdaki bileşenlerin bulunması önerilir:

* **GCC Compiler** (MinGW-w64 önerilir)
* **Raylib** Kütüphanesi (Grafik arayüz için)
* **libcurl** Kütüphanesi (HTTP istekleri için)

## 🚀 Kurulum ve Derleme

1.  Repoyu yerel makinenize klonlayın:
    ```bash
    git clone [https://github.com/kullaniciadiniz/proje-isminiz.git](https://github.com/kullaniciadiniz/proje-isminiz.git)
    ```

2.  Kütüphane dosyalarınızın (header ve lib dosyaları) doğru dizinlerde olduğundan emin olun.

3.  Projeyi derlemek için terminalde şu komutu kullanabilirsiniz (Gerekli path ayarlarını kendi sisteminize göre yapınız):

    ```bash
    gcc main.c -o WarSim.exe -O2 -Wall -Wno-missing-braces -I include/ -L lib/ -lraylib -lcurl -lgdi32 -lwinmm
    ```

## 🎮 Nasıl Kullanılır?

1.  `WarSim.exe` uygulamasını çalıştırın.
2.  Konsol ekranında listelenen senaryolardan birini seçmek için **1 ile 10 arasında bir sayı** girin.
3.  Program senaryoyu sunucudan indirecek ve simülasyonu başlatacaktır.
4.  **Raylib penceresi** açılarak orduların görsel durumunu sergileyecektir.
5.  Savaş sonuçları ve tur detayları proje klasöründeki `savas_sim.txt` dosyasına yazılacaktır.

## 📂 Dosya Yapısı

```text
Proje_Dizini/
│
├── main.c                  # Simülasyonun ana kaynak kodu
├── Files/                  # Oyun verilerini içeren JSON dosyaları
│   ├── heroes.json         # Kahraman özellikleri
│   ├── unit_types.json     # Birim temel güçleri
│   ├── creatures.json      # Yaratık bonusları
│   └── research.json       # Teknoloji seviyeleri
├── include/                # Kütüphane başlık dosyaları (.h)
├── *.png                   # Görsel varlıklar (Karakter resimleri)
└── savas_sim.txt           # Simülasyon çıktı dosyası
