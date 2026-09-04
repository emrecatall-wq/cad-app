# Çizgi CAD — GitHub'a doğru yükleme (klasörsüz, düz yapı)

Bu klasördeki dosyaların **hepsi aynı seviyede** — hiçbir alt klasör yok.
Bunun sebebi: GitHub'ın web "Upload files" ekranında dosya seçiciyle (tıklayarak)
klasör yüklenemiyor, sadece sürükle-bırakla yükleniyor. Alt klasör olmayınca
bu hata payı tamamen ortadan kalkıyor.

## Yükleme adımları
1. GitHub'da repona git (örn. `cizimmm`).
2. Önceki denemede yüklediğin TÜM dosyaları/klasörleri sil (özellikle varsa
   eski `icons/` klasörünü) — karışıklık olmasın.
3. "Add file" → "Upload files" → bu klasördeki TÜM dosyaları (index.html,
   manifest.json, sw.js, icon-72.png, icon-96.png, icon-128.png, icon-144.png,
   icon-152.png, icon-192.png, icon-384.png, icon-512.png,
   icon-512-maskable.png) tek seferde seç ve yükle. Repo kökünde dursunlar,
   klasöre koyma.
4. Commit et.
5. Settings → Pages'ten yayının güncellendiğini bekle (birkaç dakika).
6. Kontrol için tarayıcıdan şu adresi aç, resmin gerçekten açıldığını gör:
   `https://emrecatall-wq.github.io/cizimmm/icon-512.png`
   Açılmıyorsa (404 veriyorsa) dosya yüklenmemiş demektir, tekrar yükle.
7. PWA Builder'da tekrar "Start over" / adresi yeniden tara — icon hataları
   gitmiş olmalı.

## Bu sürümde ayrıca düzeltilenler
- `manifest.json`'a `id` alanı eklendi (PWA Builder'ın "add an id" uyarısını giderir).
- 72–512 px arası 8 farklı ikon boyutu eklendi (PWA Builder'ın "icon sizes" uyarısını giderir).
- "Add screenshots" uyarısı isteğe bağlıdır, APK üretimini engellemez — istersen
  uygulamanın birkaç ekran görüntüsünü PWA Builder'ın kendi arayüzünden manifest'e ekleyebilirsin.
