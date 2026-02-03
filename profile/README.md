```
  _____                      _____  _____   _    _  _____
 |  ___|                    /  __ \|  _  \ | |  | ||  _  |
 | |_  ___  _ __  __ _  ___ | /  \/| |_| | | |  | || | | |
 |  _|/ _ \| '__|/ _` |/ _ \| |    |    /  | |  | || | | |
 | | | (_) | |  | (_| |  __/| \__/\| |\ \  | |__| || |/ /
 \_|  \___/|_|   \__, |\___|  \____/\_| \_|  \____/ |___/
                  __/ |
                 |___/
```

### NO-Code Operasyon Platformu

[![Website](https://img.shields.io/badge/Website-forgecrud.io-2a85ff?style=for-the-badge&logo=google-chrome&logoColor=white)](https://forgecrud.io)
[![Demo](https://img.shields.io/badge/Canl%C4%B1-Demo-10b981?style=for-the-badge&logo=rocket&logoColor=white)](https://demo.v2.forgecrud.io)
[![Docs](https://img.shields.io/badge/Dok%C3%BCmantasyon-Rehber-6366f1?style=for-the-badge&logo=gitbook&logoColor=white)](https://forgecrud.io/docs)

---

**ForgeCRUD** operasyonel iş akışlarınızı güçlü dijital uygulamalara dönüştürür - tek satır kod yazmadan.

Dinamik formlar oluşturun, otomatik iş akışları tasarlayın ve dakikalar içinde özel API'lar oluşturun. Satın alma talepleri, izin yönetimi, fatura onayları ve hayal edebileceğiniz her türlü iş süreci için idealdir.

---

## Özellikler

<table>
<tr>
<td width="50%">

### Görsel Form Oluşturucu
Sürükle-bırak ile her türlü formu oluşturun
- 15+ alan tipi (metin, seçim, tarih, dosya yükleme...)
- Otomatik veritabanı tablo oluşturma
- Akıllı doğrulama kuralları
- İlişkisel alan desteği
- Otomatik kod üretimi (PO-000001)

</td>
<td width="50%">

### İş Akışı Motoru
ReactFlow ile görsel onay akışları tasarlayın
- Çok seviyeli onaylar (Yönetici > Direktör > CEO)
- Koşullu dallanma
- Zamanlanmış tetikleyiciler (cron tabanlı)
- E-posta ve anlık bildirimler
- Webhook entegrasyonları

</td>
</tr>
<tr>
<td width="50%">

### Özel API Oluşturucu
SQL yazmadan REST API oluşturun
- Çoklu tablo JOIN desteği
- Aggregation fonksiyonları (SUM, COUNT, AVG)
- Window fonksiyonları (ROW_NUMBER, RANK)
- Dinamik filtreleme ve sıralama

</td>
<td width="50%">

### Döküman Yönetimi
MinIO ile S3-uyumlu dosya depolama
- Versiyon kontrolü
- Klasör organizasyonu
- Erişim kontrolü
- Dosya önizleme

</td>
</tr>
<tr>
<td width="50%">

### Anlık Bildirimler
Herkesi anında bilgilendirin
- WebSocket tabanlı uyarılar
- E-posta entegrasyonu
- Özelleştirilebilir şablonlar
- Uygulama içi bildirim merkezi

</td>
<td width="50%">

### Kurumsal Güvenlik
Verileriniz için banka düzeyinde güvenlik
- 3 Seviyeli RBAC (Kullanıcı > Rol > Organizasyon)
- JWT kimlik doğrulama
- SQL Injection ve XSS koruması
- Rate limiting (100 istek/dk)
- Çoklu kiracı veri izolasyonu

</td>
</tr>
</table>

---

## Nasıl Çalışır

```
┌─────────────────┐     ┌─────────────────┐     ┌─────────────────┐     ┌─────────────────┐
│  1. TASARLA     │     │  2. OTOMATİK    │     │  3. GÜVENLİ     │     │  4. YAYINLA     │
│  ───────────    │     │  ──────────     │     │  ─────────      │     │  ─────────      │
│                 │     │                 │     │                 │     │                 │
│  Formları       │────▶│  Tetikleyiciler │────▶│  Rolleri ve     │────▶│  Dakikalar      │
│  görsel         │     │  ve aksiyonlarla│     │  izinleri       │     │  içinde         │
│  oluştur        │     │  iş akışı kur   │     │  ayarla         │     │  canlıya al     │
└─────────────────┘     └─────────────────┘     └─────────────────┘     └─────────────────┘
```

---

## Kullanım Senaryoları

| Senaryo | Açıklama |
|---------|----------|
| **Satın Alma Talepleri** | Talep > Yönetici Onayı > Bütçe Kontrolü > Direktör Onayı > Satın Alma |
| **İzin Yönetimi** | Başvur > Yönetici İncelemesi > İK Onayı > Takvim Senkronizasyonu |
| **Fatura Onayı** | Yükle > Doğrulama > Çok Seviyeli Onay > Ödeme İşleme |
| **BT Destek** | Bilet Oluşturma > Atama > Çözüm > Geri Bildirim |
| **Masraf Raporları** | Gönder > Makbuz Yükle > Onay > Geri Ödeme |

---

## Teknoloji Stack

<table>
<tr>
<td align="center" width="20%">
<img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/go/go-original-wordmark.svg" width="48" height="48" alt="Go" />
<br><strong>Go</strong>
<br><sub>Backend Servisleri</sub>
</td>
<td align="center" width="20%">
<img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/react/react-original.svg" width="48" height="48" alt="React" />
<br><strong>React</strong>
<br><sub>Frontend</sub>
</td>
<td align="center" width="20%">
<img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/typescript/typescript-original.svg" width="48" height="48" alt="TypeScript" />
<br><strong>TypeScript</strong>
<br><sub>Tip Güvenliği</sub>
</td>
<td align="center" width="20%">
<img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/postgresql/postgresql-original.svg" width="48" height="48" alt="PostgreSQL" />
<br><strong>PostgreSQL</strong>
<br><sub>Veritabanı</sub>
</td>
<td align="center" width="20%">
<img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/redis/redis-original.svg" width="48" height="48" alt="Redis" />
<br><strong>Redis</strong>
<br><sub>Cache & Queue</sub>
</td>
</tr>
<tr>
<td align="center" width="20%">
<img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/docker/docker-original.svg" width="48" height="48" alt="Docker" />
<br><strong>Docker</strong>
<br><sub>Konteynerizasyon</sub>
</td>
<td align="center" width="20%">
<img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/kubernetes/kubernetes-original.svg" width="48" height="48" alt="Kubernetes" />
<br><strong>Kubernetes</strong>
<br><sub>Orkestrasyon</sub>
</td>
<td align="center" width="20%">
<img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/rabbitmq/rabbitmq-original.svg" width="48" height="48" alt="RabbitMQ" />
<br><strong>RabbitMQ</strong>
<br><sub>Mesaj Kuyruğu</sub>
</td>
<td align="center" width="20%">
<img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/nginx/nginx-original.svg" width="48" height="48" alt="Nginx" />
<br><strong>Nginx</strong>
<br><sub>API Gateway</sub>
</td>
<td align="center" width="20%">
<img src="https://min.io/resources/img/logo/MINIO_Bird.png" width="48" height="48" alt="MinIO" />
<br><strong>MinIO</strong>
<br><sub>Dosya Depolama</sub>
</td>
</tr>
</table>

---

## Performans

| Metrik | Değer |
|--------|-------|
| API Yanıt Süresi | < 100ms |
| Eşzamanlı Kullanıcı | 10,000+ |
| Uptime SLA | %99.9 |
| Microservice | 9 |
| Veritabanı | 3 |
| Konteynerize | %100 |

---

## Hızlı Linkler

| Kaynak | Link |
|--------|------|
| Website | [forgecrud.io](https://forgecrud.io) |
| Canlı Demo | [demo.v2.forgecrud.io](https://demo.v2.forgecrud.io) |
| Dokümantasyon | [forgecrud.io/docs](https://forgecrud.io/docs) |
| İletişim | [info@forgecrud.com](mailto:info@forgecrud.com) |

---

## Bizi Takip Edin

[![Twitter](https://img.shields.io/badge/Twitter-@forgecrud-1DA1F2?style=flat-square&logo=twitter&logoColor=white)](https://twitter.com/forgecrud)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-ForgeCRUD-0A66C2?style=flat-square&logo=linkedin&logoColor=white)](https://linkedin.com/company/forgecrud)
[![GitHub](https://img.shields.io/badge/GitHub-forgecrud-181717?style=flat-square&logo=github&logoColor=white)](https://github.com/forgecrud)

---

<p align="center">
  <strong>Operasyonlarınızı Dönüştürün. Kodsuz İnşa Edin.</strong>
  <br><br>
  <a href="https://forgecrud.io">
    <img src="https://img.shields.io/badge/Hemen_Ba%C5%9Fla-ForgeCRUD-2a85ff?style=for-the-badge" alt="Hemen Başla">
  </a>
</p>

---

<p align="center">
  <a href="https://github.com/Onurlulardan">Onur Altuntaş</a> tarafından geliştirildi
  <br>
  <sub>Copyright 2026 ForgeCRUD. Tüm hakları saklıdır.</sub>
</p>
