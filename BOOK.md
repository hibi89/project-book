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
| p3 | Fable 5.1 Web Catcher | `hibi89/fable5.1_web_catcher` | 2026-10-19 00:15 KST | **Step 1 7/7·Step 2 9/9·Step 3 8/8 자동 인수 유지.** PR #3 헤더 없는 비압축 JSON, PR #4 SVG/CSS 변화 마커, **PR #7 무길이 압축 JSON 디코딩 바이트 확인 후 안전 제한 파싱** 전부 main 병합(`4fe091451e3278aab8477abb1913144c9b3d00e5`). CI **Windows 67/67 PASS** `39139094290`, 실제 headed **Chromium 22/22 PASS**+공개4/4 `39139094270`. 압축 JSON 로컬 실험 171B→1,171B 구조 분석, 461B→400,015B 안전 제외 `39138406625`. **실제 사용자 대시보드 재검증** [39139325141](https://github.com/hibi89/fable5.1_web_catcher/actions/runs/39139325141) HTTP200/12.283초, SVG2+CSS1/API1, API 상태 `compressed_size_unknown`→`decoded_too_large`: **실제 압축 해제 후 데이터 128KiB 초과로 JSON 구조 0**(안전한 제외). 클릭0·차트 변경0/연결0이라 현장 lineage 미검증. 실험/실사이트 전용 PR #6/#8 closed unmerged. 한도 자동 상향 금지, 브라우저 압축 해제 메모리 절대상한 보장 아님. 상세 `docs/STEP3_COMPRESSED_JSON_DECODED_BOUND_2026-10-18.md`; 차기 대용량 JSON의 승인 구조 정보 확보 대안 또는 사용자 직접 Windows 1회 검증. | `36919a181b5b302fa548bef03d32d6bb6e3704ad` (README main HEAD; 기능 merge `4fe091451e3278aab8477abb1913144c9b3d00e5`) |
| p4 | Astra Web Catcher | `hibi89/astra_web_catcher` | 2026-10-19 KST | **Step 4-A 캡처 근거→기능 주장 수동 검토 연결 1단위 완료.** `feature/observation-contract-20261018`에 신규 `capture_claim_review.py`, 테스트 23개 및 문서 추가. 기존 `capture_intake` 검증을 선행해 등록된 임시 캡처의 바이트·출처 ObservationBundle SHA·ID 관계를 확인하고, 검토 항목별 스크린샷/DOM 연결을 생성. 의견 `more_evidence_needed`/가시적 일치·불일치(미인증 주장) 기록 지원; 증거 없는 일치 주장, UNKNOWN 동작 승격, 가짜 승인 필드 모두 차단. **로컬 전체 325/325 PASS**(302+23), compileall PASS; 합성 DOM 등록→검토 패킷 2항목→미확인 의견 1건 기록 시험. 신규 3개 소스/테스트/설계 Git blob SHA 일치 확인. 실제 신규 캡처·원본 동작·공식·GUI E2E 검증은 없음; DB/API·기존 서비스·`main` 변경 없음, 배포·Actions 미실행, 코드생성 승인 차단 유지. **전체 진행률 약 37~38% (유의미한 상승 아님)**. **다음 ㄱ:** 정적 화면 사실과 동적 동작·산식의 주장 수준을 구분하는 검토 게이트 또는 실사용자 허가 캡처 검증. | `5ace9999d71aed4fdc39e2dfc1ee2f646b726ae7` (feature HEAD; main `dc23ee604d02513c890615a3a98440c1ea8a5270`) |
| p5 | Astra PDF Redesigner | `hibi89/astra_pdf_redesigner` | 2026-10-19 00:20:19 KST | **STEP 1 main 유지 / STEP 2 이미지 교체 트랜잭션 강제 abort·롤백·복구 검증 PASS.** 검증 기능 `154ff8d98aa97da311362c1e11ea78bac9db77d9`, GitHub Actions `39139965821` SUCCESS: Node 16/16, TS/Vite 빌드, Chrome 실제 `assets.put()` 후 트랜잭션 abort→기존 이미지 3개 참조·바이트·DB 문서 보존·새로고침 복원, 재시도 정상 교체·불필요한 기존 asset 제거·고아 asset 없음. STEP1 A4 PDF 15p 및 STEP2 JPEG/WebP/PNG·저장복구 회귀 PASS. **STEP 2 자동 검증 기준 추정 약 90%, 전체 7단계 단순 동등 가중 약 27%**(의미 있는 5%p 상승은 아님). 장문 캡션·큰 이미지 페이지 경계, 멀티탭, Windows/Edge 미검증; main 기능 미병합·STEP3 미착수. `STATUS.md`/`HANDOFF.md` 최신. | `1bb9a65062ea54045d02075eaf05736e307776c7` (main docs HEAD; feature docs HEAD `88dd75da93ef8dbf0c5be078d9b9c745952a453f`; verified code `154ff8d98aa97da311362c1e11ea78bac9db77d9`) |
| p6 | OHORA Trend Catcher · RAW v2 Meta Batch 수집 | `hibi89/ohora-trend-catcher` | 2026-10-18 KST | **실 Meta 5/5계정·25게시물 수집·DB/해시 PASS**. 좋아요 6/25 필드 미반환, 모두 VIDEO/REELS; 원인 미확정. 기존 계정·게시물 커서/관측 이력 유지. 사용자가 정정한 수집 운영: **최대 150계정 × 5게시물 연속 → 끝난 시점부터 60분 쿨다운**; 시험 5계정 뒤 145계정 즉시 이어받기(최근 파일럿 자동 인계), 150 계정별 체크포인트, API 제한 시 안전 중단. 기존 무조건 70분 대기 오류 수정, Windows 로컬 150계정 운영 미검증. Linux synthetic 22/22 PASS, GitHub main 문서 최신화. 다음: `git pull`·Windows offline unittest, `--max-batches 30` 재개 후 사용량/좋아요 누락 확인. 원본/토큰 로컬, GitHub Actions 불필요(사용 가능). | `ff87def5c17b91ccbfb71d488483ff8d242c84be` (main HANDOFF HEAD; tested collector blob `6e89ea7796aeea06c2f49a8bef4d5cc7459d88f1`) |
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
- 등록된 프로젝트: OHORA Trend Catcher (`p6`, `hibi89/ohora-trend-catcher`, 사용자 요청 수동 배정·마지막 확인 커밋 2026-10-16 11:46:12 KST), REA Studio (`p1`, `hibi89/web-rea-studio`), NAON2 Character Studio (`p2`, `hibi89/NAON2-Character-Studio`), Fable 5.1 Web Catcher (`p3`, `hibi89/fable5.1_web_catcher`, PR #7 압축 JSON decoded 길이 128KiB 검사 병합, Windows67·Chromium22 PASS, 실사이트 JSON decoded_too_large), Astra Web Catcher (`p4`, `hibi89/astra_web_catcher`), Astra PDF Redesigner (`p5`, `hibi89/astra_pdf_redesigner`, STEP 2 feature 빌드·Chrome 스모크 PASS, main 미병합·추가 검수 대기)
- 현재 번호 배정: `p1`(REA Studio, 실제 작업 2026-10-18 15:28:10 KST), `p2`(NAON2, 실제 작업 2026-10-18 00:36:00 KST), `p3`(Fable 5.1 Web Catcher, 2026-10-19 00:14 KST PR #7 압축 JSON 안전 판정 완료, 67/22/4 PASS, 실사이트 API decoded_too_large, HANDOFF b790bed9). `p4`(Astra Web Catcher), `p5`(Astra PDF Redesigner, 실제 검증 2026-10-18 21:39:37 KST·STEP 1 Chrome/CI PASS). `p0` 재실행 전 번호 유지. `p6` OHORA Trend Catcher 2026-10-18 22:55 KST Python 3.13.5 오프라인 20/20 PASS, main 4af906512e1146ed8c9394ae36c387f7f72b006d 재조회 기준. 실제 Meta/Windows/Actions는 미검증으로 사용자 PC 검증 대기. 등록부 갱신 자체로 활동 시간을 연장하지 않음.
