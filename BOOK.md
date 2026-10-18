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
| p3 | Fable 5.1 Web Catcher | `hibi89/fable5.1_web_catcher` | 2026-10-19 KST | **Step1~4 전달 원본 자동/Mock 인수 기준 4/4 단계 충족 유지**. 신규 [PR #13](https://github.com/hibi89/fable5.1_web_catcher/pull/13) **공식 OpenAI SDK HTTP 계약 오프라인 검증** `httpx2.MockTransport`, 진짜 SDK가 실제 생성한 POST·JSON schema·store false·도구 미제공·개인정보 정제·401/429/500/refusal/incomplete를 7개 새 mock transport 테스트로 검증. **Windows 98/98 PASS** [39144159568](https://github.com/hibi89/fable5.1_web_catcher/actions/runs/39144159568); **실제 Chromium 23/23 PASS + 공개 smoke 4/4 PASS** [39144159553](https://github.com/hibi89/fable5.1_web_catcher/actions/runs/39144159553). 초기 Chromium 2회 22/23은 **Step3 CDP gzip 수신 길이 누락**에 따른 `compressed_decoded_unavailable` fail-closed; 테스트를 보안 정책에 맞게 고쳤으나 **CDP 성공률 자체는 개선 미달성**. PR #13 main 병합 `1339baf0a76e291a8f7fea2698b053cf9351c1a2`. 유료 OpenAI API **0회**, 실제 모델 보고서 품질/주입 내성 미검증. 사용자 Windows 실제 필터 차트/API 현장 실증도 미완. 상세 `docs/STEP4_OFFICIAL_SDK_OFFLINE_2026-10-19.md`; 최종 상용제품 전체 %는 스코프 미정으로 미산정. | `b59817a36bfa0d63cc071d664963e835abbe67cb` (HANDOFF HEAD; PR13 merge `1339baf0a76e291a8f7fea2698b053cf9351c1a2`) |
| p4 | Astra Web Catcher | `hibi89/astra_web_catcher` | 2026-10-19 KST | **Step 4-C 물리 필드명이 다른 합성 스키마 2종에서 공통 기능 수용 어댑터 재사용 완료.** `schema_reuse_adapter.py`+신규 40테스트+설계문서+상품/고객지원 가상 스키마·수용계약 4파일을 격리 브랜치에 커밋. 명시된 상품(`sku/display_name/family/popularity`)·티켓(`ticket_key/summary/lane/priority`) 필드를 canonical `id/title/category/score`로 정규화한 뒤 **같은 기존 FastAPI+SQLite 목록·검색·필터·상세 acceptance 엔진**으로 상품 6/6·티켓 7/7 기능 케이스 PASS. **전체 로컬 pytest 447/447 PASS**(기존 407+40), compileall PASS, 실제 Uvicorn 2개 앱 각각 필터/상세 200 및 없는 항목 404 확인. 신규 7 Git blobs 테스트본과 정확히 일치. 실 DB/API·URL 동작·범용 앱 생성·CRUD·고객 권한 **미검증/미구현**, preflight `blocked_pending_review`. `main`·기존 앱·데이터 무변경, GitHub Actions·차단 브라우저 미사용. **총 진척 약 43%**(기존 42%, +5%p 미만). **다음 ㄱ:** 가상의 명시 스키마에 안전한 추가 기능 연산(정렬·타입 필터) 지원 혹은 세 번째 이종 스키마 검증; 실데이터 연결 전 별도 승인. | `f5c9a21d9618b2783ce0c8326527e83d05077a7c` (feature HEAD; main `dc23ee604d02513c890615a3a98440c1ea8a5270`) |
| p5 | Astra PDF Redesigner | `hibi89/astra_pdf_redesigner` | 2026-10-19 01:19 KST | **STEP2 실물 `.localdoc.json` 독립 Chrome 프로필 A→B 백업·이식 CI PASS.** 기능 SHA `17f2e65e1873b4c75dc484cc7c6e11965a29f5ff`, [Actions `39144399956`](https://github.com/hibi89/astra_pdf_redesigner/actions/runs/39144399956) SUCCESS: Node16/16, TS/Vite 빌드, 기존 STEP1/2 Chrome 회귀, 프로필 A synthetic 원문·설정·PNG/WebP 실제 JSON 다운로드→완전히 독립된 B 프로필 `DOM.setFileInputFiles` 실제 파일 import, 기존 B 문서 보존·원문/디자인·PNG/WebP bytes 일치·doc/section/block/asset ID 신규 생성·reload 복원·A4 PDF에 이미지 2개 내장 PASS. **남음:** v1 cold migration write abort/marker 원자적 rollback 실험, Windows Chrome/Edge A4/한글/시각 수동 점검·최종 수용. STEP2 약 96%, 전체 7단계 단순 동등비중 약 28~29% (비공식 추정). **main STEP2 기능 미병합 HOLD, STEP3~7 미착수.** `README.md`/`STATUS.md`/`HANDOFF.md`/`docs/STEP2_FINAL_REQUIREMENTS_AUDIT_2026-10-19.md` 최신. 다음 `ㄱ`: 최초 migration write 실패 주입 및 복구 E2E. | `7bf3f9eea888ddb584248dcc343153139a0d33d4` (main docs HEAD; feature docs HEAD `b87eb8d81ae810831d870ade8a437d53546d5eb6`; verified code `17f2e65e1873b4c75dc484cc7c6e11965a29f5ff`) |
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
- 등록된 프로젝트: OHORA Trend Catcher (`p6`, `hibi89/ohora-trend-catcher`, 사용자 요청 수동 배정·마지막 확인 커밋 2026-10-16 11:46:12 KST), REA Studio (`p1`, `hibi89/web-rea-studio`), NAON2 Character Studio (`p2`, `hibi89/NAON2-Character-Studio`), Fable 5.1 Web Catcher (`p3`, `hibi89/fable5.1_web_catcher`, Step4 official SDK MockTransport 검증 +7, Windows98·Chromium23 PASS, 실제 유료 API 미실행), Astra Web Catcher (`p4`, `hibi89/astra_web_catcher`), Astra PDF Redesigner (`p5`, `hibi89/astra_pdf_redesigner`, STEP 2 feature 빌드·Chrome 스모크 PASS, main 미병합·추가 검수 대기)
- 현재 번호 배정: `p1`(REA Studio, 실제 작업 2026-10-18 15:28:10 KST), `p2`(NAON2, 실제 작업 2026-10-18 00:36:00 KST), `p3`(Fable 5.1 Web Catcher, 2026-10-19 Step4 official SDK offline wire +7 tests, Windows98·Chromium23·공개4 PASS, 실제 API 미실행·CDP 불안정은 fail-closed, HANDOFF b59817a3). `p4`(Astra Web Catcher), `p5`(Astra PDF Redesigner, 실제 검증 2026-10-18 21:39:37 KST·STEP 1 Chrome/CI PASS). `p0` 재실행 전 번호 유지. `p6` OHORA Trend Catcher 2026-10-19 KST 4-post×150-account slot code main 2c04b77d57a0549dbfb696b1bcf31ae1ef0383c7, GitHub Actions 28/28 PASS, real API 4-post limit pending.13.5 오프라인 20/20 PASS, main 4af906512e1146ed8c9394ae36c387f7f72b006d 재조회 기준. 실제 Meta/Windows/Actions는 미검증으로 사용자 PC 검증 대기. 등록부 갱신 자체로 활동 시간을 연장하지 않음.
