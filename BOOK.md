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
| p3 | Fable 5.1 Web Catcher | `hibi89/fable5.1_web_catcher` | 2026-10-19 KST | **사용자 제공 Step 1~5 구현·자동/Mock 인수 기준 5/5단계 완료**. 신규 [PR #16](https://github.com/hibi89/fable5.1_web_catcher/pull/16) Step5(UTF-8 순차 배치·원자적 manifest/상대경로 한국어 요약, 두 저장 결과 오프라인 비교, 값 없는 관찰 JSON 계약·Draft2020-12 참고 Schema) main 병합 `7de7e26faec46120bbdfb509892ca267cea514c4`. 프라이버시: 원본 host/path/query 일반화, 실행별 익명 pseudo-origin; 배치 로그인·LLM 자동 호출/병렬·resume 없음. 3개 localhost URL 실제 배치 → 결과 2개 diff → 결과 1개 contracts.md 연속 fixture **PASS**. **Windows 123/123 PASS** [39148097390](https://github.com/hibi89/fable5.1_web_catcher/actions/runs/39148097390), **기존 Chromium 23/23 PASS + 선택 공개 smoke 4/4 PASS** [39148097419](https://github.com/hibi89/fable5.1_web_catcher/actions/runs/39148097419). **실제 3개 외부 사이트 배치 Runtime 사용 / 사용자 Windows Step3 필터·차트 실증 / Step4 유료 API smoke는 미검증**. 상용제품 모든 환경 최종 100% 아님. 문서 `docs/STEP5_FINAL_ACCEPTANCE_2026-10-19.md`, HANDOFF/STATUS 최신. | `dd7132f294beeaee89dd1f103558efb0ef60bbfa` (main HANDOFF HEAD; PR16 merge `7de7e26faec46120bbdfb509892ca267cea514c4`) |
| p4 | Astra Web Catcher | `hibi89/astra_web_catcher` | 2026-10-19 10:53:31 KST | **문서화된 독립 기능 2개를 읽기 전용 표준 비교 계약으로 연결.** 새 `astra_contracts/mechanism_contract_review.py`: 기존 텍스트 폼(`my-text`→Submit→local `Received!`)과 체크박스(`checkbox_input`→local Checked/Unchecked)의 input·trigger·output·transport·증거 수준 구분, 두 모듈 Git blob SHA-1 및 3개 문서 증거 SHA-256 고정 검증; 누락/변조/symlink/경로 탈출/트리거 바꿔치기/권한 승격 차단. 신규 **22/22** + 이전 체크박스 **11/11**, 총 이번 부분 테스트 **33/33 PASS**, Python compileall PASS, GitHub 코드·테스트 소스 blob 재조회 로컬 테스트본과 일치. **완전 체크아웃에서의 기본 2모듈 CLI 실행, 기존 739 전체 회귀, 실제 원본 웹 클릭/스크린샷/동등성, 고객 DB/API 연동은 미검증·미구현.** 브라우저 연결 기능은 읽기 전용, 기존 관리자 차단 브라우저 재시도 없음. feature-only, main 불변, Actions/Vercel 미사용. `review_only_no_approval`, `GenerationContract=blocked_pending_review`; 완료율 **~49% 유지**. 다음 `ㄱ`: 실제 허가된 브라우저 관찰 확보 가능성 또는 사용자 소유 스키마 기반 실제 기능 검증 전환(추가 모형 UI 양산 지양). 상세 `docs/TWO_CONTROL_MECHANISM_REVIEW_V01.md`, STATUS/HANDOFF. | `5c20011b7d0ba26100f02601cd8a9838ffc189d9` (feature HEAD docs; code `f8103f07aad9599cf8d5164bf7934f66c5389361`; test `788e879471d1d8ea3abd6c033117f7b0e60b4b26`; main `dc23ee604d02513c890615a3a98440c1ea8a5270`) |
| p5 | Astra PDF Redesigner | `hibi89/astra_pdf_redesigner` | 2026-10-19 10:48:52 KST | **STEP3 신규 이미지 누락/좌표 회귀 3건 검증 + Edge CI 연결 실패 최소 수정 완료.** 기능 브랜치 `feature/step3-pdf-import-20261019` SHA `aa63fc262d0a2db080be4be82bd91d7b4a5b3976`, 이전 테스트 SHA `2200836cc529f4272e78456783d36e50f6b0142c`에서 Actions [#39185454384](https://github.com/hibi89/astra_pdf_redesigner/actions/runs/39185454384) **Node29/29·빌드·Chrome PASS, Edge CDP 35s timeout으로 전체 FAIL**. Edge만 connect 제한 60s(Chrome35s 유지) 수정 후 [#39186875371](https://github.com/hibi89/astra_pdf_redesigner/actions/runs/39186875371) **SUCCESS**, Node29/29·TS/Vite·Chrome 및 Linux Edge155 STEP1~3 이미지 포함 PDF/DB 회귀 PASS. 기능 `src/**` 수정 없음, STEP3 Draft PR #3 open/unmerged, main STEP3 미병합. 실제 PDF 5~10개·Windows Edge/장문·복잡 클리핑/표/회전 미검증. 비공식 STEP3 65~70%, 전체 38% 유지. STATUS/HANDOFF main 최신화, 다음 `ㄱ`: 복잡 이미지 fixture 경고·복원 경계 확대. | `c58a2a6b50d6570fc4a198546ab8520cd62b3b7e` (main docs HEAD; CI-verified feature `aa63fc262d0a2db080be4be82bd91d7b4a5b3976`) |
| p6 | OHORA Trend Catcher · RAW v2.1 daily-first 수집 및 계정별 현황표 | `hibi89/ohora-trend-catcher` | 2026-10-19 KST | 공식 294계정. 운영 우선순위: 매일 front 관측 → catchup → 여유 history; 4건/계정, 5계정/배치, 슬롯 최대150, Meta 사용량85%, 슬롯 종료+63분/시작+65분 쿨타임. 사용자 Windows 확인 2026-10-19: 5계정 History HTTP200, 첫 연속 슬롯 150계정 완료·신규580·누적1930, audit PASS는 실행 전 1330건 시점; 8계정 차단, 무인 운영 미승인, 365일 완전성 미검증. 독립 읽기 전용 `raw_v2/account_collection_status.py` 추가: 계정별 보유 게시일, 마지막 front, KST 오늘 조회, catchup/history 상태를 CSV/MD로 출력. 합성 테스트 추가, Windows 운영 DB 실검증 대기. 실행법 `docs/RAW_V2_ACCOUNT_COLLECTION_STATUS.md`. | `d14926cb66e7737e4cb52a68933d06525c273a83` |
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
- 등록된 프로젝트: OHORA Trend Catcher (`p6`, `hibi89/ohora-trend-catcher`, 사용자 요청 수동 배정·마지막 확인 커밋 2026-10-16 11:46:12 KST), REA Studio (`p1`, `hibi89/web-rea-studio`), NAON2 Character Studio (`p2`, `hibi89/NAON2-Character-Studio`), Fable 5.1 Web Catcher (`p3`, `hibi89/fable5.1_web_catcher`, Step5 배치/비교/계약 통합 123/23/4 PASS, Step1~5 자동/Mock 5/5), Astra Web Catcher (`p4`, `hibi89/astra_web_catcher`), Astra PDF Redesigner (`p5`, `hibi89/astra_pdf_redesigner`, STEP 2 feature 빌드·Chrome 스모크 PASS, main 미병합·추가 검수 대기)
- 현재 번호 배정: `p1`(REA Studio, 실제 작업 2026-10-18 15:28:10 KST), `p2`(NAON2, 실제 작업 2026-10-18 00:36:00 KST), `p3`(Fable 5.1 Web Catcher, 2026-10-19 Step5 10/10 자동 인수, 전체 Step1~5 5/5 구현, Windows123·Chromium23·공개4 PASS, 실제 외부 배치/유료 API/Windows 현장 미검증, HANDOFF dd7132f2). `p4`(Astra Web Catcher), `p5`(Astra PDF Redesigner, 실제 검증 2026-10-18 21:39:37 KST·STEP 1 Chrome/CI PASS). `p0` 재실행 전 번호 유지. `p6` OHORA Trend Catcher 2026-10-19 KST 4-post×150-account slot code main 2c04b77d57a0549dbfb696b1bcf31ae1ef0383c7, GitHub Actions 28/28 PASS, real API 4-post limit pending.13.5 오프라인 20/20 PASS, main 4af906512e1146ed8c9394ae36c387f7f72b006d 재조회 기준. 실제 Meta/Windows/Actions는 미검증으로 사용자 PC 검증 대기. 등록부 갱신 자체로 활동 시간을 연장하지 않음.
