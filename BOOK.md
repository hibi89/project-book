# BOOK.md — GitHub 프로젝트 공통 등록부

> [!IMPORTANT]
> ## ChatGPT 프로젝트 명령·인수인계 공지
> - **ChatGPT 개인지침 우선.** 이 파일은 번호·저장소·최근 작업 시각·상태를 공유하는 등록부이며, 승인·보안·검증 지침을 대체하지 않는다.
> - 메시지 전체가 **`p0`**, **`p1`~`p9`**, **`ㄱ`**일 때만 단축 명령으로 처리한다.
> - **`p0`**: 이 파일 **하나만 읽고**, 마지막 실제 작업 시각이 현재 기준 **3시간 이내**인 프로젝트에 1~9번을 배정·갱신한다. 기존 활성 번호는 가능하면 유지한다. 변경된 경우에만 저장하고 확인 후 번호표 출력. 9개 초과 시 보고한다.
> - **`p1`~`p9`**: 마지막 `p0`에서 확정된 번호의 저장소를 이 파일에서 찾는다. 3시간이 경과해도 마지막 번호는 다음 `p0` 실행 전까지 유효하다. `HANDOFF.md` → `STATUS.md` → `AGENTS.md` → `REQUIREMENTS.md` → 소스·커밋 순으로 검증해 복원한다.
> - **`ㄱ`**: 현재 프로젝트에서 확정된 다음 미완료 작업 **1단위만** 실행·검증·기록한다. 사용자 확인·승인이 필요한 작업은 **실행하지 않고** 이유와 선택지를 보고한 후 중단한다. 다음 단위는 새 `ㄱ`이 있어야 진행한다.
> - **주요 작업 완료·중단·인수인계** 때 해당 프로젝트 `STATUS.md`, `HANDOFF.md`와 중앙 `BOOK.md`를 갱신한다. `BOOK.md`에는 저장소, 마지막 실제 작업 시각(**한국시간**), 상태, 근거 커밋을 기록한다. GitHub 커밋 및 재조회로 검증한다. 단순 질의·변경 없음에는 커밋하지 않는다.
> - 최종 작업 보고 **맨 끝에 BOOK에서 확인한 배정 번호 `p1`~`p9`**를 표시한다. 없으면 `미배정`.
> - 저장소·번호·시각·커밋을 추정하거나 조작하지 않는다. 충돌 시 최신 파일을 재조회하고 변경 내용을 병합한다. 등록부 갱신 자체는 다른 프로젝트의 작업으로 간주하지 않는다.

## 활성 프로젝트 번호표

> 활성 프로젝트는 검증된 마지막 실제 작업 시각을 기준으로 `p0`에서 배정한다. `p0` 조회·등록부 갱신 자체는 활동 시각을 연장하지 않는다.

| 번호 | 프로젝트 | GitHub 저장소 | 마지막 실제 작업 시각 (KST) | 상태 | 근거 커밋 SHA |
| --- | --- | --- | --- | --- | --- |
| p1 | REA Studio · Dashboard Mechanism Skills | `hibi89/web-rea-studio` | 2026-10-18 15:28:10 KST | 활성 · `mvp-three-mode-20261018` · **스킬 3종+CSV/JSON 매핑+오프라인 KPI/SVG HTML+CLI/테스트 커밋** · 로컬 시제품 Node 22.16 10/10 PASS, GitHub 최신 소스 격리 JS 필터 합계 ALL/KR/US/JP 870/450/270/150 확인 · 공식 GitHub Actions·물리 Chrome **미검증** · feature Vercel 빌드 사용량 제한 실패 · main/Production 미변경 · `docs/MECHANISM_SKILLS_RUNBOOK_2026-10-18.md` / `HANDOFF.md` / `STATUS.md` 최신화 | `d674d02e27b6b637b2bbb0e6157625c07c6167fb` |
| p2 | NAON2 Character Studio | `hibi89/NAON2-Character-Studio` | 2026-10-18 00:36:00 KST | 활성 · 841123 (10,000원)·841126 (20,000원) 심사 대기; 기존 840876 (6,000원)은 사용자 삭제 보고, 새로고침한 내 서비스 목록에서 미표시 | `ddc0164a6e28e132d517d0f2d7cc02db7d06584d` |
| p3 | Fable 5.1 Web Catcher | `hibi89/fable5.1_web_catcher` | 2026-10-18 22:32:02 KST | **Step 1 원본 7/7·Step 2 원본 9/9·Step 3 자동 인수 8/8 PASS, Windows 실사이트 35 클릭·중복 0/최종 URL 저장 검증**. **다음 1단위 완료: 헤더 없는 JSON 크기 검증 후 타입 구조 분석(Record 전용)**. PR #3 `f7b9bb9c09bc69cd305519b5676af31ff4b2d7ea` main 병합. 검증 Windows **63/63 PASS** run `39131631123`, 실제 headed Chromium **20/20 PASS** run `39131631050`, 공개 사이트 **4/4 PASS**. Step 2의 헤더 미확인 JSON 정책은 유지, 기존 민감값/인가범위/응답 수량 20건/용량 128KiB 제한 유지. Playwright 바디 디코딩의 절대 메모리 상한 아님. **Windows 실제 외부 API JSON 구조 확보 여부는 재시험 미검증**, generic CSS/SVG 차트↔API 연결 후보 0건은 별도 과제. 배포 없음. HANDOFF/STATUS 및 `docs/STEP3_HEADERLESS_JSON_BOUND_2026-10-18.md` 최신. | `2bd2ff6c3296d316ee1edb27e603beac868e233a` (문서 HEAD; PR #3 병합 `f7b9bb9c09bc69cd305519b5676af31ff4b2d7ea`) |
| p4 | Astra Web Catcher | `hibi89/astra_web_catcher` | 2026-10-18 22:28 KST | **Step 4-C 가상 앱 기능별 수용 검증 한 단위 완료.** `feature/observation-contract-20261018`: 합성 브리지의 가짜 `category=sample` 경로를 실제 가상 샘플 카테고리(인코딩)로 바로잡고 새 `synthetic_acceptance.py`로 템플릿/입력 SHA/trace 정합성, 실제 FastAPI 목록·필터·검색·상세·404·422·문자 escaping·SQLite 영속성을 검증. **로컬 170/170 PASS**(기존 152+신규 18), 8개 생성 파일과 12개 수용 검사 PASS, 별도 가상 채용 사례 PASS, Uvicorn 실제 loopback HTTP 200/404/422, compileall PASS. JSON 결과 `/mnt/data/astra_synthetic_acceptance_20261018.json`. **원본 URL/DB 동작 미검증**, GUI 브라우저 E2E 미실행, `GenerationContract` blocked_pending_review 유지. 다섯 새/수정 소스·테스트·문서 파일 및 HANDOFF/STATUS Git blob SHA 일치, 원격 GitHub author/committer `hibi89` 재조회. `main`·기존 앱·데이터 무변경, 배포 미적용. **다음 ㄱ:** 관찰 근거/필드 의미의 사용자 검토·승인 결정 기록 1단위(실DB 연결/원본 변형은 별도 승인). | `01a8893e1bd89bece837b551bc686b07a8a5842c` (feature HEAD; main `dc23ee604d02513c890615a3a98440c1ea8a5270`) |
| p5 | Astra PDF Redesigner | `hibi89/astra_pdf_redesigner` | 2026-10-18 22:06:03 KST | **STEP 1 자동 검증 완료, STEP 2 블록 모델·STEP 1 비파괴 변환 첫 단위 완료**. 기존 앱/저장키 변경 없음, 로컬 9/9 PASS, GitHub Ubuntu 빌드·Chrome PDF smoke PASS run `39129894290`. STEP 2 UI/이미지 저장/다중 문서/export-import **미구현**. Windows PDF 인쇄 확인 대기. 사용자 확정 최종 목표=원본 PDF 콘텐츠 보존 후 디자인 재조판, 아스트라 단계 순서 유지. `docs/STEP2_DESIGN_DECISION_2026-10-18.md` · `HANDOFF.md` · `STATUS.md` | `3e3503ba0dc80903f810f8507eae35a5a2d1da41` (문서 HEAD; STEP 2 기능 `5eb2b8d5db89f69a2a61254ddd79651d1226ad56`) |
| p6 | OHORA Trend Catcher · Meta Batch API 수집 | `hibi89/ohora-trend-catcher` | 2026-10-18 21:46 KST | **활성 · 설계 목표 기록만 완료, 실행 보류** · 294계정 × 최근 50개(목표 최대 14,700) → 최신 동기화 + 과거 1~2년 확장 + 지표 재관측 · 4탭 대시보드 구상. `docs/LONG_TERM_RAW_COLLECTION_VISION_2026-10-18.md`/STATUS/HANDOFF 기록 · 신규 코드·API 요청·실수집·배포 없음 · 앱 B 기존 토큰 만료/실 API 미검증 · 사용자 후속 토론 대기 | `afc6e01c7c5490cf9003c09e2709416522d70901` (문서 HEAD) |
| p7 | — | — | — | 미배정 | — |
| p8 | — | — | — | 미배정 | — |
| p9 | — | — | — | 미배정 | — |

## 등록 프로젝트 · 번호 미배정

> 번호는 `p0`에서 검증된 최근 3시간 이내 실제 작업을 기준으로 배정한다. 등록 자체는 실제 작업 시각을 만들지 않는다.

| 프로젝트 | GitHub 저장소 | 마지막 실제 작업 시각 (KST) | 상태 | 근거 커밋 SHA |
| --- | --- | --- | --- | --- |

## 운영 규칙

1. **등록부 고정 위치:** 비공개 `hibi89/project-book`, `main`, `/BOOK.md`. 다른 채팅에서도 항상 이 주소를 먼저 사용한다. 이 주소를 ChatGPT 개인지침 0항에도 명시한다.
2. 담당 GitHub 저장소와 프로젝트가 확인되면 최초 등록한다. 해당 저장소의 최신 문서·소스·커밋을 근거로 삼고, 프로젝트가 불명확하면 묻는다.
3. 최근 3시간 판정은 **기록된 실제 작업 시각**을 기준으로 한다. 단순 `p0` 조회·등록부 갱신 시각만으로 활동 시간을 연장하지 않는다.
4. `p0`에서 3시간 지난 프로젝트를 활성 목록에서 제외하더라도 이전 프로젝트 정보가 필요하면 GitHub 이력으로 추적할 수 있다. 번호는 저장 확인 후 확정하고 다음 `p0`까지 유지한다.
5. 갱신 시 현재 `BOOK.md`의 blob SHA를 확인해 조건부 저장한다. 충돌 시 최신 내용 재조회 후 병합·재시도한다. 저장 성공은 커밋 SHA와 다시 읽은 파일 내용으로 확인한다.
6. 작업 상세 상태는 프로젝트의 `HANDOFF.md`·`STATUS.md`가 기준이다. BOOK에 비밀값·토큰·`.env`·고객 개인정보·대용량 원본을 기록하지 않는다.

## 운영 상태

- 중앙 등록부: `hibi89/project-book` / `main` / `BOOK.md`
- 등록된 프로젝트: OHORA Trend Catcher (`p6`, `hibi89/ohora-trend-catcher`, 사용자 요청 수동 배정·마지막 확인 커밋 2026-10-16 11:46:12 KST), REA Studio (`p1`, `hibi89/web-rea-studio`), NAON2 Character Studio (`p2`, `hibi89/NAON2-Character-Studio`), Fable 5.1 Web Catcher (`p3`, `hibi89/fable5.1_web_catcher`, headerless JSON Record 전용 개선 PR #3, Windows63·Chromium20·공개4 PASS, 사용자 실사이트 신규 기능 미검증), Astra Web Catcher (`p4`, `hibi89/astra_web_catcher`), Astra PDF Redesigner (`p5`, `hibi89/astra_pdf_redesigner`, STEP 1 검증·STEP 2 데이터 모델 착수, 9개 테스트·CI PASS, 편집 UI 미구현)
- 현재 번호 배정: `p1`(REA Studio, 실제 작업 2026-10-18 15:28:10 KST), `p2`(NAON2, 실제 작업 2026-10-18 00:36:00 KST), `p3`(Fable 5.1 Web Catcher, 2026-10-18 22:30 KST PR #3 headerless JSON 단위 완료, Windows63·Chromium20·공개4 PASS, 현장 신규 분석 미검증, 문서 HEAD 2bd2ff6c). `p4`(Astra Web Catcher), `p5`(Astra PDF Redesigner, 실제 검증 2026-10-18 21:39:37 KST·STEP 1 Chrome/CI PASS). `p0` 재실행 전 번호 유지. `p6` OHORA Trend Catcher 2026-10-18 21:46 KST 설계 문서 저장 확인, 이후 실행은 사용자 토론·승인 대기. 등록부 갱신 자체로 활동 시간을 연장하지 않음.
