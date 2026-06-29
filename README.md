# 원케어 배관 랜딩사이트

부천 하수구막힘, 싱크대막힘, 변기막힘, 배관막힘 상담용 정적 1페이지 웹사이트입니다.

## 배포 주소

- 기본 Cloudflare Pages 주소: `https://onecare.pages.dev/`

## 프로젝트 구조

```txt
/
├─ index.html
├─ robots.txt
├─ sitemap.xml
├─ _headers
├─ _redirects
├─ 404.html
└─ README.md
```

## Cloudflare Pages 설정값

```txt
Framework preset: None
Build command: 비워두기
Build output directory: .
Production branch: main
```

## GitHub에 처음 올리는 CMD 명령어

```cmd
git init -b main
git add .
git commit -m "first deploy"
git remote add origin GitHub_리포지토리_URL
git push -u origin main
```

## 수정 후 다시 배포하는 CMD 명령어

```cmd
git add .
git commit -m "update website"
git push
```

Cloudflare Pages를 GitHub 리포지토리와 연결해두면 `git push` 후 자동으로 다시 배포됩니다.

## 네이버 서치어드바이저 등록 순서

1. 네이버 서치어드바이저 접속
2. 사이트 등록: `https://onecare.pages.dev/`
3. 소유확인 진행
4. `index.html`의 `NAVER_VERIFICATION_CODE`를 실제 네이버 인증코드로 교체 후 다시 배포
5. 사이트맵 제출: `sitemap.xml`
6. 웹 페이지 수집 요청: `https://onecare.pages.dev/`
7. URL 검사
8. 네이버 검색창에서 `site:onecare.pages.dev` 검색

## 소유확인 HTML 파일 방식 사용 시

네이버가 제공한 파일을 프로젝트 루트에 그대로 넣으세요.

예:

```txt
naverxxxxxxxxxxxx.html
```

배포 후 아래 주소에서 직접 열려야 합니다.

```txt
https://onecare.pages.dev/naverxxxxxxxxxxxx.html
```

## 배포 후 확인 URL

```txt
https://onecare.pages.dev/
https://onecare.pages.dev/robots.txt
https://onecare.pages.dev/sitemap.xml
```

`robots.txt`는 반드시 아래처럼 보여야 합니다.

```txt
User-agent: *
Allow: /

Sitemap: https://onecare.pages.dev/sitemap.xml
```

## SEO 점검 포인트

- title은 너무 길지 않게 유지
- description은 한 문장으로 명확하게 작성
- canonical, og:url, sitemap URL은 실제 배포 주소와 동일하게 유지
- `robots.txt` 파일명은 반드시 `robots.txt`
- 네이버 소유확인 코드가 비어 있으면 소유확인이 실패하므로 실제 코드로 교체
