# 📊 Database & Class Diagram

## 🧱 Database Schema

### batches
| Kolom | Tipe | Keterangan |
|------|------|-----------|
| id | bigint | Primary Key |
| product_name | string | Nama produk |
| product_code | string | Unique |
| batch_number | string | Unique |
| date_created | date | Tanggal |
| created_at | timestamp | |
| updated_at | timestamp | |

---

### test_data
| Kolom | Tipe | Keterangan |
|------|------|-----------|
| id | bigint | Primary Key |
| batch_id | bigint | Foreign Key |
| parameter_name | string | Nama parameter |
| value | float | Nilai |
| measurement_unit | string | Nullable |
| created_at | timestamp | |
| updated_at | timestamp | |

---

## 🔗 Relasi
- Batch hasMany TestData
- TestData belongsTo Batch

---

## 🧩 ERD (ASCII)

batches
+-------------------+
| id (PK) |
| product_name |
| product_code (UQ) |
| batch_number (UQ) |
| date_created |
+-------------------+
|
| 1
|
| *
+-------------------+
| test_data |
+-------------------+
| id (PK) |
| batch_id (FK) |
| parameter_name |
| value |
| measurement_unit |
+-------------------+

---

## 📌 Constraint
- product_code → unique
- batch_number → unique
- batch_id → foreign key (cascade delete)

---

## ⚡ Indexing
- index(batch_id, parameter_name) → mempercepat query filter

---

## 🧪 Dummy Data

### batches
1. Keripik Singkong | P001 | B001
2. Kerupuk Udang | P002 | B002
3. Snack Jagung | P003 | B003

### test_data
- pH, 6.5
- Suhu, 30°C
- Kekerasan, 12

---

## 🔄 Alur Sistem
1. QC membuat batch
2. Sistem menyimpan data batch
3. QC input test_data
4. Data tersimpan dan terhubung ke batch
