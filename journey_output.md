# 🚀 Journey Output

---

## 🧪 User Story 1 — Create Batch

### Context File
app/Http/Controllers/BatchController.php

### Task
As a QC staff, I want to create a batch so that I can record product identity

### Input
- product_name
- product_code
- batch_number
- date_created

### Output
Redirect dengan success message

### Rules
- Semua field required
- product_code unique
- batch_number unique

### What Changed
Added batch creation feature

### Commit Message
feat(batch): create batch

---

## 🧪 User Story 2 — Validation Test Data

### Context File
StoreTestDataRequest.php

### Task
Validate test data input

### Rules
- batch_id → exists
- value → numeric
- parameter_name → required

### What Changed
Added validation layer

### Commit Message
feat(validation): add test data validation

---

## 🧪 User Story 3 — Submit Test Data

### Context File
TestDataController.php

### Task
Store test data

### Input
- batch_id
- parameter_name
- value
- measurement_unit

### Output
Redirect success

### Rules
- batch harus ada
- value numeric

### What Changed
Added test data submission

### Commit Message
feat(test_data): store data
