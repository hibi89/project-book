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
| p3 | Fable 5.1 Web Catcher | `hibi89/fable5.1_web_catcher` | 2026-10-18 21:22:44 KST | **Step 1 원본 7/7, Step 2 원본 9/9, Step 3 headed Record CLI 자동 인수검사 8/8 PASS**. --record(기본 max-duration900초), Enter/Ctrl+C/시간·창 종료, 승인 origin·새 탭/문서 분리, click/change 마커, Step2 네트워크/차트/번들 재사용·점진 JSON 요약·마스킹. PR #1 main 병합. Windows **60/60 PASS** run `39126644441`, 실제 headed Chromium **16/16 PASS** run `39126644405`, 공개 홈페이지 선택 smoke **4/4 PASS**. 검증 소스 `80f71d2b...`, main merge `e28ea7f1...`. 사용자 Windows 실제 로그인→필터→Enter는 **미검증**, 배포 없음. `docs/STEP3_FINAL_ACCEPTANCE.md`·HANDOFF·STATUS 최신. | `20ace48dc0779120f8118b745f41e67f1d8db8ae` (문서 HEAD; 기능 병합 `e28ea7f1f5a91d2f7a69160377558c6bc72e836d`) |
| p4 | Astra Web Catcher | `hibi89/astra_web_catcher` | 2026-10-18 21:33:38 KST | **Step 4-B 사용자 소유 DB/API 스키마 매핑 진단 계약 1단위 완료.** `feature/observation-contract-20261018`: 명시 매핑·구조 충돌·누락·타입·nullability 비교, 근거 SHA·미확인/승인 게이트 출력. 실제 DB/API 연결·수정·자동 필드 추정 없음. **로컬 71/71 PASS**(기존 46+신규 25), compileall 및 CLI JSON PASS; 합성 데이터 10건(구조일치 미승인 3/미매핑 4/리소스누락 1/필드누락 1/타입충돌 1). GitHub 새 파일 5개·HANDOFF/STATUS 원격 blob 해시 일치 확인, 브랜치 HEAD 및 GitHub Author/Committer `hibi89` 확인. `main`·기존 앱·DB 변경 없음, Production 미적용. **다음 ㄱ:** 별도 독립 코드 생성 계약 및 승인/안전 게이트 설계·테스트 1단위, 실서비스 변경은 승인 대기. | `ec59c3830ef69cc78d522e24d178d0f274e407e0` (feature HEAD; main `dc23ee604d02513c890615a3a98440c1ea8a5270`) |
| p5 | Astra PDF Redesigner | `hibi89/astra_pdf_redesigner` | 미확인 (저장소 초기화 전) | 등록 · 비공개 빈 저장소 · 초기 작업 대기 · `HANDOFF.md`/`STATUS.md` 없음 | — (커밋 없음) |
| p6 | OHORA Trend Catcher · Meta Batch API 수집 | `hibi89/ohora-trend-catcher` | 2026-10-16 11:46:12 KST (최신 확인 커밋 시각) | **사용자 요청 수동 배정** · 294계정 × 최근 5개 Batch 수집 및 2앱 150/144 분리 설계 · 90분 이력 백필 코드 작성, 실제 2앱 구동·Windows 테스트 미검증 · 2번째 앱 토큰 만료로 차단 · 마지막 확인 작업이 3시간 초과여서 다음 `p0`의 활성 판정 대상은 아님 | `71fa917aba523d9d95f074f5607a6433128b13bd` |
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
- 등록된 프로젝트: OHORA Trend Catcher (`p6`, `hibi89/ohora-trend-catcher`, 사용자 요청 수동 배정·마지막 확인 커밋 2026-10-16 11:46:12 KST), REA Studio (`p1`, `hibi89/web-rea-studio`), NAON2 Character Studio (`p2`, `hibi89/NAON2-Character-Studio`), Fable 5.1 Web Catcher (`p3`, `hibi89/fable5.1_web_catcher`, Step 1 7/7·Step 2 9/9·Step 3 자동검증 8/8, Windows 60·Chromium 16 PASS), Astra Web Catcher (`p4`, `hibi89/astra_web_catcher`), Astra PDF Redesigner (`p5`, `hibi89/astra_pdf_redesigner`, 빈 저장소·첫 커밋 전)
- 현재 번호 배정: `p1`(REA Studio, 실제 작업 2026-10-18 15:28:10 KST), `p2`(NAON2, 실제 작업 2026-10-18 00:36:00 KST), `p3`(Fable 5.1 Web Catcher, Step 3 수동 Record CI 자동검증 완료, 2026-10-18 21:22:44 KST, Windows 60/60·Chromium 16/16·선택 URL 4/4 PASS, Windows 사람 직접 로그인 미검증, 문서 HEAD `20ace48d`). `p4`(Astra Web Catcher), `p5`(Astra PDF Redesigner, 실제 작업 시각·커밋 없음). `p0` 재실행 전 번호 유지. 사용자 요청으로 `p6` OHORA Trend Catcher 수동 등록(최근 3시간 외·재배정 가능). 등록부 갱신 자체로 활동 시간을 연장하지 않음.
