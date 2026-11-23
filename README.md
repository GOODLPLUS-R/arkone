# 청라 아크원 푸르지오 오피스텔·상가 분양 홈페이지

정적 HTML 한 장짜리 분양 안내 페이지입니다. 빌드 과정이 없어서 GitHub Pages로 바로 게시할 수 있습니다.

## 구성

```
.
├── index.html      # 페이지 전체 (HTML + CSS + JS)
├── assets/         # 조감도, 배치도, 커뮤니티 이미지
├── .nojekyll       # GitHub Pages가 Jekyll 처리를 건너뛰도록 함
└── README.md
```

## GitHub Pages로 게시하기

1. GitHub에서 새 저장소를 만듭니다. 예: `arkone-prugio`
2. 이 폴더의 파일 전체를 저장소 최상위에 올립니다.
   - 웹: 저장소 화면의 **Add file → Upload files**에서 `index.html`, `assets` 폴더, `.nojekyll`을 끌어다 놓고 **Commit changes**
   - 터미널:
     ```bash
     git init
     git add .
     git commit -m "분양 홈페이지 첫 게시"
     git branch -M main
     git remote add origin https://github.com/<계정>/<저장소>.git
     git push -u origin main
     ```
3. 저장소 **Settings → Pages**에서 **Source**를 `Deploy from a branch`, 브랜치를 `main`, 폴더를 `/ (root)`로 지정하고 **Save**합니다.
4. 1~2분 뒤 `https://<계정>.github.io/<저장소>/` 주소로 접속됩니다.

## 정식 도메인 연결

1. 저장소 최상위에 `CNAME` 파일을 만들고 도메인 한 줄만 적습니다. 예: `www.example.com`
   (Settings → Pages의 **Custom domain**에 입력해도 같은 파일이 만들어집니다.)
2. 도메인 업체의 DNS 설정에서 `www`는 `CNAME` 레코드로 `<계정>.github.io`를 가리키게 합니다.
3. DNS 반영 후 Pages 설정에서 **Enforce HTTPS**를 켭니다.

## 수정할 때 확인할 곳 (`index.html`)

| 내용 | 찾을 단어 |
|---|---|
| 상담 전화번호 | `1666-4250` (여러 곳) |
| 청약·계약 일정 | `12월 7일`, `12/7` |
| 타입별 공급금액 | `공급금액 (VAT 포함)` |
| 개인정보처리방침 본문 | `id='pv'` |
| 하단 사업자 정보 | `<footer>` |
| 팝업 | `id="pop"` |

## 게시 전 확인 사항

- 분양 조건과 금액은 입주자모집공고(2026.11.20)와 반드시 대조하세요.
- 개인정보처리방침의 보유기간과 보호책임자 등은 시행사 확인을 받은 뒤 게시하세요.
- 이 페이지는 외부 서버로 개인정보를 보내지 않습니다. 예약과 문의는 전화로만 받습니다.
- 글꼴은 Google Fonts(Noto Sans KR, Noto Serif KR)를 불러옵니다.
