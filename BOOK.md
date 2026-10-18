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
| p3 | Fable 5.1 Web Catcher | `hibi89/fable5.1_web_catcher` | 2026-10-18 21:39:00 KST | **Step 1 원본 7/7·Step 2 원본 9/9·Step 3 자동 인수검사 8/8 PASS**. 실제 사용자 Record 47.344초에서 SPA 문서 ID/클릭 중복·browser_closed 최종 URL 누락·차트 ID 충돌 가능성 검출→PR #2 main 병합으로 보정. Windows **60/60 PASS** run `39128145838`, 실제 headed Chromium **19/19 PASS** run `39128145939`, 공개 페이지 선택 smoke **4/4 PASS**. 검증 소스 `173d42d3...`, merge `b5496a61...`. API는 대시보드와 별개 origin이라 응답 구조 기본 분석 제외(명시적 `--allow-origin` 필요). generic SVG/CSS 차트→API 후보 0건은 인과 근거 부족으로 강제 링크 금지. **사용자 Windows 수정 후 재시험 미검증**, 배포 없음. HANDOFF/STATUS/`docs/STEP3_REAL_RECORD_FEEDBACK_2026-10-18.md` 최신. | `dc6b1c86842a427bf022969a594fe57f245eba8d` (문서 HEAD; 기능 병합 `b5496a61bd82d56204bdab24c984288230a95713`) |
| p4 | Astra Web Catcher | `hibi89/astra_web_catcher` | 2026-10-18 21:45 KST | **Step 4-C 독립 코드생성 안전 사전계약 구현(1단위)**. `feature/observation-contract-20261018`에 기능명세·스키마·매핑보고서 재검증, SHA 일치, 경로탈출·승인위조·보고서조작 차단, 독립 생성 예정 파일 목록만 내는 `contract_only` 사전검사 추가. 샘플 8가지 생성차단 사유, 7 기존 승인게이트/4 추가 검토항목. **로컬 pytest 111/111 PASS**(기존 71+신규 40), CLI 골든 JSON 일치, compileall PASS; 5개 신규 파일+HANDOFF/STATUS Git blob SHA·브랜치 HEAD·GitHub 작성자 재조회 확인. 실제 코드 생성·파일 기록·DB/API 접근·배포 **전혀 없음**. `main` 및 앱·기존 DB 불변. **다음 ㄱ:** 격리된 합성 데이터 기반 코드 생성 프로토타입 또는 사용자 검토 워크플로 중 1단위 선택 후 실제 실행·테스트. 실제 고객 데이터 접속/소스 변경은 별도 승인 필요. | `c122cd948e2ca47e6145df6700656276ba35f317` (feature HEAD; main `dc23ee604d02513c890615a3a98440c1ea8a5270`) |
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
- 등록된 프로젝트: OHORA Trend Catcher (`p6`, `hibi89/ohora-trend-catcher`, 사용자 요청 수동 배정·마지막 확인 커밋 2026-10-16 11:46:12 KST), REA Studio (`p1`, `hibi89/web-rea-studio`), NAON2 Character Studio (`p2`, `hibi89/NAON2-Character-Studio`), Fable 5.1 Web Catcher (`p3`, `hibi89/fable5.1_web_catcher`, Step 1 7/7·Step 2 9/9·Step 3 자동검증 8/8, 현장 SPA 버그 수정 Windows60·Chromium19 PASS), Astra Web Catcher (`p4`, `hibi89/astra_web_catcher`), Astra PDF Redesigner (`p5`, `hibi89/astra_pdf_redesigner`, STEP 1 검증·STEP 2 데이터 모델 착수, 9개 테스트·CI PASS, 편집 UI 미구현)
- 현재 번호 배정: `p1`(REA Studio, 실제 작업 2026-10-18 15:28:10 KST), `p2`(NAON2, 실제 작업 2026-10-18 00:36:00 KST), `p3`(Fable 5.1 Web Catcher, 현장 Record 피드백/SPA 중복 수정 자동검증 2026-10-18 21:39 KST, Windows60·Chromium19·공개4 PASS, Windows 실제 재시험 미검증, 문서 HEAD dc6b1c86). `p4`(Astra Web Catcher), `p5`(Astra PDF Redesigner, 실제 검증 2026-10-18 21:39:37 KST·STEP 1 Chrome/CI PASS). `p0` 재실행 전 번호 유지. `p6` OHORA Trend Catcher 2026-10-18 21:46 KST 설계 문서 저장 확인, 이후 실행은 사용자 토론·승인 대기. 등록부 갱신 자체로 활동 시간을 연장하지 않음.
