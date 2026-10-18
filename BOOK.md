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
| p4 | Astra Web Catcher | `hibi89/astra_web_catcher` | 2026-10-18 KST | **Step 4-A/4-D 관찰 근거 파일 무결성 점검 1단위 완료**. 새 `evidence_integrity.py`에서 수동 파일 증거의 observation JSON ID/출처·SHA-256·파일 크기·형식·경로 검증, symlink/경로탈출·민감 텍스트 차단, snapshot/verify JSON CLI. **전체 로컬 pytest 270/270 PASS**(기존 237+신규 33), compileall 및 CLI PASS, 새 파일 4개 원격 Git blob 해시가 로컬과 일치. 기존 일본 네일 사례는 **2차 보관문서 1개 파일의 바이트만 일치**하며 실제 스크린샷·실사이트 동작·계산식 미검증. GitHub Actions·관리자 차단 GUI 브라우저 재시도 없음, 승인/DB/API/코드생성/배포 권한 항상 false. `GenerationContract` 여전히 blocked_pending_review. `main`·기존 앱/DB 불변. **다음 ㄱ:** 명시적으로 허가된 신규 캡처가 있으면 증거 링크/가시적 동작 검토, 없으면 수동 자료 인입 안전성 및 주장 수준 차단 강화. | `83bdd8befb47f042fde709ca5cc613ff95112d00` (feature HEAD; main `dc23ee604d02513c890615a3a98440c1ea8a5270`) |
| p5 | Astra PDF Redesigner | `hibi89/astra_pdf_redesigner` | 2026-10-19 00:10:27 KST | **STEP 1 main 유지 / STEP 2 IndexedDB 저장 실패·응급 백업·재시도 Chrome 검증 PASS.** 기능 `9339adb319a78192a0dda5ae437de248e9a056ca`, GitHub Actions `39139215112` SUCCESS: Node 16/16, TS/Vite 빌드, Chrome `QuotaExceededError` 문서 쓰기 실패 주입 → DB 원본 불변·메모리 편집 보존·페이지 이탈 경고·미저장 JSON 긴급 백업(이미지 포함)·수동 재시도·에러 배너 해제·새로고침 복구 PASS. STEP1 PDF 15p/STEP2 이미지·JSON 회귀 PASS. **STEP2 자동 검증 기준 약 85~90%; 전체 7단계 단순 동등 가중 약 26~27%(거친 추정치)**. 이미지 트랜잭션 실패/멀티탭/대형 이미지·캡션/Windows 미검증; main 기능 미병합, STEP3 미착수. `STATUS.md`, `HANDOFF.md`, feature 검증 문서 최신. | `afbfb7d60fcf80ca42c52a73288fd2905e07d682` (main docs HEAD; feature docs HEAD `7d22c7a3f7dbffe529e6fa823a4c4b6b51367a24`; verified code `9339adb319a78192a0dda5ae437de248e9a056ca`) |
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
- 등록된 프로젝트: OHORA Trend Catcher (`p6`, `hibi89/ohora-trend-catcher`, 사용자 요청 수동 배정·마지막 확인 커밋 2026-10-16 11:46:12 KST), REA Studio (`p1`, `hibi89/web-rea-studio`), NAON2 Character Studio (`p2`, `hibi89/NAON2-Character-Studio`), Fable 5.1 Web Catcher (`p3`, `hibi89/fable5.1_web_catcher`, Public, PR #4 Windows65·Chromium21 PASS; 실사이트 read-only HTTP200·SVG2/CSS1/API1·압축 JSON 구조 미수집), Astra Web Catcher (`p4`, `hibi89/astra_web_catcher`), Astra PDF Redesigner (`p5`, `hibi89/astra_pdf_redesigner`, STEP 2 feature 빌드·Chrome 스모크 PASS, main 미병합·추가 검수 대기)
- 현재 번호 배정: `p1`(REA Studio, 실제 작업 2026-10-18 15:28:10 KST), `p2`(NAON2, 실제 작업 2026-10-18 00:36:00 KST), `p3`(Fable 5.1 Web Catcher, 2026-10-18 23:46 KST, 실사이트 Record 읽기 전용 PASS·JSON compressed_size_unknown/차트변경 미검증, HANDOFF 2e2d0fa7). `p4`(Astra Web Catcher), `p5`(Astra PDF Redesigner, 실제 검증 2026-10-18 21:39:37 KST·STEP 1 Chrome/CI PASS). `p0` 재실행 전 번호 유지. `p6` OHORA Trend Catcher 2026-10-18 22:55 KST Python 3.13.5 오프라인 20/20 PASS, main 4af906512e1146ed8c9394ae36c387f7f72b006d 재조회 기준. 실제 Meta/Windows/Actions는 미검증으로 사용자 PC 검증 대기. 등록부 갱신 자체로 활동 시간을 연장하지 않음.
