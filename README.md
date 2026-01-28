⚔️ İnsan İmparatorluğu vs Ork Lejyonu - Savaş Simülasyonu
Bu proje, C programlama dili kullanılarak geliştirilmiş, JSON tabanlı veri okuma, web üzerinden senaryo çekme ve Raylib kütüphanesi ile görselleştirme özelliklerine sahip kapsamlı bir stratejik savaş simülasyonudur.

İnsan İmparatorluğu ve Ork Lejyonu arasındaki epik savaşları; birim türleri, kahramanlar, canavarlar ve araştırma seviyelerine göre simüle eder.

📋 Özellikler
Dinamik Senaryo Yükleme: libcurl kullanılarak sunucudan (örn: kocaeli.edu.tr) güncel savaş senaryoları (JSON) çekilir.

Gelişmiş JSON Ayrıştırma: Birimler, kahramanlar, yaratıklar ve araştırmalar yerel JSON dosyalarından okunur.

Görsel Arayüz (Raylib): Savaş öncesi ve sonrası orduların durumu, sağlık barları ve birim sayıları grafiksel olarak ekrana çizdirilir.

Detaylı Savaş Mekaniği:

Birimler: Piyadeler, Okçular, Süvariler, Kuşatma Makineleri vs. Ork Dövüşçüleri, Troller, Varg Binicileri.

Bonuslar: Kahraman (örn: Fatih Sultan Mehmet, Goruk Vahşi) ve Canavar etkileri.

Araştırmalar: Saldırı, Savunma, Kritik Vuruş şansı gibi yükseltmeler.

Hesaplama: Saldırı/Savunma puanları, kritik vuruşlar ve net hasar hesaplamalarıyla tur tabanlı simülasyon.

Loglama: Savaşın her adımı detaylı bir şekilde savas_sim.txt dosyasına raporlanır.

🛠️ Gereksinimler
Projeyi derlemek ve çalıştırmak için aşağıdaki kütüphanelere ve araçlara ihtiyacınız vardır:

GCC Compiler (MinGW veya benzeri)

Raylib (Grafik arayüzü için)

libcurl (Ağ işlemleri için)

Windows ortamı (Kod yapısı windows.h bağımlılıkları içerir)

🚀 Kurulum ve Derleme
Bu repoyu klonlayın:

git clone https://github.com/kullaniciadiniz/proje-isminiz.git
Gerekli kütüphanelerin (include ve lib dosyaları) proje dizininde olduğundan emin olun.

Projeyi derleyin (Örnek GCC komutu):

gcc main.c -o SavasSimulasyonu.exe -O2 -Wall -Wno-missing-braces -I include/ -L
