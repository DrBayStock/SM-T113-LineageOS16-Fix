# SM-T113 LineageOS 16 Fix

Samsung Galaxy Tab 3 Lite / Tab E 7.0 — **SM-T113 (goyavewifi)**

**[🇹🇷 Türkçe](#türkçe)** | **[🇬🇧 English](#english)**

**İndir / Download:** [Releases](https://github.com/DrBayStock/SM-T113-LineageOS16-Fix/releases)

---

## Türkçe

Bu depo, `lineage-16.0-20260901-UNOFFICIAL-goyavewifi` ROM'u (geliştirici: **vigus**) için düzeltmeler içerir. Orijinal ROM bu tablette kendi başına sorunlu çalışır; buradaki dosyalar o sorunları giderir.

### Dosyalar (Releases bölümünde)

| Dosya | Açıklama |
|---|---|
| `A-TEMIZ(CLEAN)-...-T113FIX-20261117.zip` | **Temiz:** bütün düzeltmeleri hazır eklenmiş tam ROM. Tek başına kurulur. |
| `B1-ORIJINAL-BOZUK(ORIGINAL-BROKEN)-...zip` | **Bozuk:** orijinal, değiştirilmemiş ROM. |
| `B2-DUZELTME(FIX)-T113-LOS16-FixPack-20261117.zip` | **Düzeltme:** B1'in üzerine kurulan yama (10 MB). |

A ile "B1 + B2" aynı sonucu verir.

### Kurulum (TWRP)

Önce: **Wipe > Advanced Wipe** → System, Data, Cache, Dalvik

- **Seçenek A:** `A-TEMIZ` → (isteğe bağlı GApps) → Reboot
- **Seçenek B:** `B1-ORIJINAL-BOZUK` → `B2-DUZELTME` → (isteğe bağlı GApps) → Reboot

GApps: ARM, Android 9.0, pico/nano önerilir. TWRP'de "Zip signature verification" kapalı olmalı. İlk açılış ~25 sn uzun sürer.

### Düzeltilenler

- **Kamera:** arka kamera çalışır, doğru yönde, video kaydı çalışır. *Kamera uygulaması devre dışı/görünmüyorsa: Ayarlar > Uygulamalar > Kamera > Etkinleştir, ya da Snap / Open Camera kurun.*
- **Wi-Fi:** temiz kurulumda açılmama sorunu giderildi; TV'ye ekran yansıtma (Miracast) etkin.
- **Dokunmatik:** doğru yere basar; ekran kapanıp açılınca kilit ekranında donması giderildi.
- **Ekran:** donma ve grafik çökmesi giderildi; kilit ekranı da döner; ortam ekranı (pil harcıyordu) kapatıldı.
- **Diğer:** otomatik döndürme, Bluetooth, adb/USB, derin uyku/pil, 384 MB takas, ortak depolamaya yazma, kapalı şarj ekranı.

Ayrıntılar: [BENIOKU.txt](BENIOKU.txt)

> Not: Kamera için boot bölümüne aynı geliştiricinin LineageOS 15.1 kerneli yazılır. TV yansıtmada ses aktarımı test edilmedi. Kullanım riski size aittir.

---

## English

This repository contains fixes for the `lineage-16.0-20260901-UNOFFICIAL-goyavewifi` ROM (developer: **vigus**). The original ROM has problems on this tablet on its own; the files here fix them.

### Files (in Releases)

| File | Description |
|---|---|
| `A-TEMIZ(CLEAN)-...-T113FIX-20261117.zip` | **Clean:** full ROM with all fixes built in. Install it on its own. |
| `B1-ORIJINAL-BOZUK(ORIGINAL-BROKEN)-...zip` | **Broken:** the original, unmodified ROM. |
| `B2-DUZELTME(FIX)-T113-LOS16-FixPack-20261117.zip` | **Fix:** patch flashed on top of B1 (10 MB). |

A and "B1 + B2" give the same result.

### Installation (TWRP)

First: **Wipe > Advanced Wipe** → System, Data, Cache, Dalvik

- **Option A:** `A-TEMIZ` → (optional GApps) → Reboot
- **Option B:** `B1-ORIJINAL-BOZUK` → `B2-DUZELTME` → (optional GApps) → Reboot

GApps: ARM, Android 9.0, pico/nano recommended. "Zip signature verification" must be off in TWRP. First boot takes ~25 s longer.

### Fixed

- **Camera:** rear camera works, correct orientation, video recording works. *If the Camera app is disabled/hidden: Settings > Apps > Camera > Enable, or install Snap / Open Camera.*
- **Wi-Fi:** fixed Wi-Fi not turning on after a clean install; screen casting to a TV (Miracast) enabled.
- **Touchscreen:** touches land in the right place; fixed freezing on the lock screen after screen off/on.
- **Display:** fixed freezes and graphics crash; lock screen rotates; ambient display (was draining battery) turned off.
- **Other:** auto-rotate, Bluetooth, adb/USB, deep sleep/battery, 384 MB swap, shared storage write access, off-mode charging screen.

Details: [README.txt](README.txt)

> Note: For the camera, the same developer's LineageOS 15.1 kernel is written to the boot partition. Audio while casting to a TV has not been tested. Use at your own risk.
