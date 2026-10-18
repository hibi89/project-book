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
| p3 | Fable 5.1 Web Catcher | `hibi89/fable5.1_web_catcher` | 2026-10-18 20:32:23 KST | **Step 1 원본 7/7, Step 2 원본 9/9 CLI MVP 완료**. 첫 실사이트(젤네일 인사이트 대시보드, #v-dash) 실제 Chromium 분석: HTTP 200, XHR 2, 작은 아이콘 SVG 오탐 다수 제거 및 반복 CSS 막대 1개 탐지, 차트 후보 **14~15 → 3(큰 SVG 2 + CSS 1)**. SPA hash 브라우저 경로 보존·출력 비노출 수정. Windows 3.11 **57/57 PASS** run `39123343492`, Ubuntu 실제 Chromium **12/12 PASS** run `39123322129`, 사용자 URL 구조 진단 PASS run `39123343463`, 기능 SHA `b7c707386034a14c44820709b4a13388dfcf7e7e`. 실제 차트↔API lineage 및 모든 CSS 시각화의 탐지율은 미검증. `docs/DASHBOARD_LIVE_ACCURACY_2026-10-18.md`·HANDOFF·STATUS 최신. 사용자 Windows는 git pull 후 재검증 필요. 배포 없음 | `df51bf30f7ab8ca22a996b12c5ede5e65445478e` (문서 HEAD; 검증 코드 `b7c707386034a14c44820709b4a13388dfcf7e7e`) |
| p4 | Astra Web Catcher | `hibi89/astra_web_catcher` | 2026-10-18 20:55:33 KST | **Step 2 관찰 증거 계약 v1 / Step 4-A 기반 1단위 완료.** `feature/observation-contract-20261018`에 Pydantic JSON 계약·CLI validate/schema·합성 예제·검증 테스트·설계 문서 추가, **로컬 19/19 PASS**, CLI/JSON Schema/compileall PASS, GitHub blob 해시·브랜치 SHA 재조회 확인. `main` 기존 쇼핑/채용·연구 네일 대시보드·실험 CSV/DB 미변경, Production 미적용. **다음 ㄱ:** 기존 일본 네일 브랜드 필터 관찰 1건을 근거/미확인 구분해 계약 JSON으로 변환·테스트. 기능 명세 자동화·DB/API 매핑·생성 파이프라인 미구현. | `85e21f3960a1adf6c87867840f93525a75e65b78` (feature HEAD; main `dc23ee604d02513c890615a3a98440c1ea8a5270`) |
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
- 등록된 프로젝트: OHORA Trend Catcher (`p6`, `hibi89/ohora-trend-catcher`, 사용자 요청 수동 배정·마지막 확인 커밋 2026-10-16 11:46:12 KST), REA Studio (`p1`, `hibi89/web-rea-studio`), NAON2 Character Studio (`p2`, `hibi89/NAON2-Character-Studio`), Fable 5.1 Web Catcher (`p3`, `hibi89/fable5.1_web_catcher`, Step 1 7/7·Step 2 9/9 완료·첫 실사이트 CSS 차트 개선, Windows 57 PASS·Chromium 12 PASS), Astra Web Catcher (`p4`, `hibi89/astra_web_catcher`), Astra PDF Redesigner (`p5`, `hibi89/astra_pdf_redesigner`, 빈 저장소·첫 커밋 전)
- 현재 번호 배정: `p1`(REA Studio, 실제 작업 2026-10-18 15:28:10 KST), `p2`(NAON2, 실제 작업 2026-10-18 00:36:00 KST), `p3`(Fable 5.1 Web Catcher, Step 1 7/7·Step 2 9/9 완료·실사이트 정확도 1차 개선, 문서 HEAD 2026-10-18 20:32:23 KST, Windows 57/57·Chromium 12/12 PASS). `p4`(Astra Web Catcher), `p5`(Astra PDF Redesigner, 실제 작업 시각·커밋 없음). `p0` 재실행 전 번호 유지. 사용자 요청으로 `p6` OHORA Trend Catcher 수동 등록(최근 3시간 외·재배정 가능). 등록부 갱신 자체로 활동 시간을 연장하지 않음.
