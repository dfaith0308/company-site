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

## 2026-09-28 — 문서 저장, 랜딩 관리자 요청 접수
- 첫 점검 문서들 커밋(3c79e39). 인터넷 반영(push)은 하지 않음.
- 대표 요청: 광고용 랜딩이므로 ① 효과 측정 ② 쉬운 문구·사진 수정(관리자 화면) 필요.
- 참고: 다른 식식이 서비스(siksiki-os, siksiki-console)는 Next.js + Supabase로 만들어져 있음 → 같은 도구로 관리자 화면을 만들 수 있음.
- 다음: 대표가 방식 결정 → 설계서 docs/design/v1-step1-랜딩관리자.md 작성

## 2026-09-28 — 랜딩 관리자 설계서 작성
- 대표 결정: 직접 제작, 무거운 버전, 광고 매체 네이버·인스타·유튜브.
- 설계서 5개 작성: docs/design/v1-step0(개요) ~ step4(식식이 이전).
- 판단 4건 DECISIONS.md에 기록 (새 프로젝트로 분리, 칸 쌓기 방식, 이메일 알림, 테스트 주소 먼저).
- 다음: 대표 설계서 확인 → 새 저장소 만들기(대표 승인 필요) → step1 제작.

## 2026-09-28 — 랜딩OS 프로젝트 분리
- C:\dev\Vault\landing-os 생성, 설계서 5개·문서 표준 옮김. 이쪽 docs/design 에는 옮긴 위치 안내만 남김.
- 인터넷 반영(push)은 여전히 하지 않음.
