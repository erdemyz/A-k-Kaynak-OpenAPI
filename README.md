
# Library API - OpenAPI Tanımı

Bu proje, bir üniversitenin çevrim içi kütüphane sistemi için OpenAPI 3.0 spesifikasyonuna uygun olarak hazırlanmıştır. API, `books`, `students` ve `loans` gibi temel varlıkları yönetmek için gerekli CRUD endpoint’lerini içermektedir.

## 📚 Özellikler
- **Kitaplar**: Kitap ekleme, güncelleme, silme ve listeleme
- **Öğrenciler**: Öğrenci ekleme, güncelleme, silme ve listeleme
- **Ödünç Alma**: Kitap ödünç alma, iade etme ve tüm ödünç işlemlerini listeleme
- **Sayfalama**: `GET /books` endpoint’inde `page` ve `size` parametreleri ile
- **Güvenlik**: Bearer Token desteği (`JWT`)

## 🛠️ Yapı
```
/
├── openapi.yaml        # OpenAPI 3.0 tanımı
├── DELIVERY.md         # Teslimat açıklamaları
└── README.md           # Bu dosya, proje özeti
```

## ⚙️ Kullanılan Araçlar
- [Swagger Editor](https://editor.swagger.io) – Test ve validasyon
- Visual Studio Code – YAML düzenleme

## 🚀 Kullanım
1. `openapi.yaml` dosyasını Swagger Editor’e yükleyerek tüm endpoint’leri inceleyebilirsin.

## 📦 Test
Swagger Editor’de test edilmiştir – **No errors** sonucu alınmıştır.

---

### ✨ İletişim
Herhangi bir sorunuz olursa bana ulaşabilirsiniz.
