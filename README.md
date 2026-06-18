# North Launcher

**North Launcher**, modern, hızlı ve kullanıcı dostu bir Minecraft launcher projesidir.
Amaç; Minecraft sürüm yönetimi, Microsoft hesabı ile giriş, offline profil modu, mod yönetimi, skin sistemi ve instance/profil yönetimini tek bir temiz arayüzde toplamaktır.

> North Launcher, resmi Minecraft deneyimini kolaylaştırmayı hedefleyen bağımsız bir launcher projesidir.

---

## 🚀 Özellikler

### 👤 Hesap Sistemi

* Microsoft hesabı ile resmi giriş desteği
* Güvenli OAuth / Device Code Flow mantığı
* Birden fazla hesap ekleme
* Hesaplar arasında geçiş yapma
* Offline Profil Modu
* Offline profiller için kullanıcı adı seçme
* Offline profil için local skin desteği

> Offline Profil Modu yalnızca yerel test, geliştirme, LAN ve offline sunucu kullanımı için tasarlanmıştır. Microsoft/Minecraft lisans doğrulamasını atlatmaya yönelik değildir.

---

### 🎮 Minecraft Başlatma Sistemi

* Minecraft sürüm seçme
* Vanilla sürüm desteği
* Forge desteği
* Fabric desteği
* Quilt desteği
* Instance/profil bazlı oyun klasörü
* RAM ayarı
* Java yolu algılama
* JVM argümanları
* Canlı log ekranı
* Crash/hata raporlama sistemi

---

### 🧩 Mod Yönetimi

* Local mod yükleme
* Mod silme
* Mod aktif/pasif yapma
* Mod klasörünü açma
* Mod sürüm uyumluluk kontrolü
* Forge/Fabric/Quilt uyumluluk kontrolü
* Eksik bağımlılık uyarısı
* Modrinth entegrasyonu planı
* CurseForge entegrasyonu planı
* Modpack import/export desteği planı

---

### 🧍 Skin Sistemi

* Local skin yükleme
* 3D skin önizleme
* Steve/Alex model seçimi
* Offline profil için skin seçme
* Skin dosyası doğrulama
* Basit skin editörü planı
* Hazır skin şablonları planı

---

### ⚙️ Launcher Ayarları

* Tema seçimi
* Dil seçimi
* RAM ayarları
* Java yolu ayarı
* Minecraft ana klasörü seçimi
* İndirme ayarları
* Log seviyesi
* Otomatik güncelleme ayarları

---

## 🖼️ Arayüz

North Launcher modern, sade ve koyu tema odaklı bir arayüze sahiptir.

Planlanan ana ekranlar:

* Ana Sayfa
* Hesaplar
* Instance Yönetimi
* Sürüm Seçimi
* Modlar
* Skinler
* Ayarlar
* İndirme Yöneticisi
* Log Ekranı
* Hata / Crash Ekranı

---

## 🛠️ Kullanılan Teknolojiler

Planlanan teknoloji yapısı:

* **Electron**
* **TypeScript**
* **React**
* **Vite**
* **TailwindCSS**
* **pnpm**
* **Vitest**
* **Playwright**
* **@xmcl/core**
* **@xmcl/installer**
* **@xmcl/user**
* **@xmcl/mod-parser**
* **@xmcl/model**
* **@xmcl/modrinth**
* **@xmcl/curseforge**

---

## 📁 Proje Yapısı

```txt
north-launcher/
├── apps/
│   └── desktop/
│       ├── src/
│       │   ├── main/
│       │   ├── preload/
│       │   └── renderer/
│       └── package.json
│
├── packages/
│   ├── launcher-core/
│   │   ├── src/
│   │   │   ├── accounts/
│   │   │   ├── downloads/
│   │   │   ├── instances/
│   │   │   ├── java/
│   │   │   ├── launch/
│   │   │   ├── logs/
│   │   │   ├── mods/
│   │   │   ├── skins/
│   │   │   └── versions/
│   │   └── tests/
│   │
│   ├── shared/
│   │   └── src/
│   │
│   └── ui/
│       └── src/
│
├── tests/
│   ├── unit/
│   ├── integration/
│   └── e2e/
│
├── docs/
├── package.json
├── pnpm-workspace.yaml
├── tsconfig.json
└── README.md
```

---

## 📦 Kurulum

Önce bilgisayarında şu araçların kurulu olması gerekir:

* Git
* Node.js LTS
* pnpm

Projeyi klonla:

```bash
git clone https://github.com/kullanici-adin/north-launcher.git
cd north-launcher
```

Bağımlılıkları yükle:

```bash
pnpm install
```

Geliştirme modunda çalıştır:

```bash
pnpm dev
```

---

## 🧪 Testler

Kod kalitesini kontrol etmek için:

```bash
pnpm lint
```

TypeScript kontrolü:

```bash
pnpm check
```

Unit testleri çalıştırmak için:

```bash
pnpm test
```

Build almak için:

```bash
pnpm build
```

E2E testler için:

```bash
pnpm test:e2e
```

---

## ✅ Test Hedefleri

North Launcher geliştirilirken şu testlerin başarılı olması hedeflenir:

* Instance oluşturma testi
* Offline profil oluşturma testi
* RAM ayarı doğrulama testi
* Java yolu doğrulama testi
* Mod ekleme/silme testi
* Mod aktif/pasif yapma testi
* Skin dosyası doğrulama testi
* Ayarları kaydetme/yükleme testi
* İndirme kuyruğu testi
* Hash doğrulama testi
* Uygulama açılış E2E testi
* Ana sayfa görüntüleme testi
* Ayarlar sayfası testi
* Modlar sayfası testi
* Skin sayfası testi

---

## 🔐 Güvenlik

North Launcher güvenli bir launcher mimarisi hedefler.

* Microsoft şifresi launcher içinde alınmaz.
* Resmi Microsoft OAuth sistemi kullanılır.
* Tokenlar düz metin olarak saklanmaz.
* Electron tarafında `contextIsolation` açık tutulur.
* `nodeIntegration` kapalı tutulur.
* Renderer doğrudan Node.js API kullanmaz.
* IPC kanalları tip güvenli tasarlanır.
* Harici dosya indirmelerinde hash/checksum doğrulaması yapılır.
* Kullanıcıdan habersiz dosya çalıştırılmaz.
* Şüpheli dosya uzantılarında kullanıcı uyarılır.

---

## 🗺️ Yol Haritası

### MVP

* [ ] Electron uygulama iskeleti
* [ ] Ana sayfa
* [ ] Offline profil oluşturma
* [ ] Instance oluşturma
* [ ] Minecraft sürüm seçme
* [ ] Java algılama
* [ ] RAM ayarı
* [ ] Local mod yönetimi
* [ ] Local skin yükleme
* [ ] Log ekranı
* [ ] Ayarları kaydetme
* [ ] Unit testler
* [ ] Build sistemi

### Gelişmiş Özellikler

* [ ] Microsoft hesabı ile resmi giriş
* [ ] Forge kurulumu
* [ ] Fabric kurulumu
* [ ] Quilt kurulumu
* [ ] Modrinth entegrasyonu
* [ ] CurseForge entegrasyonu
* [ ] Modpack import/export
* [ ] 3D skin editörü
* [ ] Launcher otomatik güncelleme
* [ ] Windows installer
* [ ] Portable sürüm
* [ ] Çoklu dil desteği
* [ ] Discord RPC

---

## 🧊 North Launcher Marka Kimliği

North Launcher; kuzey pusulası, buz mavisi renkler ve voxel/blok temalı detaylardan ilham alır.

Önerilen renk paleti:

```txt
Ana arka plan: #050A14
İkincil arka plan: #0B1220
Ana vurgu: #00C8FF
İkincil vurgu: #007BFF
Yazı rengi: #EAF6FF
Hata rengi: #FF4D4D
Başarı rengi: #35D07F
```

---

## ⚠️ Yasal Uyarı

North Launcher bağımsız bir projedir.

Bu proje Microsoft, Mojang veya Minecraft ile resmi olarak bağlantılı değildir.
Minecraft, Mojang Studios ve Microsoft ilgili sahiplerinin ticari markalarıdır.

North Launcher, resmi Minecraft hesabı ile giriş sistemini desteklemeyi hedefler.
Offline Profil Modu yalnızca yerel test, geliştirme, LAN veya offline kullanım senaryoları için düşünülmüştür.

Bu proje korsan kullanımı, lisans doğrulamasını atlatmayı veya yetkisiz erişimi teşvik etmez.

---

## 🤝 Katkıda Bulunma

Katkıda bulunmak için:

1. Bu repoyu forkla
2. Yeni branch oluştur

```bash
git checkout -b feature/yeni-ozellik
```

3. Değişikliklerini yap
4. Testleri çalıştır

```bash
pnpm lint
pnpm check
pnpm test
pnpm build
```

5. Pull request gönder

---

## 📜 Lisans

Bu proje için lisans henüz belirlenmemiştir.

Önerilen lisans:

```txt
MIT License
```

Eğer başka açık kaynak projelerden kod veya paket kullanılırsa, ilgili projelerin lisans şartlarına uyulmalıdır.

---

## ⭐ Destek

Projeyi beğendiysen GitHub üzerinden yıldız verebilirsin.

**North Launcher — Modern Minecraft Launcher Experience**

