# 3DGS_Docker


Docker 다 깐 이후부터 




## 📌 COLMAP

### ✅ 2. 작업 디렉토리 만들기

COLMAP은 작업 결과를 저장할 경로가 필요해요. 예를 들어:

```bash

mkdir /workspace/sparse
mkdir /workspace/dense

```

---

### ✅ 3. Feature 추출

```bash

colmap feature_extractor \
    --database_path /workspace/database.db \
    --image_path /workspace/images

```

---

### ✅ 4. Feature 매칭

```bash

colmap exhaustive_matcher \
    --database_path /workspace/database.db

```

---

### ✅ 5. SfM 재구성 (sparse reconstruction)

```bash

colmap mapper \
    --database_path /workspace/database.db \
    --image_path /workspace/images \
    --output_path /workspace/sparse

```

---

### ✅ 6. 포인트 클라우드 확인 (옵션: GUI 모드에서)
```bash
colmap gui
```
