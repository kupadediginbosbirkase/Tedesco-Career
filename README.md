# Domenico Tedesco Career Scraper
Domenico Tedesco'nun kariyer bilgilerini çeken bir python scripti, tedesco fanıysanız bu ilginizi çekebilir.

Bu proje, futbol teknik direktörü Domenico Tedesco'nun kariyer bilgilerini otomatik olarak çekmek için geliştirilmiş bir Python tabanlı web scraping uygulamasıdır.

Proje, veri kaynağı olarak Transfermarkt sitesini kullanır ve Scrapy framework'ü ile geliştirilmiştir.

---

# Proje Amacı

Bu projenin amacı:

- Web scraping mantığını öğrenmek
- Gerçek bir web sitesinden veri çekmek
- Python ve Scrapy kullanımı pratiği yapmak
- Yapısal veri işleme süreçlerini anlamaktır

---

# Kullanılan Teknolojiler

- Python 3
- Scrapy
- JSON

---

# Çekilen Veriler

Scraper aşağıdaki bilgileri çekmektedir:

- Teknik direktör adı
- Doğum tarihi
- Uyruk
- Lisans bilgisi
- Kariyer geçmişi
- Çalıştırdığı takımlar
- Maç istatistikleri
- Puan ortalaması
- Görev süreleri

---

# Kurulum

## 1. Repository'i klonla

```bash
git clone https://github.com/kupadediginbosbirkase/domenico-tedesco-scraper.git
```

## 2. Proje klasörüne gir

```bash
cd domenico-tedesco-scraper
```

## 3. Gerekli paketleri kur

```bash
pip install scrapy
```

---

# Scrapy Projesi Oluşturma

Eğer projeyi sıfırdan oluşturmak istersen:

```bash
scrapy startproject tedesco_scraper
```

Spider oluştur:

```bash
scrapy genspider tedesco transfermarkt.com
```

---

# Çalıştırma

Spider'ı çalıştırmak için:

```bash
scrapy crawl tedesco
```

Komut çalıştıktan sonra:

```bash
tedesco.json
```

dosyası oluşacaktır.

---

# Örnek JSON Çıktısı

```json
{
    "name": "Domenico Tedesco",
    "nationality": "Italy",
    "career_history": [
        {
            "team": "Fenerbahce"
        },
        {
            "team": "Turkey"
        }
    ]
}
```

---

# Proje Yapısı

```bash
tedesco_scraper/
│
├── scrapy.cfg
│
└── tedesco_scraper/
    │
    ├── spiders/
    │   └── tedesco.py
    │
    ├── items.py
    ├── pipelines.py
    ├── settings.py
    └── middlewares.py
```

---

# Geliştirme Fikirleri

Projeye ileride şu özellikler eklenebilir:

- CSV çıktısı
- SQLite / PostgreSQL desteği
- Proxy rotasyonu
- Anti-bot bypass
- Async scraping
- Takım detay sayfaları
- Veri görselleştirme
- API desteği

---

# Uyarı

Bu proje yalnızca eğitim amaçlı geliştirilmiştir.

Transfermarkt sitesinin kullanım şartlarına dikkat edilmelidir.

Yoğun istek gönderimi yapılmamalıdır.

---

# Lisans

MIT License
