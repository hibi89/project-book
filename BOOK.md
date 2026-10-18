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
| p3 | Fable 5.1 Web Catcher | `hibi89/fable5.1_web_catcher` | 2026-10-19 KST | **원본 Step 1(7/7)·2(9/9)·3(8/8) 자동 인수 PASS**. PR #3(headerless JSON), #4(SVG/CSS 변화), #7(압축 JSON decoded 크기) 이어 **PR #10 대용량 JSON의 32KiB 부분 필드 힌트** main 병합 `07fb7ed6fd0b7fb095eb1710e4432557d5cffae5`; Windows **70/70 PASS** run `39140626259`, 실제 headed Chromium **23/23 PASS**+보조 공개사이트 **4/4 PASS** run `39140626261`. **실제 사용자 대시보드 [39140868626](https://github.com/hibi89/fable5.1_web_catcher/actions/runs/39140868626) HTTP200/12.395초, 승인 API1/SVG2/CSS1, `decoded_too_large` 유지하면서 부분 구조 0→**1건** 확보**. 전체 JSON 본문은 읽지 않음, 부분 샘플은 chart↔API 후보로 승격하지 않음. 실험 PR #9/실사이트 검증 PR #11 **closed unmerged**. 수동 클릭0, 차트 변화·API 계보 사용자 현장 검증 미완. 전체 제품 최종 단계 분모 미확정으로 총 % 임의 추정 금지; 원본 Step1~3 자동 인수는 100% 완료. 근거 `docs/STEP3_PARTIAL_LARGE_JSON_PREFIX_2026-10-19.md`, STATUS/HANDOFF 최신. | `17160ffb56c80c74dca97aa85222495e8575ab07` (main README 문서 HEAD; 기능 PR #10 merge `07fb7ed6fd0b7fb095eb1710e4432557d5cffae5`) |
| p4 | Astra Web Catcher | `hibi89/astra_web_catcher` | 2026-10-19 KST | **Step 4-A 정적 화면/상호작용/계산식 증거 계층 게이트 1단위 완료.** `feature/observation-contract-20261018`: `evidence_claim_levels.py` + 신규 테스트 24개 + 문서. 등록된 합성 캡처 바이트 무결성/관찰 ID 재검사 후 각 관찰을 `visible_state`(스크린샷/DOM), `interaction_transition`(시연·수동 테스트+action+전후 공통값 변화), `calculation_formula`(반드시 별도 감사)로 분리. **349/349 전체 로컬 pytest PASS**(325+24), compileall PASS, 합성 사례 2관찰→6계층 검토 후보 생성. UI 표시 근거 ≠ 클릭·계산식 증명; 모든 인증/승인/DB/코드생성/배포 플래그 false. 신규 소스·테스트·문서의 Git blob 3개가 로컬 검증본과 일치. 실제 원본 캡처/GUI 브라우저·실DB/API·배포·GitHub Actions 없음, `main`/기존 앱/DB 불변. **전체 추정 약 38%, 유의미한 상승 없음.** **다음 ㄱ:** 허가된 수동 인터랙션 기록→기능 명세→독립 합성 수용 테스트 최소 연결. | `5a24215373e7598a2de1a3f974e09f60e5088c5b` (feature HEAD; main `dc23ee604d02513c890615a3a98440c1ea8a5270`) |
| p5 | Astra PDF Redesigner | `hibi89/astra_pdf_redesigner` | 2026-10-19 00:29:24 KST | **STEP 1 main 유지 / STEP 2 대형 세로 이미지·긴 캡션 Chrome A4 출력 검증 PASS.** 검증 기능 SHA `3173098c0df9d210cd8d762b28d09a36b5298f73`, Actions `39140653462` SUCCESS: Node 16/16, TS/Vite 빌드, Chrome 1200×2500 이미지 인쇄·짧은 캡션과 이미지 같은 페이지·190줄 긴 캡션 추가 페이지 생성/원문 보존·PDF 문자 A4 page bounds 검사, 기존 STEP1 PDF15p/STEP2 IndexedDB·JPEG/WebP·JSON·트랜잭션 회귀 PASS. **다음 1단위: 실제 2탭 Web Locks 보호 E2E; Windows/Edge 수동 인쇄·픽셀 단위 시각 검사 미검증. STEP2 약 92%, 전체 7단계 단순 동일 가중 약 28%(추정); main 기능 미병합, STEP3~7 미착수.** `STATUS.md`/`HANDOFF.md` 최신 | `3006d3c41bf89fc1019a63ba0ead3f971afb048f` (main docs HEAD; feature docs HEAD `4517a8927f22bda1f0cc8e68ea1aab8b39948c8b`; tested code `3173098c0df9d210cd8d762b28d09a36b5298f73`) |
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
- 등록된 프로젝트: OHORA Trend Catcher (`p6`, `hibi89/ohora-trend-catcher`, 사용자 요청 수동 배정·마지막 확인 커밋 2026-10-16 11:46:12 KST), REA Studio (`p1`, `hibi89/web-rea-studio`), NAON2 Character Studio (`p2`, `hibi89/NAON2-Character-Studio`), Fable 5.1 Web Catcher (`p3`, `hibi89/fable5.1_web_catcher`, PR #10 대용량 JSON 부분 구조 1건 실사이트 확인, Windows70·Chromium23 PASS), Astra Web Catcher (`p4`, `hibi89/astra_web_catcher`), Astra PDF Redesigner (`p5`, `hibi89/astra_pdf_redesigner`, STEP 2 feature 빌드·Chrome 스모크 PASS, main 미병합·추가 검수 대기)
- 현재 번호 배정: `p1`(REA Studio, 실제 작업 2026-10-18 15:28:10 KST), `p2`(NAON2, 실제 작업 2026-10-18 00:36:00 KST), `p3`(Fable 5.1 Web Catcher, 2026-10-19 PR #10 32KiB 부분 구조 힌트 완료, Windows70·Chromium23·공개4 PASS, 실사이트 부분 힌트 0→1, HANDOFF f439ae71). `p4`(Astra Web Catcher), `p5`(Astra PDF Redesigner, 실제 검증 2026-10-18 21:39:37 KST·STEP 1 Chrome/CI PASS). `p0` 재실행 전 번호 유지. `p6` OHORA Trend Catcher 2026-10-18 22:55 KST Python 3.13.5 오프라인 20/20 PASS, main 4af906512e1146ed8c9394ae36c387f7f72b006d 재조회 기준. 실제 Meta/Windows/Actions는 미검증으로 사용자 PC 검증 대기. 등록부 갱신 자체로 활동 시간을 연장하지 않음.
