# SQL_Assignment_1

## Sorgu Senaryoları

* film tablosunda bulunan title ve description sütunlarındaki verileri sıralayınız.

```bash
SELECT title, description
FROM film
ORDER BY title, description;
```

* film tablosunda bulunan tüm sütunlardaki verileri film uzunluğu (length) 60 dan büyük VE 75 ten küçük olma koşullarıyla sıralayınız.

```bash
SELECT *
FROM film
WHERE length > 60 AND length < 75
ORDER BY length;
```

* film tablosunda bulunan tüm sütunlardaki verileri rental_rate 0.99 VE replacement_cost 12.99 VEYA 28.99 olma koşullarıyla sıralayınız.

```bash
SELECT *
FROM film
WHERE rental_rate = 0.99 AND (replacement_cost = 12.99 OR replacement_cost = 28.99)
ORDER BY rental_rate, replacement_cost;
```

* customer tablosunda bulunan first_name sütunundaki değeri 'Mary' olan müşterinin last_name sütunundaki değeri nedir?

```bash
SELECT last_name
FROM customer
WHERE first_name = 'Mary';
```

* film tablosundaki uzunluğu(length) 50 ten büyük OLMAYIP aynı zamanda rental_rate değeri 2.99 veya 4.99 OLMAYAN verileri sıralayınız.

```bash
SELECT *
FROM film
WHERE length <= 50 AND (rental_rate != 2.99 AND rental_rate != 4.99)
ORDER BY length, rental_rate;
```

## Notlar:

* Bu sorgular, dvdrental örnek veritabanı üzerinde çalıştırılmalıdır.
* Sorgular, MySQL, PostgreSQL veya SQL Server gibi herhangi bir SQL veritabanı yönetim sisteminde kullanılabilir.
* Sorgu sonuçları, veritabanınızdaki verilerin içeriğine bağlı olarak değişiklik gösterebilir.