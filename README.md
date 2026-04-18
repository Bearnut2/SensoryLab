# 🧪 SensoryLab AI Project

## 📌 Deskripsi
SensoryLab adalah aplikasi Laravel sederhana untuk pengujian kualitas produk makanan berbasis data numerik (instrument testing).

Fitur utama:
- Input batch produk
- Input hasil pengujian (test data)
- Validasi input otomatis

---

## 🧱 Database Schema

### batches
- id (PK)
- product_name
- product_code (unique)
- batch_number (unique)
- date_created

### test_data
- id (PK)
- batch_id (FK)
- parameter_name
- value (float)
- measurement_unit (nullable)

Relasi:
- 1 Batch → banyak Test Data

---

## 👥 Anggota Tim

- Avantio → Database & ERD  
- Ratna → Class Diagram  
- Naufal → SKILL.md  
- Aliya → Validation  
- Aqilla → Implementasi & Integrasi  

---

## 🔄 Workflow
Avantio → Ratna & Naufal → Aliya → Aqilla

---

## 🤖 AI Tools
- ChatGPT
- GitHub Copilot
- Gemini

---

## ⚠️ Catatan
Semua output dibuat dengan bantuan AI dan disertai screenshot sebagai bukti.
