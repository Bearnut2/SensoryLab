Lokasi file ini: /skills/SKILL.md

# SensoryLab Skill Configuration

## Project Context
Aplikasi Laravel untuk pengujian kualitas produk makanan berbasis data numerik.

## Database
- batches
- test_data

## Model Conventions
- Batch hasMany TestData
- TestData belongsTo Batch

## Controller Conventions
- Gunakan RESTful controller
- Validasi wajib sebelum simpan data

## Validation Rules
- product_code → unique
- batch_number → unique
- value → numeric

## Route Conventions
- Gunakan web.php
- Gunakan Route::resource

## View Conventions
- Blade + Tailwind
- Gunakan form sederhana

## Testing
- Gunakan Laravel Feature Test

## Security Rules
- Validasi semua input
- Pastikan foreign key valid
- Hindari data duplikat
