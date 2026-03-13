# 🎬 Video OCR Extractor v2.1

비디오의 특정 영역을 지정하여 초 단위로 텍스트/숫자를 추출하고 표로 저장하는 앱입니다.

[![Streamlit App](https://static.streamlit.io/badges/streamlit_badge_black_white.svg)](https://share.streamlit.io)

---

## ✨ 주요 기능

- 🎥 비디오 업로드 (MP4, MOV, AVI, WebM)
- 🖱️ 드래그로 OCR 영역 선택 (캔버스 인터페이스)
- 🔢 숫자 특화 OCR (LCD 디스플레이, 계기판 등)
- 📊 결과를 **CSV / Excel / PDF / TSV** 로 내보내기
- 🔍 실시간 전처리 미리보기

---

## 🚀 Streamlit Cloud 배포 방법

1. 이 레포를 GitHub에 Push
2. [share.streamlit.io](https://share.streamlit.io) 접속
3. **New app** → Repository 선택
4. Main file path: `app.py`
5. **Deploy** 클릭

---

## 💻 로컬 실행

```bash
# 시스템 패키지 설치 (Ubuntu/Debian)
sudo apt-get install tesseract-ocr tesseract-ocr-kor tesseract-ocr-eng

# Python 패키지 설치
pip install -r requirements.txt

# 앱 실행
streamlit run app.py
```

### macOS
```bash
brew install tesseract tesseract-lang
pip install -r requirements.txt
streamlit run app.py
```

---

## 📁 파일 구조

```
video-ocr-extractor/
├── app.py                  # 메인 Streamlit 앱
├── requirements.txt        # Python 패키지
├── packages.txt            # 시스템 패키지 (Streamlit Cloud용)
├── .streamlit/
│   └── config.toml         # 테마 및 서버 설정
└── README.md
```

---

## ⚙️ OCR 설정 가이드

| 설정 | 권장값 | 용도 |
|------|--------|------|
| 언어 | 영어 | 숫자 추출 시 정확도 높음 |
| OCR 모드 | 숫자 위주 | 소수점·부호 포함 숫자 |
| 이미지 확대 | 3× | 작은 글씨 인식률 향상 |
| 전처리 | 반전+대비 | 밝은 LCD 디스플레이 |

---

## 📦 사용 라이브러리

- [Streamlit](https://streamlit.io) — UI 프레임워크  
- [OpenCV](https://opencv.org) — 비디오 프레임 추출  
- [Tesseract OCR](https://github.com/tesseract-ocr/tesseract) — 문자 인식 엔진  
- [streamlit-drawable-canvas](https://github.com/andfanilo/streamlit-drawable-canvas) — 영역 선택  
- [openpyxl](https://openpyxl.readthedocs.io) — Excel 생성  
- [fpdf2](https://py-fpdf2.readthedocs.io) — PDF 생성  
