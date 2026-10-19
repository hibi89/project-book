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
| p4 | Astra Web Catcher | `hibi89/astra_web_catcher` | 2026-10-19 KST | **합성 소유자별 스키마 매핑 및 공유 SQLite 데이터 격리 E2E 성공.** 사용자 실제 DB 없이 합성 demo_alpha·demo_beta의 5컬럼(소유자+시계열 의미 역할4) 명시적 매핑, 공유 `:memory:` SQLite에서 세션 HttpOnly 쿠키 기반 `WHERE owner_id=?` 적용. A/B 데이터 혼합 없음; IDOR 다른 소유자 요청 404, 미인증/위조 세션 401, 헤더 사칭 무효, A 변경 시 B 불변, Chart/Table 전환 확인. GitHub Actions [run 39225637124](https://github.com/hibi89/astra_web_catcher/actions/runs/39225637124) **2/2 SUCCESS**, 전체 pytest **940 PASS / 2 기존 OWID ZIP SKIP / 0 FAIL**, 신규 소유자 격리 **33/33 PASS**, 실제 Chromium loopback HTTP PASS. 새 구현·테스트·CI·예제·보고서·README·STATUS·HANDOFF feature 커밋 완료; main 미병합, 실제 인증/DB/배포/생성 미승인. 진행률 약 **51% (주관적 추정)**. 다음 `ㄱ`: API 데이터 기반 소유자별 클라이언트 렌더링·응답 불일치 차단. | `b3166b67604381a9d2afd41667b65f9a9b103b37` |
| p5 | Astra PDF Redesigner | `hibi89/astra_pdf_redesigner` | 2026-10-19 17:39 KST | **Windows 실제 설치판에서 IndexedDB v1→v2 스키마 변경 마이그레이션 PASS**: 0.1.0(v1) NSIS 실제 설치→GUI 합성 문서·PNG/캡션 저장→코드/DB 스키마가 변경된 0.1.1(v2) 별도 빌드·동일 경로 덮어 설치→기존 활성 문서/PNG 유지, `migrationAudit` 신설, DB version2, 제거까지 [Windows Actions #39223771185](https://github.com/hibi89/astra_pdf_redesigner/actions/runs/39223771185) **SUCCESS**, 코드 SHA `0e5198341d4a708af20a3be3c481f058fecbfaf2`. 이전 버전번호만 변경한 설치 회귀 [#39216361190](https://github.com/hibi89/astra_pdf_redesigner/actions/runs/39216361190)와 구분. 합성 Chrome/Edge v1→v2·롤백 [#39222517425](https://github.com/hibi89/astra_pdf_redesigner/actions/runs/39222517425) **SUCCESS**. 독립 [STEP3 PR3](https://github.com/hibi89/astra_pdf_redesigner/pull/3), [Windows PR4](https://github.com/hibi89/astra_pdf_redesigner/pull/4), [IDB v2 PR5](https://github.com/hibi89/astra_pdf_redesigner/pull/5), [Windows통합 PR6](https://github.com/hibi89/astra_pdf_redesigner/pull/6) **전부 Draft/open/unmerged**, STEP4 미착수. Windows 10/11 일반 사용자 데이터·실고객 PDF·서명/SmartScreen·PDF 픽셀/글꼴 육안·전원중단 예외 미검증, unsigned 시험 설치판만 생성. 전체7단계 비공식 약38% 유지. 다음 `ㄱ`: 잔여 실패 복구/설치판 수용 검증 정리 또는 사용자 승인 대기; main 병합 금지. | `0e5198341d4a708af20a3be3c481f058fecbfaf2` (Windows schema CI); `e2f767d87f1657f6fdecdee0457b223f285823f0` (integration HANDOFF); `9fbc976e679530dafa5381af316d42b75400ecce` (Chrome/Edge IDB CI) |
| p6 | OHORA Trend Catcher · 294/294 합성 E2E + 원본 증거 변조 차단 | `hibi89/ohora-trend-catcher` | 2026-10-19 KST | 공식 294개 실제 계정 목록/단일 API 운영 collector는 변경하지 않음. 294개 가상 계정 전체 front 합성 배치+1계정 page2/page3/page4 Catch-up, front proofs 296 + catchup proof 1, RAW mirror 309 post/observation/media, 재시작 멱등·account294 누락 시 global catchup 차단까지 검증. 추가 3건: staging 원본 변조, 수집시각 증거 삭제·변경 시 fail-closed 및 신규 fixture 진입 차단. 85%/65min/15min cooldown/lease 테스트 유지. [3-API Actions 305/305 PASS](https://github.com/hibi89/ohora-trend-catcher/actions/runs/39239206405) (28 suites), [RAW v2 Actions 403/403 PASS](https://github.com/hibi89/ohora-trend-catcher/actions/runs/39239206392); source `ed74bd1`, HANDOFF/STATUS/설계/Codex 문서 `a27f87c`에 최신화. **실 Meta/실토큰/운영 collection.sqlite 0회**. 합성 294/294는 실제 294계정 완주 검증 아님. 실 Meta nested children 권한·실 A/B/C 독립 quota, 실 page4+ HTTP, 운영 RAW 통합 및 무인 scheduler는 미검증/미구현. 다음 단위: 합성 수집 실패 격리·증거 무결성 취약점 점검·부하 검증. 실호출·운영 DB는 별도 승인 전 금지. | `a27f87ce7f65241a9b5aa4bada94f744f9d67369` (main docs); `ed74bd158fcd9c4f7add2346fcb44c7a8d791a1a` (CI-success code) |
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
- 현재 번호 배정: `p1`(REA Studio, 실제 작업 2026-10-18 15:28:10 KST), `p2`(NAON2, 실제 작업 2026-10-18 00:36:00 KST), `p3`(Fable 5.1 Web Catcher, 2026-10-19 Step5 10/10 자동 인수, 전체 Step1~5 5/5 구현, Windows123·Chromium23·공개4 PASS, 실제 외부 배치/유료 API/Windows 현장 미검증, HANDOFF dd7132f2). `p4`(Astra Web Catcher), `p5`(Astra PDF Redesigner, 2026-10-19 16:11:22 KST·Windows STEP2 저장 실제 PDF A4 3p/5토큰/1이미지 Windows CI SUCCESS, PR4 Draft 미병합). `p0` 재실행 전 번호 유지. `p6` OHORA Trend Catcher 2026-10-19 KST 4-post×150-account slot code main 2c04b77d57a0549dbfb696b1bcf31ae1ef0383c7, GitHub Actions 28/28 PASS, real API 4-post limit pending.13.5 오프라인 20/20 PASS, main 4af906512e1146ed8c9394ae36c387f7f72b006d 재조회 기준. 실제 Meta/Windows/Actions는 미검증으로 사용자 PC 검증 대기. 등록부 갱신 자체로 활동 시간을 연장하지 않음.
