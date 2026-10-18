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
| p3 | Fable 5.1 Web Catcher | `hibi89/fable5.1_web_catcher` | 2026-10-18 23:49:00 KST | **Step 1 원본 7/7·Step 2 원본 9/9·Step 3 자동 인수 8/8, 사용자 Windows 구버전 Record 35클릭/중복0 PASS.** PR #3 헤더 없는 비압축 JSON 및 PR #4 SVG/CSS 기하 변화 감지 `main` 병합, CI Windows **65/65**, 실제 Chromium **21/21**, 공개 smoke **4/4 PASS**. **이번 ㄱ: 실제 사용자 데모 URL의 Ubuntu headed Chromium 읽기 전용 Record 12.397초, HTTP 200, SVG2/CSS bar1/API1, 종료 성공** [run 39137433372](https://github.com/hibi89/fable5.1_web_catcher/actions/runs/39137433372). **압축·Content-Length 미확인 API `compressed_size_unknown`으로 JSON 구조 0건**, 사용자 클릭0/차트변화0/API차트 연결0이라 현장 변경 감지·계보는 미검증. 임시 검증 PR #5 **closed unmerged**, main에 테스트용 코드 안 넣음. URL/응답값 원본/개인정보 업로드 없음. 근거 `docs/STEP3_LIVE_READONLY_2026-10-18.md`; 다음 작업 안전한 압축 응답 구조 분석 방식 검토/후속 Windows 수동 검증. | `2e2d0fa77b09b3732df91add6198a7e1788c1b14` (HANDOFF HEAD; PR #4 merge `67e72529be4d5e6a190d7c63fc0c840878301965`) |
| p4 | Astra Web Catcher | `hibi89/astra_web_catcher` | 2026-10-18 KST | **Step 4-C 로컬 검토 의견 JSON 내보내기/가져오기 1단위 완료.** 검토 패킷/기록 SHA-256 및 원본 ReviewPacket 대상 재검증, 의견 기록 불변·승인위조 차단. 로컬 UI 다운로드/파일 가져오기 버튼과 GET `/api/export/{id}`·POST `/api/import`, 임시 JSON 신규 기록 ID, 64KiB 제한·세션 토큰/Origin 검사 구현. **전체 로컬 pytest 237/237 PASS**(기존 213+신규 24), compileall 및 JS syntax PASS. 실제 Uvicorn localhost 저장→내보내기→가져오기→재조회 HTTP 모두 200, 13건 패킷에 3412바이트 bundle. SHA 자체는 인증/동의의 증거가 아님. 소스/테스트/문서 6개 Git blob SHA가 로컬 검증본과 동일; HANDOFF/STATUS 갱신. Chromium GUI 클릭 E2E는 기존 관리자 정책 차단으로 미검증. 실제 사용자의 의견·승인·DB/API 연결·사이트 기능 자동생성·배포 없음; `main`/기존 앱/DB 보존. **다음 ㄱ:** 승인된 새 원본 관찰 근거 확인이나 허가된 실제 브라우저에서 UI 수동 검증 1단위; 기존 관리자 차단 재시도 금지. | `1a27ac85daf66479529c641787fb7044c96eddbc` (feature HEAD; main `dc23ee604d02513c890615a3a98440c1ea8a5270`) |
| p5 | Astra PDF Redesigner | `hibi89/astra_pdf_redesigner` | 2026-10-18 23:38:59 KST | **STEP 1 main 기존 검증 유지, STEP 2 feature 통합 자동 검증 PASS**. 저장소 Public 전환 후 runner 복구, 이미지 블록 TS 오류·잘못된 PNG 테스트 CRC 수정. 기능 `caa0747a5b6967393e05b1b704fe0aa5b3f6aa24` 기준 Actions run `39136882566` SUCCESS: npm 단위 14/14, TS/Vite 빌드, Chrome STEP 1 회귀 A4 PDF 15p, STEP 2 IndexedDB/섹션/PNG/JSON/PDF 스모크. JPEG/WebP·멀티탭/저장 경쟁·Windows 검증 남음. **STEP 2 feature main 미병합**. `HANDOFF.md`/`STATUS.md` 최신 | `af2821654ac34d730e958f58409304e19b350ca6` (main 문서 HEAD; feature 문서 HEAD `cc2f48bf8ad98c33d645c4393d4d351bac904f9b`; 검증 코드 `caa0747a5b6967393e05b1b704fe0aa5b3f6aa24`) |
| p6 | OHORA Trend Catcher · RAW v2 Meta Batch 수집 | `hibi89/ohora-trend-catcher` | 2026-10-18 22:55 KST | **코드 구현·오프라인 검증 20/20 PASS / 실 Meta 수집 대기** · 294계정, 계정별 5개 단위·70분 최소 실행 간격, 7일 논리 창, 최신·이력 커서/누락 재개, 좋아요·댓글·팔로워 관측·미반환/NULL/오류 진단·실행별 JSON/CSV/manifest/검증기. 수동 70분 Windows 루프 포함, main 반영·재조회. 실제 Meta 호출·Windows 실행·Actions CI·누락 근본 원인 **미검증**. 사용자 PC 원본/인증 필요, 기존 데이터 보존·Vercel 미적용. `raw_v2/README.md`, STATUS/HANDOFF | `4af906512e1146ed8c9394ae36c387f7f72b006d` (main) |
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
- 등록된 프로젝트: OHORA Trend Catcher (`p6`, `hibi89/ohora-trend-catcher`, 사용자 요청 수동 배정·마지막 확인 커밋 2026-10-16 11:46:12 KST), REA Studio (`p1`, `hibi89/web-rea-studio`), NAON2 Character Studio (`p2`, `hibi89/NAON2-Character-Studio`), Fable 5.1 Web Catcher (`p3`, `hibi89/fable5.1_web_catcher`, Public, PR #4 Windows65·Chromium21 PASS; 실사이트 read-only HTTP200·SVG2/CSS1/API1·압축 JSON 구조 미수집), Astra Web Catcher (`p4`, `hibi89/astra_web_catcher`), Astra PDF Redesigner (`p5`, `hibi89/astra_pdf_redesigner`, STEP 2 feature 빌드·Chrome 스모크 PASS, main 미병합·추가 검수 대기)
- 현재 번호 배정: `p1`(REA Studio, 실제 작업 2026-10-18 15:28:10 KST), `p2`(NAON2, 실제 작업 2026-10-18 00:36:00 KST), `p3`(Fable 5.1 Web Catcher, 2026-10-18 23:46 KST, 실사이트 Record 읽기 전용 PASS·JSON compressed_size_unknown/차트변경 미검증, HANDOFF 2e2d0fa7). `p4`(Astra Web Catcher), `p5`(Astra PDF Redesigner, 실제 검증 2026-10-18 21:39:37 KST·STEP 1 Chrome/CI PASS). `p0` 재실행 전 번호 유지. `p6` OHORA Trend Catcher 2026-10-18 22:55 KST Python 3.13.5 오프라인 20/20 PASS, main 4af906512e1146ed8c9394ae36c387f7f72b006d 재조회 기준. 실제 Meta/Windows/Actions는 미검증으로 사용자 PC 검증 대기. 등록부 갱신 자체로 활동 시간을 연장하지 않음.
