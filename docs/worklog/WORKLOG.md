# 작업 기록

## 2026-09-28 — 첫 점검 (Claude Code 처음 투입)

### 한 일
- 저장소 전체 확인: 실제 내용이 있는 페이지는 `index.html`(랜딩) 하나. `shop/`, `dashboard/`는 제목만 있는 자리표시, `os/`, `ads/`, `design/`, `jeongmoo/`는 빈 파일.
- 변경 이력 확인: 2026-03-16 시작 → 05-19 사업자 정보 추가 → 06-26 랜딩 전면 교체(식식이OS 신규) 및 하단 정리. 이후 변경 없음.
- 실제 사이트 점검: siksiki.com은 Vercel에서 운영, www.siksiki.com으로 넘어감. 실제 화면 내용 = 저장소 main 과 동일.
- 페이지 안 모든 링크 점검 (결과 아래).
- 표준에 맞춰 문서 생성: CLAUDE.md, docs/STATUS.md, docs/DECISIONS.md, docs/worklog/WORKLOG.md, DFAITH-DOC-STANDARD.md 복사, docs/design/ 폴더.
- `.vercelignore` 생성 (내부 문서 공개 방지).
- 사이트 화면 파일은 수정하지 않음 (이유는 DECISIONS.md).

### 검사 결과
| 주소 | 결과 |
|---|---|
| siksiki.com | 정상 (www.siksiki.com으로 임시 이동, 307) |
| siksiki.com/og-image.png (공유 미리보기 이미지) | ❌ 없음 (404) |
| siksiki.com/robots.txt, /sitemap.xml | ❌ 없음 (404) |
| siksiki.com/favicon.ico | 있음, 단 투명 1×1 점 |
| restaurant.siksiki.com (시작하기) | 정상 → 로그인 화면, 회원가입 링크 있음 |
| app.siksiki.com (공급자 입점 문의) | 로그인 화면만 있음, 제목 "RealMyOS", 문의 수단 없음 |
| /os, /ads, /jeongmoo | 빈 흰 화면 (공개 상태) |
| /shop, /dashboard | 제목 한 줄 자리표시 (공개 상태) |

### 발견한 문제
- 16건, docs/STATUS.md BACKLOG 표에 정리.

### 다음 할 일
- 대표가 BACKLOG 중 결정 필요한 항목(이미지, 카톡 채널 주소, 회사명, 무료체험 여부, 빈 페이지 처리) 정하기
- 새 문서들을 커밋할지 결정 (아직 커밋 안 함)
