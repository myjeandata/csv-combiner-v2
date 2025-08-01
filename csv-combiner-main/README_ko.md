# CSV 파일 병합기 (CSV Combiner)

## 프로젝트 개요
여러 개의 CSV 파일을 하나로 합치는 Python 스크립트를 구현한 프로젝트입니다.

## 주요 기능
- `data` 폴더 안의 모든 `.csv` 파일을 자동으로 탐색
- `pandas`를 사용해 모든 파일을 병합
- 병합 결과를 `combined_sales.csv`로 저장

## 사용 방법
1. `data` 폴더에 CSV 파일들을 넣습니다.
2. `combine_files.py` 실행
3. 병합된 결과는 `combined_sales.csv`에 저장됩니다.

## 사용 기술
- Python 3.x
- pandas
- glob

## 파일 구조
project/
│
├── data/
│ ├── sample1.csv
│ └── sample2.csv
│
├── combine_files.py
├── combined_sales.csv
└── README_ko.md
