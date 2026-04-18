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
