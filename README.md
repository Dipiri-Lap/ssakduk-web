# 싹둑 웹사이트 (정적 사이트)

- `index.html` 메인 소개 페이지
- `cancel/` 구독 서비스 38개 해지 방법 (서비스별 페이지)
- `guide/` 구독 관리 가이드 4편 (무료체험 자동결제, 구글 플레이, 아이폰, 가족 정산)
- `prices/` 공식 요금이 확인된 서비스 요금 비교
- `sitemap.xml`, `robots.txt`, `404.html`

## 배포 전에 할 것
1. 도메인이 정해지면 BASE 주소를 바꿔서 다시 생성해야 해요 (현재 임시값: https://ssakduk.tmhub.co.kr).
   canonical, og:url, sitemap.xml, robots.txt에 들어가요.
2. 폴더 전체를 정적 호스팅(GitHub Pages, Vercel, Netlify, Cloudflare Pages)에 올리면 돼요. 빌드 과정 없음.
3. 검색 등록: Google Search Console, 네이버 서치어드바이저에 사이트 등록 후 sitemap.xml 제출.

## 데이터 출처
- 요금·해지 방법: `src/data/catalog.ts` (2026-10-23 조사)
- 요금 숫자는 `docs/CATALOG_NOTES.md`에서 '공식'으로 확인된 서비스만 표시해요.
- 넷플릭스 해지 절차는 넷플릭스 고객센터(help.netflix.com/ko/node/407) 기준.
- 생성 스크립트: `scripts/build-site.aside.js` (Aside가 실행, 카탈로그가 바뀌면 다시 생성)
