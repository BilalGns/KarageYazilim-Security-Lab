# 🛡️ Karage Security OS (Ultimate Edition)

![Platform](https://img.shields.io/badge/Platform-Android-green) ![Language](https://img.shields.io/badge/Language-Java-orange) ![Type](https://img.shields.io/badge/Type-Pentest_Tool-red) ![Status](https://img.shields.io/badge/Status-Stable-blue)

**Karage Security OS**, Android cihazlar için geliştirilmiş, **Root yetkisi gerektirmeyen**, tamamen yerel (Native Java) çalışan hibrit bir siber güvenlik ve analiz laboratuvarıdır.

Klasik simülasyonların aksine, **gerçek TCP soketleri** ve **HTTP protokolü** üzerinden hedef sistemlerle etkileşime girer. İçerisinde ağ keşif araçları, web zafiyet tarayıcıları ve veri analiz modülleri bulunur.

---

## 🚀 Öne Çıkan Özellikler

Bu proje, Android'in güvenlik kısıtlamalarını (Sandbox) aşarak maksimum verimlilik sağlamak için özel teknikler kullanır:

### 🔥 1. Özel Modüller
* **🕵️ Stealth Mode (Hayalet Modu):** WAF (Web Application Firewall) atlatmak için her istekte otomatik olarak **User-Agent Rotasyonu** yapar (iPhone, Windows, Linux gibi davranır).
* **👀 Traffic Logger (Burp Lite):** Uygulamanın yaptığı tüm HTTP isteklerini (Request) ve sunucudan dönen cevapları (Response) canlı olarak ekrana basar.

### ⚔️ 2. Red Team (Saldırı & Keşif)
* **SQL Injection Scanner:** Hedef URL'de Error-Based SQLi zafiyeti arar.
* **XSS Scanner:** Reflected XSS açıklarını tespit eder.
* **Admin Panel Finder:** Admin, cpanel, wp-admin gibi gizli giriş yollarını brute-force ile bulur.
* **Web Crawler:** Hedef sitedeki tüm linkleri (`<a href>`) kazır.
* **Port Scanner:** Çoklu thread (25 Thread) kullanarak TCP Connect taraması yapar.
* **Lan Scanner:** Yerel ağdaki (Wi-Fi) aktif cihazları tespit eder (Ping Sweep).

### 🛠️ 3. Analyst (Veri & Analiz)
* **HTTP Header Analyzer:** Sunucu güvenlik başlıklarını ve versiyon bilgilerini çeker.
* **Data Tools:** JSON Formatter, Regex Tester, Base64 Encoder/Decoder, Hash Generator (MD5/SHA1).
* **Recon:** Whois, DNS Lookup, Ping, Public IP & Geo Location.

---

## 💻 Teknik Detaylar

Bu proje, hazır kütüphaneler yerine **Core Java** yetenekleri ile geliştirilmiştir:

* **Networking:** `java.net.Socket` ve `HttpURLConnection` kullanılarak, harici binary (Termux vb.) gerektirmeden ağ işlemleri yapılır.
* **Concurrency:** Ağ taramalarının hızlı olması için `ExecutorService` ile **Thread Pooling** (20-25 eşzamanlı işlem) mimarisi kullanılmıştır.
* **UI/UX:** Klavye açıldığında ekranı dinamik olarak yeniden boyutlandıran (`adjustResize`) ve terminal akışını bozmayan Responsive tasarım.

---

## ⚙️ Kurulum

1.  Bu depoyu klonlayın:
    ```bash
    git clone [https://github.com/KULLANICI_ADINIZ/Karage-Security-OS.git](https://github.com/KULLANICI_ADINIZ/Karage-Security-OS.git)
    ```
2.  Projeyi **Android Studio** ile açın.
3.  Cihazınızı bağlayın veya Emülatörü başlatın.
4.  **Run (▶)** tuşuna basın.

*Not: Uygulama internet izni gerektirir, `AndroidManifest.xml` dosyasında izinlerin tanımlı olduğundan emin olun.*

---

## ⚠️ Yasal Uyarı (Disclaimer)

Bu yazılım **sadece eğitim ve laboratuvar** amaçlı geliştirilmiştir. Geliştirici, bu aracın yasadışı kullanımından doğacak hiçbir sorumluluğu kabul etmez. **Sadece izniniz olan sistemlerde test yapınız.**

---

## 👨‍💻 Geliştirici

**Karage Yazılım** Mobil Uygulama Güvenliği & Android Geliştirici

[LinkedIn Profilim](LINKEDIN_ADRESIN) | [Website](WEBSITE_ADRESIN)

---
