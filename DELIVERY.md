
# OpenAPI Tasarımı Ödevi Teslim Raporu

## 👤 Öğrenci Bilgileri
- **Ad Soyad**: [Erdem Yorulmaz]
- **Öğrenci Numarası**: [170422042]

---

## 📂 OpenAPI YAML Dosyası

- **openapi.yaml** dosyası proje kök dizininde yer almaktadır.
- Swagger Editor (https://editor.swagger.io) kullanılarak tüm endpoint’ler test edilmiştir ve `No errors` sonucu alınmıştır.

### 🔗 GitHub Repo Linki
https://github.com/erdemyz/A-k-Kaynak-OpenAPI/upload/main

---

## 📝 API Açıklaması

Bu proje, üniversitenin çevrim içi kütüphane sistemi için tasarlanan bir REST API’dir.  
OpenAPI 3.0 standardı kullanılarak hazırlanmıştır.

### 📌 Varlıklar (Entities)
- **books**: Kitap bilgilerini içerir (`id`, `title`, `author`, `isbn`, `publisher`, `pageCount`, `stock`).
- **students**: Öğrenci bilgilerini içerir (`id`, `name`, `studentNumber`, `email`, `isActive`).
- **loans**: Ödünç alma işlemlerini içerir (`id`, `studentId`, `bookId`, `loanDate`, `returnDate`, `status`).

### 🔗 CRUD İşlemleri ve Endpoint’ler
- `GET /books`, `GET /books/{id}`, `POST /books`, `PUT /books/{id}`, `DELETE /books/{id}`
- `GET /students`, `GET /students/{id}`, `POST /students`, `PUT /students/{id}`, `DELETE /students/{id}`
- `GET /loans`, `GET /loans/{id}`, `POST /loans`, `PATCH /loans/{id}/return`

### ⚙️ Kullanılan OpenAPI Bölümleri
- **components/schemas**: Her varlık için veri modelleri tanımlandı.
- **parameters**: Sayfalama (`page`, `size`) ve path parametreleri (`id` gibi) eklendi.
- **requestBody**: `POST` ve `PUT` endpoint’lerinde `required: true` ile kullanıldı.
- **responses**: Başarı ve hata durumları için `200`, `201`, `400`, `404`, `500` kodları tanımlandı.
- **example**: Örnek veri `POST /books` endpoint’inde sağlandı.
- **tags**: Her varlık için açıklayıcı `tags` kullanıldı.
- **securitySchemes**: Bearer Token (`JWT`) örneği eklendi.

### 📄 Sayfalama ve Hata Yönetimi
- `GET /books` için `page` ve `size` parametreleri ile sayfalama sağlandı.
- Tüm endpoint’lerde hata durumları için `400`, `404`, `500` kodları ve açıklamalar tanımlandı.

---

## 🧪 Test Notları

- `GET /books`: Tüm kitapların JSON dizisi döner.
- `POST /students`: Örnek `requestBody` ile öğrenci eklenir.
- `PATCH /loans/{id}/return`: Kitabın iade edildiği yanıt döner.
- Hatalı `POST /books` isteğinde `400` kodlu yanıt döner.

---

## 📌 Ek Açıklamalar

- Tüm yapı Swagger Editor’de test edildi.
- API tanımı `openapi.yaml` dosyasında eksiksiz yer almaktadır.
- Kod yazılmamıştır; yalnızca OpenAPI YAML tanımı hazırlanmıştır.

