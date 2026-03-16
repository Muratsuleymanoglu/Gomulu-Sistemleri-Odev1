# Gomulu-Sistemleri-Odev1

Bu repository, Gömülü Sistemler dersi kapsamında hazırlanan ilk ödev çalışmasını içermektedir. Proje, STM32F103 (Blue Pill) geliştirme kartı üzerinde temel giriş/çıkış işlemleri ve hata ayıklama (debug) tekniklerinin uygulanmasını kapsamaktadır.


## 📋 Proje Özeti
Proje kapsamında STM32F103C8T6 mikrodenetleyicisi üzerinde yer alan kullanıcı LED'i (PC13), 500ms yanık ve 500ms sönük kalacak şekilde (1 saniye periyotla) programlanmıştır. Çalışma; donanım yapılandırması, kod geliştirme, derleme ve donanım üzerinde hata ayıklama aşamalarından oluşmaktadır.

## 🛠️ Kullanılan Teknolojiler ve Araçlar
Donanım: STM32F103C8T6 (Blue Pill), ST-Link V2 Debugger.

Geliştirme Ortamı: Visual Studio Code (VS Code).

Derleyici: GNU Arm Embedded Toolchain (arm-none-eabi-gcc).

Yapılandırma: STM32CubeMX (Makefile tabanlı proje yönetimi).

Hata Ayıklayıcı: OpenOCD & Cortex-Debug.

## 📁 Proje Yapısı
Core/Src/main.c: HAL kütüphanesi kullanılarak LED Toggle ve Gecikme komutlarının yazıldığı ana uygulama dosyası.

Drivers/: Mikrodenetleyiciye özgü donanım soyutlama katmanı (HAL) kütüphaneleri.

Makefile: Projenin derleme parametrelerini ve dosya bağımlılıklarını yöneten yapı.

.vscode/launch.json: VS Code üzerinde canlı hata ayıklama (Step-by-step Debug) için yapılandırılmış debugger ayarları.

## 💻 Uygulama ve Deney Süreci
Pin Yapılandırması: CubeMX üzerinden PC13 pini GPIO_Output olarak atanmış ve sistem saati (Clock) yapılandırılmıştır.

Derleme (Build): Terminal üzerinden make komutu çalıştırılarak build/ dizini altında .elf ve .bin dosyaları üretilmiştir.

Yükleme (Flash): OpenOCD aracı yardımıyla hazırlanan firmware ST-Link üzerinden MCU flash belleğine yazılmıştır.

Hata Ayıklama (Debug): Kodun kritik satırlarına Breakpoint eklenerek program akışı durdurulmuş, işlemci kayıtçıları ve pin durumları canlı olarak gözlemlenmiştir.

## 🎥 Uygulama Videosu
Projenin çalışma kanıtı ve debug aşamalarını içeren YouTube videosuna aşağıdaki bağlantıdan ulaşabilirsiniz:

https://youtu.be/36EJ7ECZdhY 

