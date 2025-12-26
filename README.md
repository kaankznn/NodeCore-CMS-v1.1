# NodeCore-CMS v1.1

![Node.js](https://img.shields.io/badge/Node.js-Backend-success)
![MySQL](https://img.shields.io/badge/MySQL-Relational-blue)
![SQL](https://img.shields.io/badge/SQL-3NF%20Design-orange)

## CMS (NodeJS + MySQL)

Bu proje, NodeJS tabanlı bir CMS (Content Management System) uygulaması için
MySQL üzerinde tasarlanmış ilişkisel veritabanını ve örnek SQL scriptlerini içerir.

Projede aşağıdaki gereksinimler sağlanmıştır:
- En az 5 ana tablo + 1 log tablosu
- 3NF normalizasyon
- PRIMARY KEY, FOREIGN KEY, CHECK, UNIQUE gibi kısıtlamalar
- 3 adet VIEW
- 3 adet STORED PROCEDURE
- 3 adet TRANSACTION örneği
- 10 adet kompleks SQL sorgusu
- Trigger kullanılarak otomatik loglama

### Current version: v1.1

## Kullanılan Teknolojiler
- NodeJS
- MySQL (XAMPP)
- phpMyAdmin
- mysql2/promise
- bcrypt / bcryptjs

## ​🛠️​ Özellikler

- Kullanıcı ve rol yönetimi (admin / editor)
- Yazı (post) yönetimi: ekleme, güncelleme, silme, yayınlama
- Kategori sistemi
- Statik sayfa yönetimi (Hakkımızda, İletişim vb.)
- Yorum sistemi
- Veritabanı seviyesinde otomatik loglama (trigger ile)
- 3NF normalizasyonuna uygun veri modeli
- View, Stored Procedure, Transaction ve kompleks SQL sorguları

## 🧱 Veritabanı Tasarımı

Proje veritabanı aşağıdaki gereksinimleri sağlayacak şekilde tasarlanmıştır:

- En az **5 ana tablo + 1 log tablosu**
- PRIMARY KEY ve AUTO_INCREMENT ile benzersiz kayıt yönetimi
- FOREIGN KEY ile tablo ilişkilerinin DB seviyesinde korunması
- CHECK, UNIQUE, DEFAULT ve NOT NULL kısıtlamaları
- INSERT / UPDATE / DELETE işlemleri için trigger tabanlı loglama
- View’lar ile uygulama katmanına sade ve okunabilir veri sunumu

## 📁 Proje Yapısı

nodecore-cms-nodejs/
│
├─ controllers/
├─ middlewares/
├─ routes/
├─ views/
├─ sql/
│ ├─ schema.sql # Veritabanı kurulumu (tablolar, constraint’ler, trigger’lar, view’lar, SP)
│ └─ examples.sql # Kompleks sorgular, transaction örnekleri
│
├─ project-report/
│ └─ CMS_Project_Report.docx
│
├─ app.js
├─ db.js
├─ package.json
├─ .env.example
├─ .gitignore
└─ README.md

yaml
Kodu kopyala


## Kurulum ve Çalıştırma

1) Bağımlılıkları kur:

npm install
.env oluştur:
.env.example dosyasını kopyalayarak .env oluştur ve kendi MySQL bilgilerini yaz.

Veritabanını kur:
phpMyAdmin → SQL sekmesi

Önce sql/schema.sql çalıştır

Sonra sql/examples.sql (opsiyonel / kanıt sorguları)

Uygulamayı çalıştır:

node app.js

Uygulama: http://localhost:3000

## Notlar

+ .env dosyası güvenlik için repo'ya eklenmemiştir.
+ node_modules/ repo dışında tutulmuştur.
