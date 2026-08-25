<img width="9119" height="5015" alt="main2" src="https://github.com/user-attachments/assets/e53d2aee-52fb-43e7-af41-ee162b232ea0" />

<div align="center">

# 🏕️ [나갔음 청년](https://www.nagasseum.com)

### *MZ세대의 주거 독립을 위한 자산 형성 & 목표 관리 플랫폼*

<sub>KB IT's Your Life 7기 - 25반 1팀 최종 프로젝트</sub>

</div>


---

## 📖 목차

1. [프로젝트 개요 및 소개](#1-프로젝트-개요-및-소개)
2. [팀원 소개](#-팀원-소개)
3. [개발 기간](#2-개발-기간)
3. [개발 환경 및 기술 스택](#3-개발-환경-및-기술-스택)
4. [협업 과정](#4-협업-과정)
5. [커밋 컨벤션](#5-커밋-컨벤션)
6. [이슈 컨벤션](#6-이슈-컨벤션)
7. [PR 컨벤션](#7-pr-컨벤션)
8. [ERD](#8-erd)
9. [시스템 아키텍처](#9-시스템-아키텍처)
10. [서비스 기능](#10-서비스-기능)
11. [이슈 및 트러블슈팅](#11-이슈-및-트러블슈팅)

---

## 1. 프로젝트 개요 및 소개

청년에게 독립은 단순히 집을 구하는 일이 아니라, **“내 자산으로 언제쯤 이 집을 감당할 수 있을까”를 판단해야 하는 금융 의사결정**에 가깝습니다. 하지만 이를 스스로 판단하려면 현재 자산, 소득, 매달 저축 가능액에 더해 **목표 시점의 집값**까지 직접 계산해야 하고, 집값은 오늘과 목표 시점이 다르기 때문에 지금 시세만 보고 판단하면 빗나가기 쉽습니다.

**「나갔음 청년」은 이 복잡한 계산을 대신해 주는 서비스입니다.** 사용자의 금융 자산을 연동해 현재 상황을 파악하고, 국토부 실거래가 데이터로 목표 시점의 집값을 예측한 뒤, *“목표 시점에 이 조건의 집을 마련할 확률은 몇 %”* 라는 형태로 진단합니다.

### 핵심 가치

- 🎯 **정직한 진단**: 가능/불가능이 아니라 몬테카를로 시뮬레이션 기반 달성 확률과 가격 분포로 답합니다.
- 🔗 **실제 데이터 연동**: CODEF로 사용자 자산을, 국토부 API로 실거래가를 실시간 반영합니다.
- 🧭 **실행 가능한 계획**: 같은 목표를 이루는 여러 플랜을 제안하고, 저축 진행을 추적합니다.
- 🌱 **동기 부여 UX**: 캐릭터, 진행률, 또래 비교로 자립 준비를 게임처럼 이어가게 합니다.

---

## 👥 팀원 소개

<table>
  <tr>
    <td align="center"><img src="https://github.com/slowsteadyman.png?size=120" width="120"><br><b>최규진</b></td>
    <td align="center"><img src="https://github.com/yerimming.png?size=120" width="120"><br><b>김예림</b></td>
    <td align="center"><img src="https://github.com/hyobin13.png?size=120" width="120"><br><b>전효빈</b></td>
    <td align="center"><img src="https://github.com/jinwoojwa.png?size=120" width="120"><br><b>좌진우</b></td>
    <td align="center"><img src="https://github.com/Rockernun.png?size=120" width="120"><br><b>박병욱</b></td>
  </tr>
  <tr>
    <td align="center"><a href="https://github.com/slowsteadyman">slowsteadyman</a></td>
    <td align="center"><a href="https://github.com/yerimming">yerimming</a></td>
    <td align="center"><a href="https://github.com/hyobin13">Hyobin</a></td>
    <td align="center"><a href="https://github.com/jinwoojwa">Jinwoo</a></td>
    <td align="center"><a href="https://github.com/Rockernun">Rockernun</a></td>
  </tr>
  <tr>
    <td align="center"><b>Team Lead</b>, PM, Frontend/Backend</td>
    <td align="center">Frontend/Backend, UI/UX</td>
    <td align="center">Frontend/Backend, UI/UX</td>
    <td align="center">Frontend/Backend, Git Lead(Frontend)</td>
    <td align="center">Backend, CI/CD, Infra, Git Lead(Backend)</td>
  </tr>
</table>

---

## 2. 개발 기간

| 구분 | 기간 |
| --- | --- |
| 기획 및 설계 | 2026.07.09 ~ 2026.07.22|
| 개발 (구현) | 2026.07.23 ~ 2026.08.24 |
| 배포 및 시연 | 2026.08.26 |


---

## 3. 개발 환경 및 기술 스택

### Frontend

| 구분 | 기술 |
| --- | --- |
| Framework | Vue 3, Vite |
| Runtime | Node.js 20.19+ / 22.12+ |
| 품질 도구 | ESLint, Prettier, Husky + lint-staged |
| 테스트 / 문서 | Vitest, Storybook, MSW (Mock Service Worker) |
| 배포 | Vercel |

### Backend

| 구분 | 기술 |
| --- | --- |
| Language | Java 17 |
| Framework | Spring Framework 5.3.39 |
| SQL Mapper | MyBatis 3.5.16 |
| DB / Cache | MySQL 8.4.9, Redis 7.1 |
| Build / WAS | Maven, Apache Tomcat 9.0.118 |
| 외부 연동 | CODEF(자산), 국토교통부 실거래가 API, 카카오 로그인 API |

### Infra & DevOps

| 구분 | 기술 |
| --- | --- |
| Cloud | AWS (VPC, EC2, RDS, ElastiCache, ALB, NAT Instance, SSM) |
| 컨테이너 | Docker, Docker Compose |
| CI/CD | GitHub Actions → Docker Hub → AWS SSM 배포 |
| 형상관리 | Git, GitHub (Organization) |

---

## 4. 협업 과정

브랜치 기반 워크플로로 협업했습니다. **이슈로 작업을 정의**하고, **브랜치를 파서 구현**한 뒤, **PR로 리뷰**를 거쳐 `develop`에 머지하는 흐름입니다.

```
1. Issue 생성
2. 브랜치 생성
3. 기능 구현
4. Pull Request 작성
5. 코드 리뷰 후 Merge (develop)
6. CI/CD 자동 배포
```

### 브랜치 전략

| 브랜치 | 용도 |
| --- | --- |
| `main` | 배포/릴리스 기준 브랜치 |
| `develop` | 개발 통합 브랜치 (기본 브랜치) |
| `feat/설명` | 기능 개발 브랜치 |
| `fix/설명` | 버그 수정 브랜치 |
| `refactor/설명` | 리팩터링 브랜치 |
| `docs/설명` | 문서 수정 브랜치 |

- 작업은 항상 **이슈 → 브랜치** 순서로 시작합니다.
- PR은 **최소 1인 이상의 리뷰 승인** 후 머지합니다.
- 프론트엔드는 `Husky + lint-staged`로 커밋 시 자동 린트, 포맷을 강제합니다.


---

## 5. 커밋 컨벤션

**Conventional Commits** 형식을 따릅니다.

```
<type>: <subject>

예)
feat: 자산 동기화 비동기 처리 구현 
fix: 몬테카를로 Itô 보정 이중 적용 수정
docs: README 시스템 아키텍처 섹션 추가
```

| type | 설명 |
| --- | --- |
| `feat` | 새로운 기능 추가 |
| `fix` | 버그 수정 |
| `refactor` | 기능 변화 없는 코드 구조 개선 |
| `docs` | 문서 수정 |
| `test` | 테스트 코드 추가 및 수정 |
| `chore` | 빌드, 설정, 패키지 등 기타 작업 |
| `style` | 포맷, 세미콜론 등 코드 스타일 (동작 변화 없음) |

**규칙**
- 제목은 **명령형 or 현재형**으로, 마침표 없이 작성합니다.
- 하나의 커밋은 **하나의 논리적 변경**만 담습니다.

---

## 6. 이슈 컨벤션

작업은 이슈로 먼저 정의합니다. 제목에 라벨 성격을 접두어로 붙여 한눈에 구분되게 했습니다.

```
[FEAT] 목표 달성 확률 시뮬레이션 API 구현
[FIX]  전세/월세 평당가 계산 시 월세 미반영 버그
[DOCS] ERD 문서화
```

**이슈 본문 템플릿**

```markdown
## 📌 작업 내용
- 무엇을 왜 하는지 간단히

## ✅ 체크리스트
- [ ] 세부 작업 1
- [ ] 세부 작업 2

## 📎 참고
- 관련 문서/링크/스크린샷
```

| 라벨 | 설명 |
| --- | --- |
| `feat` | 기능 개발 |
| `fix` | 버그 수정 |
| `refactor` | 리팩터링 |
| `docs` | 문서 |
| `infra` | 인프라 & 배포 |
| `question` | 논의 필요 |

---

## 7. PR 컨벤션

PR 제목은 커밋 컨벤션과 동일한 형식을 따르고, 본문에 **변경 요약, 확인 방법, 관련 이슈**를 남깁니다.

```
feat: 자산 동기화 비동기 전환
```

**PR 본문 템플릿**

```markdown
## #️⃣연관된 이슈

> ex) #이슈번호

## 📝작업 내용

> 이번 PR에서 작업한 내용을 상세하게 설명해주세요(이미지 첨부 가능)

### 스크린샷 (선택)

## 💬리뷰 요구사항(선택)

> 리뷰어가 특별히 봐주었으면 하는 부분이 있다면 작성해주세요
>
> ex) 메서드 XXX의 이름을 더 잘 짓고 싶은데 혹시 좋은 명칭이 있을까요?
```

**규칙**
- PR은 **작게, 자주** 올려 리뷰 부담을 줄입니다.
- **최소 1인 승인** 후 `develop`에 머지합니다.
- 머지 후에는 브랜치 삭제가 원칙입니다.

---

## 8. ERD

<img width="3910" height="2462" alt="kb-final-project-erd (18)" src="https://github.com/user-attachments/assets/bac8412a-4173-4090-8232-411ac6b43a87" />

---

## 9. 시스템 아키텍처

<img width="3611" height="2357" alt="architecture" src="https://github.com/user-attachments/assets/3f0fb77f-bdc3-4381-8d07-35e4b36dead9" />



- **3-Tier 네트워크 격리**: VPC(`10.0.0.0/16`)를 Public / App(Private) / Data(Private) 세 계층으로 분리하고, App과 Data 계층에는 **공인 IP를 부여하지 않아** 인터넷에서 직접 접근할 수 없게 했습니다.
- **NAT Instance (아웃바운드 전용)**: 외부 API 호출은 나가되 인바운드는 차단하고 아웃바운드가 적은 특성에 맞춰 NAT Gateway 대신 **NAT Instance로 비용을 절감**했습니다.
- **Multi-AZ 이중화**: 2개 가용영역에 걸쳐 배치, RDS Multi-AZ로 장애 시 자동 승격되도록 처리했습니다.
- **관리 접근은 SSM**: SSH(22)를 열지 않고 AWS SSM Session Manager로 접속하도록 했습니다 *(CIS AWS Foundations Benchmark 네트워킹 권고 준수)*
- **CI/CD 자동화**: `develop` push 시 GitHub Actions가 빌드 → Docker Hub push → SSM으로 API와 Batch 서버에 배포 → 헬스체크

---

## 10. 서비스 기능

사용자의 **자립 여정**을 따라 기능을 소개합니다. 온보딩부터 목표 달성 추적까지 하나의 흐름으로 이어집니다.

### ① 온보딩: 로그인부터 자산 연동까지

카카오 간편 로그인 후 이름과 생년월일을 등록하고, **CODEF로 은행, 증권 자산을 연동**합니다. 예적금, 투자, 대출이 한 번에 모여 현재 자산이 집계됩니다.

<table>
  <tr>
    <td align="center"><img width="1170" height="2532" alt="1 login" src="https://github.com/user-attachments/assets/b8d0e9e2-3ddd-4729-84e6-184ffed1f9ff" />
<br><sub>로그인</sub></td>
    <td align="center"><img width="1170" height="2532" alt="2-1 signup-nickname" src="https://github.com/user-attachments/assets/d5cf24f8-bf45-4af1-a34f-e79171c68e51" />
<br><sub>회원가입</sub></td>
    <td align="center"><img width="1170" height="2532" alt="localhost_5173_callback_code=WhP4aqtPtOtn0oLXgdDLEzywrmzG1o8F90VFVPmrxmWdnfwiVzqW9AAAAAQKDRmQAAABoDa0mdXE017PSiBv1Q(demo)" src="https://github.com/user-attachments/assets/fa784f5a-0c3d-4663-9c0e-c572f82cd3f8" />
<br><sub>자산 연동</sub></td>
    <td align="center"><img width="1170" height="2532" alt="3 home-nogoal" src="https://github.com/user-attachments/assets/1319c2d7-4b25-4848-8f26-64aa7616687a" />
<br><sub>홈, 연동된 자산 확인</sub></td>
    <td align="center"><img width="1170" height="2532" alt="localhost_5173_home(demo)" src="https://github.com/user-attachments/assets/a04aa923-cf0d-491c-95b1-495de4208151" />

<br><sub>자산 상세</sub></td>
  </tr>
</table>

### ② 목표 설정: 7단계 대화형 입력

지역, 주거형태, 거래유형, 평수, 보증금, 목표 시점, 월 저축액을 **대화형으로** 입력합니다. 모르는 조건은 건너뛸 수 있고, 모든 예산 산정은 **국토부 실거래가**에 기반합니다.

<table>
  <tr>
    <td align="center"><img width="1170" height="3741" alt="4-1 diagnosis-region" src="https://github.com/user-attachments/assets/209a518c-3dc7-4400-a07f-4faae69159ef" />
<br><sub>지역 선택</sub></td>
    <td align="center"><img width="1170" height="2532" alt="4-5 diagnosis-deposit" src="https://github.com/user-attachments/assets/ba2a11d6-af8d-4deb-a689-abb1740f1060" />
<br><sub>보증금 범위 선택</sub></td>
    <td align="center"><img width="1170" height="2532" alt="4-7 diagnosis-date" src="https://github.com/user-attachments/assets/6d40ebf8-37eb-4507-9331-8a0851d52838" />
<br><sub>목표 시점 선택</sub></td>
  </tr>
</table>

### ③ 추천 계획: 같은 목표, 다른 방법

입력한 조건을 바탕으로 **여러 개의 실현 플랜**을 제시합니다. “현재 준비 상황 반영”, “목표 시점 조정”, “월 저축액 조정” 등 서로 다른 전략을 비교하고, 상세 화면에서 목표 시점의 예상 시세까지 확인합니다.

<table>
  <tr>
    <td align="center"><img width="1170" height="4356" alt="5-1 recommendation" src="https://github.com/user-attachments/assets/ac0c5d6d-72e6-428e-82f5-c31f3ccb82b7" />
<br><sub>진단, 추천 계획</sub></td>
    <td align="center"><img width="1170" height="3444" alt="5-2 recommendation-preference-savingfix" src="https://github.com/user-attachments/assets/bf0597a8-1abf-488d-b0cf-1ce5bdf1b1c4" />
<br><sub>대안 비교, 상세</sub></td>
    <td align="center"><img width="1170" height="2964" alt="5-4 recommendation-realistic" src="https://github.com/user-attachments/assets/9df3aee1-0d37-441c-931b-74628b12d9df" />
<br><sub>대안 비교, 상세</sub></td>
  </tr>
</table>

### ④ 목표 추적: 진행률과 저축 관리

목표를 확정하면 홈에서 **달성 진행률**을 캐릭터와 함께 보여줍니다. 매달 저축을 기록하고, **최근 실거래가 변동을 목표에 다시 반영**하며, 필요하면 월 저축 계획을 수정합니다.

<table>
  <tr>
    <td align="center"><img width="1170" height="3153" alt="6-1 home" src="https://github.com/user-attachments/assets/b60bfd99-d6b8-49b0-87b9-1085672fbe97" />
<br><sub>목표 홈, 진행률</sub></td>
    <td align="center"><img width="1170" height="2532" alt="6-2 monthlySaving-input" src="https://github.com/user-attachments/assets/0f233378-18ab-400d-9396-e7eb18d9e4b7" />
<br><sub>실제 월 저축액 입력</sub></td>
    <td align="center"><img width="1170" height="3870" alt="7-1 goal" src="https://github.com/user-attachments/assets/0567667b-ec4d-4bcb-802b-692aed280330" />
<br><sub>목표 상세, 실거래 반영</sub></td>
    <td align="center"><img width="1170" height="2532" alt="7-2 goal-monthlySaving-edit" src="https://github.com/user-attachments/assets/15261192-996e-439a-94ba-c5dfb8aa2c2f" />
<br><sub>저축 계획 수정</sub></td>
  </tr>
</table>

### ⑤ 또래 비교 & 마이페이지

비슷한 조건의 **또래 파티원들과 익명으로 자산을 비교**해 동기를 얻고, 마이페이지에서 캐릭터, 프로필, 알림, 테마를 관리합니다.

<table>
  <tr>
    <td align="center"><img width="1170" height="3726" alt="8 compare1" src="https://github.com/user-attachments/assets/3eeb4424-7231-49d1-8cd8-1e6decc90392" />
<br><sub>또래 비교</sub></td>
<td align="center"><img width="1170" height="3795" alt="8 compare2" src="https://github.com/user-attachments/assets/46c3bc83-6653-45c5-b971-f1c281d528ee" />
<br><sub>또래 비교</sub></td>
    <td align="center"><img width="1170" height="3231" alt="9-1 mypage" src="https://github.com/user-attachments/assets/2d748f38-4e47-40e9-a4a8-9585e8ebbfbd" />
<br><sub>마이페이지</sub></td>
  </tr>
</table>

---

## 11. 이슈 및 트러블슈팅

프로젝트에서 **“동작하지만 틀린”** 문제와 **증상과 원인의 거리가 먼** 문제들을 근본 원인까지 파고들어 해결했습니다.

### 🔴 몬테카를로 시뮬레이션의 Itô 보정 이중 적용

- **문제**: 미래 집값 시뮬레이션 결과가 이론 기댓값보다 낮게 나왔습니다. 테스트로는 잡히지 않는 비즈니스 로직이어서 발견이 어려웠습니다.
- **원인**: `ln(price)~t` 회귀 기울기는 로그-드리프트(μ−σ²/2)인데, 이를 산술 드리프트 μ로 오인해 엔진에서 σ²/2를 한 번 더 빼고 있었습니다.
- **해결**: 추정 단계에서 `annualDrift = logDrift + σ²/2`로 변환해 엔진의 표준 GBM 계약을 지켰습니다. **(P50가 이론 대비 −5.76% → +0.07%로 정합)**

### 🔴 자산 동기화 25.87초 → 0.029초 (동기 → 비동기 전환)

- **문제**: CODEF로 다계좌 동기화 시 장시간 요청 스레드가 점유되어 스레드 고갈 및 UI 블로킹 위험이 있었습니다.
- **원인/해결**: REST Long-Running Task 패턴(`202 Accepted` + 폴링)으로 전환했습니다. `@Async` 자기 호출이 프록시를 안 타는 문제를 빈 분리로 해결하고, 서버 2대 환경을 위해 작업 상태를 Redis에 공유하도록 했습니다.


---

<div align="center">

### 🏕️ 나갔음 청년

*“처음에는 독립처럼 멀어 보이던 목표가, 어느새 가까워지는 경험”*

<sub>KB IT's Your Life 7기 - 25반 1팀</sub>

</div>
