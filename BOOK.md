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
| p4 | Astra Web Catcher | `hibi89/astra_web_catcher` | 2026-10-19 KST | **첫 실제 공개 웹 참조 Selenium Web form 수동적(read-only) 관찰 및 공식 문서 확인**: 입력창·Submit 렌더 텍스트 확인, 공식 예제의 `name=my-text`→Submit→`Received!`는 퍼블리셔 설명일 뿐 **직접 클릭 미검증**. 실 URL 조작/브라우저 검증 불가, 기존 차단 사이트 미재시도. 로컬 오프라인 근거 검토+명시 실행형 Selenium 캡처 스크립트 작성, **신규 36/36·관련 합산 160/160 PASS**, compileall PASS, 전체 716 수집했으나 전부 실행하지 않음. **GitHub에는 근거 문서+트리아지 JSON 2개만 기능 커밋 `61dcdb7a`로 보존**, 코드·테스트는 대화 아카이브 `astra_p4_public_reference_probe_20261019.zip`에 있으나 원격 미반영(전송 제한). 기존 `main`·고객 DB/API 불변, preflight `blocked_pending_review`. **전체 추정 49% 유지**. **다음 ㄱ:** 로컬 원본을 브랜치에 완전히 이관해 통합 회귀하고, 실제 승인된 환경이 있을 때만 공개 데모 버튼 1회 검증. | `61dcdb7a20b73c21e916a9ead1b7713807b57191` (public source docs commit; feature HEAD follows handoff/status, main unchanged) |
| p5 | Astra PDF Redesigner | `hibi89/astra_pdf_redesigner` | 2026-10-19 | **STEP3 기존 PDF 가져오기 첫 실사용 흐름 MVP 구현·Chrome/Edge CI 검증 성공, main 미병합.** [Draft PR #3](https://github.com/hibi89/astra_pdf_redesigner/pull/3): `feature/step3-pdf-import-20261019` → `main`, Draft 유지. 기반: STEP2 안정 main, 마지막 코드 CI #39157047624 success. STEP3 새 `pdfjs-dist 6.4.299`(Apache-2.0) 브라우저 로컬 PDF 파서: 30MiB/50p, 텍스트/viewport 원본 좌표·단일열 읽기순서/제목/본문/캡션 추정, Blob PDF 원본 뷰어와 추출 블록 순서/분류/내용 수동 수정, 이미지 미복원·혼합·스캔·다단 누락 위험 경고, 사용자 확인 후 기존 원본 보존하며 신규 schemaVersion2 문서 단일 IDB 트랜잭션 저장·STEP2 테마/PDF 인쇄 연계. 구현 검증 코드 SHA **`e216866a592362342ac6dd2ca2105b71799cc8fc`**, [Actions #39159350165](https://github.com/hibi89/astra_pdf_redesigner/actions/runs/39159350165) **SUCCESS**: Node **21/21 PASS**, TS/Vite build, Chrome/Edge 각각 합성 선택형 PDF 생성→PDF.js 원본 대조→별도 문서 저장→테마·리로드→A4 PDF 재출력 E2E PASS, 기존 STEP1/2 이미지·저장·멀티탭·V1 migration 복구 회귀 PASS. **미완료:** 사용자 실제 단순 PDF 5~10개 원문/추출 검수, PDF 이미지 원본 자동 복원, Windows Chrome/Edge 실제 PDF 가져오기 및 이전 STEP2 Windows Edge 장문/이미지·키보드 육안 검수는 NOT RUN. OCR/복잡 다단·표 재현 제외. STEP3 전체 검증 완료·main 병합 승인 아님, Draft 유지. [설계](https://github.com/hibi89/astra_pdf_redesigner/blob/feature/step3-pdf-import-20261019/docs/STEP3_PDF_IMPORT_DESIGN_2026-10-19.md) / [MVP 검증 보고](https://github.com/hibi89/astra_pdf_redesigner/blob/feature/step3-pdf-import-20261019/docs/STEP3_MVP_IMPLEMENTATION_AND_CI_2026-10-19.md). **비공식 동등비중 진행률: STEP1 100%, STEP2 기술 구현 99%(Windows 미완료), STEP3 약45~50%, STEP4~7 0%; 전체 약35%(이전 28~29% 대비 유의미 상승).** 다음: PDF 이미지 감지/누락·읽기순서/혼합 페이지 실 PDF 정확도 검증 후 단계별 구현. | `09fdc4441830937ee096fa5a7dcde71e8884954d` (main HANDOFF/STATUS docs-only; STEP3 Draft PR feature head `95e00103c71854d963a9ec24574f5ab6a785fa66`; tested code `e216866a592362342ac6dd2ca2105b71799cc8fc`) |
| p6 | OHORA Trend Catcher · RAW v2 Meta Batch 수집 | `hibi89/ohora-trend-catcher` | 2026-10-19 KST | **다음 실험 4게시물×최대150계정/slot**로 최종 결정(기존 15~25개 시험 반복하지 않음). 기실측 130계정 시도·126성공·4 Meta 110 Invalid user id·누적 630 게시물·`total_time` 76% 중단. 코드 default `--limit 4` / optional 5 rollback, 기존 5개 데이터·커서 보존, FRONT/HISTORY 독립, 계정별 역방향 4개 cursor, 365일 고정 anchor, DB add-only metadata. 150+144=294 이상적 2-slot 순회(요청 한도·실패 시 더 많은 회차). 터미널 반복 실행 수동 opt-in: 시작 간격 최소70분 + 종료 뒤 60분, API 안전중단70%. GitHub Actions Python 3.11 합성 **28/28 PASS** (run 39141110684), Windows·Meta 실 4×150·과거 실제 커서 미검증. 다음: `git pull`, Windows 28테스트 및 기존 LOCALAPPDATA DB `--limit 4 --batch-size 5 --max-batches 30 --stop-usage 70 --live` (쿨다운 끝난 뒤 사용자 명시 실행). | `2c04b77d57a0549dbfb696b1bcf31ae1ef0383c7` (latest app docs; CI source/run 39141110684) |
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
