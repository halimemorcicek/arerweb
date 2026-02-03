# ARER Web Sitesi - Logo Entegrasyonu

## 📦 Paket İçeriği

Bu pakette ARER logosunun tüm sayfalara entegre edilmiş versiyonları bulunmaktadır:

- index.html (Ana Sayfa)
- haberler.html (Haberler)
- robot-kol.html (Robot Kol Uygulamaları)
- makine-imalati.html (Makine İmalatı)
- dijital-fabrikalar.html (Dijital Fabrikalar)
- kontrol-scada.html (Kontrol & SCADA)
- endustriyel-egitim.html (Endüstriyel Eğitim)
- iletisim.html (İletişim)

## 🖼️ Logo Dosyası Kurulumu

### Adım 1: Logo Dosyasını Hazırlayın

1. Yüklediğiniz `logoheader.jpg` dosyasını alın
2. Dosyayı `logo.jpg` olarak yeniden adlandırın

### Adım 2: Images Klasörü Oluşturun

Web sitenizin ana dizininde bir `images` klasörü oluşturun:

```
web-siteniz/
├── images/
│   └── logo.jpg          ← Logo dosyanızı buraya koyun
├── index.html
├── haberler.html
├── robot-kol.html
├── makine-imalati.html
├── dijital-fabrikalar.html
├── kontrol-scada.html
├── endustriyel-egitim.html
├── iletisim.html
└── styles.css (ve diğer CSS dosyaları)
```

### Adım 3: CSS Ekleyin (Eğer Yoksa)

Ana CSS dosyanıza (örn. `styles.css`) aşağıdaki kodu ekleyin:

```css
/* Logo Stilleri */
.brand-logo {
    height: 60px;
    width: auto;
    display: block;
}

/* Responsive Logo */
@media (max-width: 768px) {
    .brand-logo {
        height: 45px;
    }
}
```

## ✅ Logo Değişiklikleri

Tüm sayfalarda aşağıdaki değişiklik yapılmıştır:

**ÖNCE:**
```html
<div class="brand">
    <span class="brand-text">ARER</span>
</div>
```

**SONRA:**
```html
<div class="brand">
    <a href="index.html">
        <img src="images/logo.jpg" alt="ARER Logo" class="brand-logo" />
    </a>
</div>
```

## 🎨 Logo Özelleştirme

Logo boyutunu değiştirmek isterseniz CSS'te `height` değerini ayarlayabilirsiniz:

```css
.brand-logo {
    height: 70px;  /* İstediğiniz yüksekliği girin */
    width: auto;
}
```

## 📱 Responsive Tasarım

Logo, mobil cihazlarda otomatik olarak küçülecek şekilde ayarlanmıştır. Mobil boyutu özelleştirmek için:

```css
@media (max-width: 768px) {
    .brand-logo {
        height: 40px;  /* Mobil için logo yüksekliği */
    }
}
```

## 🔗 Sayfa Linkleri

Tüm sayfalarda logo ana sayfaya (index.html) link verir. Bu, logoya tıklandığında kullanıcıları ana sayfaya yönlendirir.

## ⚠️ Önemli Notlar

1. Logo dosyasının (`logo.jpg`) mutlaka `images/` klasöründe olması gerekir
2. Logo dosyası isminin tam olarak `logo.jpg` olduğundan emin olun
3. Tüm HTML dosyalarının aynı seviyede (aynı klasörde) olması gerekir
4. CSS dosyalarınızın doğru yolları gösterdiğinden emin olun

## 🛠️ Sorun Giderme

**Logo görünmüyorsa:**
1. `images/logo.jpg` dosyasının doğru konumda olduğunu kontrol edin
2. Dosya isminin tam olarak `logo.jpg` olduğunu doğrulayın (büyük-küçük harf duyarlı)
3. Tarayıcınızı yenileyin (Ctrl + F5)
4. Tarayıcı konsolunda hata olup olmadığını kontrol edin (F12)

**Logo çok büyük/küçük görünüyorsa:**
- CSS'teki `.brand-logo` sınıfının `height` değerini ayarlayın

## 📞 Destek

Herhangi bir sorun yaşarsanız, lütfen iletişime geçin.

---
© 2026 ARER Otomasyon - Tüm hakları saklıdır
