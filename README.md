# Nöbetçi Eczane API Dökümantasyonu

Bu API, Türkiye'deki nöbetçi eczanelerin bilgilerine erişim sağlar. Geliştiricilerin uygulamalarında kullanabileceği basit ve etkili bir arayüz sunar.

> 📢 **Resmi Dökümantasyon**: Daha detaylı bilgi ve canlı örnekler için [Eczaneler.org Nöbetçi Eczane API Dökümantasyonu](https://eczaneler.org/nobetci-eczane-api-docs) sayfasını ziyaret edebilirsiniz.

## 📌 Özellikler

- Şehir ve ilçe bazında nöbetçi eczane sorgulama
- Güncel eczane bilgileri (isim, adres, telefon, konum)
- Kolay entegrasyon için RESTful API
- JSON formatında yanıt

## 🔧 Kullanım

### Temel Uç Nokta

```
GET /api/nobetci-eczaneler
```

### Parametreler

| Parametre | Tip     | Zorunlu | Açıklama                          |
|-----------|---------|---------|----------------------------------|
| sehir     | string  | Evet    | Şehir adı (örn: 'istanbul')      |
| ilce      | string  | Hayır   | İlçe adı (örn: 'kadikoy')        |

### Örnek İstek

```bash
curl -X GET "https://api.ornek.com/api/nobetci-eczaneler?sehir=istanbul&ilce=kadikoy"
```

### Örnek Yanıt

```json
{
  "success": true,
  "data": [
    {
  "data": [
    {
      "slug": "adana-cukurova-aygul-eczanesi",
      "title": "Adana Çukurova Aygül Eczanesi",
      "name": "Aygül Eczanesi",
      "phone": "+905070251485",
      "phone_formatted": "+90 507 025 14 85",
      "city": "Adana",
      "district": "Çukurova",
      "address": "MAHFESIĞMAZ MAH.ŞEHİTLER BULV. KAROL SİTESİ NO:14/L",
      "sentry_date": "2025-06-22",
      "is_sentry": true,
      "is_open": true,
      "workingHours": "08:00 - 23:59",
      "updated_at": "2025-06-22 00:03:37",
      "note": "",
      "coordinates": {
        "lat": "37.03424072",
        "lon": "35.30810547"
      }
    }
  ],
  "pagination": {
    "total": 13,
    "per_page": "12",
    "current_page": "1",
    "total_pages": 2,
    "has_more": true,
    "prev_page": null,
    "next_page": 2
  }
}
  ]
}
```

## 🔐 Güvenlik

- Tüm istekler HTTPS üzerinden yapılmalıdır
- API anahtarı gerektirebilir (isteğe bağlı)

## 🌐 Diğer Kaynaklar

- [Eczaneler.org Ana Sayfa](https://eczaneler.org)
- [Nöbetçi Eczane Sorgulama](https://eczaneler.org/nobetci-eczaneler)

## 📄 Lisans

Bu proje MIT lisansı altında lisanslanmıştır. Daha fazla bilgi için `LICENSE` dosyasına bakınız.

## 🔗 Faydalı Bağlantılar

- [Nöbetçi Noter API'si ](https://eczaneler.org/nobetci-noter-api-docs)

## 📞 İletişim

Sorularınız veya geri bildirimleriniz için:
- İletişim: https://eczaneler.org/iletisim
