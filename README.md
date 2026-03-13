# 🎬 Video OCR Extractor v3.0

비디오 특정 영역의 숫자/텍스트를 프레임 단위로 추출하고, 사용자별 이력을 저장하는 앱.

[![Streamlit App](https://static.streamlit.io/badges/streamlit_badge_black_white.svg)](https://share.streamlit.io)

---

## ✨ v3.0 신규 기능

| 기능 | 설명 |
|------|------|
| 👤 사용자 관리 | 사용자 등록/로그인, 개인별 데이터 분리 |
| 📋 추출 이력 저장 | SQLite DB에 세션별 전체 결과 영구 저장 |
| 📁 파일 이력 목록 | CSV/Excel/PDF 내보내기 이력 목록 관리 |
| 🔁 이력 재다운로드 | 과거 세션 결과를 언제든 재다운로드 |
| 📊 사용자별 통계 | 세션수/추출행수/내보내기 현황 대시보드 |

---

## 🚀 Streamlit Cloud 배포

1. 레포 전체를 GitHub에 Push
2. [share.streamlit.io](https://share.streamlit.io) → New app
3. Main file path: `app.py` → Deploy

---

## 📁 파일 구조

```
video-ocr-extractor/
├── app.py                  # 메인 앱 (v3.0)
├── requirements.txt        # Python 패키지
├── packages.txt            # 시스템 패키지 (Tesseract)
├── .streamlit/
│   └── config.toml         # 테마 설정
└── README.md
```

> `ocr_history.db` — 앱 실행 중 자동 생성되는 SQLite DB (이력 저장)

---

## 💻 로컬 실행

```bash
# Ubuntu/Debian
sudo apt-get install tesseract-ocr tesseract-ocr-kor tesseract-ocr-eng

pip install -r requirements.txt
streamlit run app.py
```
