# CSV 파일 결합기 (CSV Combiner)

이 프로젝트는 `data/` 폴더 안에 있는 모든 CSV 파일을 하나로 결합하여 `combined_sales.csv` 파일로 저장해주는 간단한 Python 스크립트입니다.

---

## 🔧 사용한 기술

- Python
- pandas
- glob

---

## 📁 폴더 구조

csv-combiner-main/
├── csv-combiner-main/
│   ├── data/
│   │   ├── sample1.csv
│   │   ├── sample2.csv
│   │   └── ...
│   ├── combine_files.py
│   └── combined_sales.csv
├── README_ko.md
└── README_en.md

---

## 🧾 코드 설명 (combine_files.py)

```python
import pandas as pd
import glob

files = glob.glob("data/*.csv")  # data 폴더 안 모든 CSV 파일 경로 찾기
dfs = [pd.read_csv(f) for f in files]  # 모든 CSV 파일을 DataFrame으로 읽어오기

combined = pd.concat(dfs, ignore_index=True)  # 하나의 큰 DataFrame으로 결합
combined.to_csv("combined_sales.csv", index=False)  # 결과 저장