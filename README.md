# Film ve Müşteri Verileri İçin SQL Sorguları

Bu dosya, `film` ve `customer` tablolarından veri çekmek için kullanılan SQL sorgularını ve her bir sorgunun işlevini açıklamaktadır.

---

### Sorgu 1: Tüm Filmleri Seç
```sql
SELECT title, description
FROM film;
Bu sorgu, film tablosundaki tüm filmlerin title (başlık) ve description (açıklama) sütunlarını getirir.
```

### Sorgu 2: Belirli Süre Aralığındaki Filmleri Seç
```sql
SELECT *
FROM film
WHERE length > 60 AND length < 75;
Bu sorgu, süresi 60 dakikadan fazla ve 75 dakikadan az olan filmleri seçer. Tüm film bilgilerini içeren satırlar döner.
```

### Sorgu 3: Kiralama Ücreti ve Yenileme Maliyetine Göre Filmleri Seç
```sql
SELECT *
FROM film
WHERE rental_rate = 0.99 AND (replacement_cost = 12.99 OR replacement_cost = 28.99);
Bu sorgu, rental_rate değeri 0.99 olan ve replacement_cost değeri 12.99 veya 28.99 olan filmleri getirir.
```

### Sorgu 4: Adı Mary Olan Müşterileri Seç
```sql
SELECT first_name, last_name
FROM customer
WHERE first_name = 'Mary';
Bu sorgu, first_name değeri 'Mary' olan müşterilerin first_name ve last_name sütunlarını seçer.
```

### Sorgu 5: Süresi Belirli Aralıkta Olan ve Belirli Kiralama Ücretlerini Hariç Tutan Filmleri Seç
```sql
SELECT length, rental_rate
FROM film
WHERE length <= 50 AND rental_rate NOT IN (2.99, 4.99);
Bu sorgu, süresi 50 dakikadan kısa veya eşit olan ve kiralama ücreti 2.99 veya 4.99 olmayan filmlerin length ve rental_rate sütunlarını getirir.
```

