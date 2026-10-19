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
| p4 | Astra Web Catcher | `hibi89/astra_web_catcher` | 2026-10-19 KST | **기존에 미검증이던 신규 capture_intake 통합 5건을 실제 원본 모듈로 실행하여 5/5 PASS 확인.** GitHub connector에서 필요한 원본 파일을 복원해 `git hash-object`로 16/16 원격 blob 일치 검증. 2개 전후 DOM 자료를 생성하는 `make_review_package`→기존 `CaptureIntakeRequest/register_captures/verify_captures`를 실제 호출해 2/2 `bytes_match_untrusted`, 같은 길이 파일 변조, 관찰 해시 불일치, 미등록 observation, 승인 위조 차단 시험 통과. **총 로컬 타깃 68/68 PASS, 0 FAIL/SKIP**(5 new+20 fake Selenium+18 schema+25 mapping), compileall 및 기본 Selenium dry-run CLI PASS. 이전 신규 5건 PENDING 상태 해소(로컬 실행 범위만). **완전한 저장소 checkout/739+ 전수 회귀/실제 Chrome 원본 클릭/고객 DB/API/Production 미검증, GitHub Actions 푸시 CI 결과는 별도로 미확인**(조회 가능한 commit status 없음, PR 전용 run search 제약). 소스·기능 코드·기존 `main` 불변, GitHub에는 `docs/PUBLIC_CAPTURE_INTAKE_CHAIN_20261019.md` 검증 보고와 STATUS/HANDOFF만 갱신. `GenerationContract=blocked_pending_review`; 전체 진행 추정 **~49% 유지**. **다음 ㄱ:** 로컬 운영자 소유 Chrome에서 허가된 공개 Selenium 테스트 1회 실행하고 실제 전후 증거 등록·독립 검토; 실행 전 성공 주장 금지. | `721338fe2faaf1be30a049b7f833d960cc4d11f8` (feature docs HEAD; main `dc23ee604d02513c890615a3a98440c1ea8a5270`; report `357afaef472ac6308ea992093faeaecb379ec664`) |
| p5 | Astra PDF Redesigner | `hibi89/astra_pdf_redesigner` | 2026-10-19 15:02:33 KST | **Windows Electron 설치형 + 네이티브 PDF 파일 저장 시험판 검증 완료.** 독립 [Draft PR #4](https://github.com/hibi89/astra_pdf_redesigner/pull/4) open/draft/unmerged, 안정 STEP1/2 main 기반, STEP3 PDF 업로드 기능은 **아직 설치판에 포함되지 않음**. 저장 버튼에서 Electron preload 최소 IPC → native Windows showSaveDialog → A4 printToPDF → 사용자 선택 경로 파일 저장(브라우저 기존 window.print fallback) 구현. [Windows CI #39206761720](https://github.com/hibi89/astra_pdf_redesigner/actions/runs/39206761720) **SUCCESS**, 코드 SHA `e11076cf77946416bc59bcaa88227c8265499ab3`: Node **19/19**, desktop 보안 **3/3**, Vite/TypeScript build, Windows 개발 Electron + 실제 패키징 EXE 로컬 IndexedDB/localStorage·secure app origin·preload IPC·실제 PDF **15,257 bytes** 디스크 생성/읽기 PASS. 새 unsigned NSIS `ASTRA-PDF-Redesigner-Setup-0.1.0-x64.exe` SHA256 `1FEB8C6801EB2870479955A5669B9405AC3117490A99954230AECB1470D3C84C` / [Actions Artifact #12165323804](https://github.com/hibi89/astra_pdf_redesigner/actions/runs/39206761720/artifacts/12165323804) ZIP 112,306,801 bytes·7일 보존. **실제 Windows 소비자 PC 설치·삭제, 저장 대화상자 수동 동작, 한글/A4/장문/이미지 출력 육안, 코드서명·SmartScreen/아이콘·JSON 프로필 이동 미검증; 정식 판매 금지.** PR4 보고서 docs-only SHA `d62f89b7ebc04eb0de3b6b2c44363c2e08996312`, main STATUS/HANDOFF docs HEAD `f008d7a8f25ed0e931d8e736ba5930af6bf7c54d`. 별도 STEP3 [Draft PR #3](https://github.com/hibi89/astra_pdf_redesigner/pull/3) open/unmerged, Node43/43 [#39203639740](https://github.com/hibi89/astra_pdf_redesigner/actions/runs/39203639740) PASS지만 실문서·Windows 수용 미완료. 7단계 전체 약38%는 비공식 추정 유지, 데스크톱은 별도 상품화 트랙. **다음:** Windows 실제 NSIS 설치·PDF 저장 대화상자/한글 문서 수동 인수 테스트 및 사용자 승인 후 PR3/PR4 통합 검토. **PR3·PR4 모두 main 기능 병합은 사용자 명시 승인 전 금지.** | `f008d7a8f25ed0e931d8e736ba5930af6bf7c54d` (main docs), `e11076cf77946416bc59bcaa88227c8265499ab3` (CI-verified Windows code), `d62f89b7ebc04eb0de3b6b2c44363c2e08996312` (PR4 docs-only), STEP3 `1ebbb7958c477c309e22e24fed7255658f56b58b` |
| p6 | OHORA Trend Catcher · RAW v2.1 daily-first 수집 및 계정별 현황표 | `hibi89/ohora-trend-catcher` | 2026-10-19 KST | 공식 294계정. 운영 우선순위: 매일 front 관측 → catchup → 여유 history; 4건/계정, 5계정/배치, 슬롯 최대150, Meta 사용량85%, 슬롯 종료+63분/시작+65분 쿨타임. 사용자 Windows 확인 2026-10-19: 5계정 History HTTP200, 첫 연속 슬롯 150계정 완료·신규580·누적1930, audit PASS는 실행 전 1330건 시점; 8계정 차단, 무인 운영 미승인, 365일 완전성 미검증. 독립 읽기 전용 `raw_v2/account_collection_status.py` 추가: 계정별 보유 게시일, 마지막 front, KST 오늘 조회, catchup/history 상태를 CSV/MD로 출력. 합성 테스트 추가, Windows 운영 DB 실검증 대기. 실행법 `docs/RAW_V2_ACCOUNT_COLLECTION_STATUS.md`. | `e730e02efdc743b28bd73525106a36c90b6d902a` |
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
