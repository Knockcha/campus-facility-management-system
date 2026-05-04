# Campus Facility Management System 🏫

> 학교 시설을 통합 관리하는 풀스택 웹 시스템 — **시설 예약 · 도서관 · 동아리 · 기숙사 · 식당 · 상담 · 마이페이지 + 관리자 기능**.
> Spring Boot + React 기반 팀 프로젝트(3인).

Forked from [`WizWix/campus-facility-management-system`](https://github.com/WizWix/campus-facility-management-system)
작업 기간: **2026-02-19 ~ 2026-03-05 (약 2주)** · 팀: WizWix(팀장) · soooojinn(수진) · **Knockcha(본인)**

---

## ✨ Features

- 🔐 **인증/권한** — 회원가입 / 로그인 / 비밀번호 재설정, `ROLE_USER` / `ROLE_ADMIN` / 교수 역할 분기
- 🏛 **시설 예약** — 강의실·시설 단위 예약 + 마이페이지 예약 내역 + 관리자 예약 관리
- 📚 **도서관** — 도서 등록 / 검색 / 대출 / 삭제 (조건 완화 룰 적용)
- 🎭 **동아리** — 동아리 생성 / 회장 자동 ClubMember 등록 / 마이페이지 동아리 탭
- 🛏 **기숙사** — 신청 / 층별 정렬 / 신청자 이름 표시
- 🍱 **식당** — 오늘의 학식 + 푸드코트 메뉴
- 💬 **상담** — 상담 예약
- 🛠 **관리자** — 사용자/예약/도서/동아리 통합 관리

---

## 🛠 Tech Stack

| Layer | Stack |
| --- | --- |
| Backend | Java · **Spring Boot** · Spring Security · Gradle |
| Frontend | **React** · JSX · Vite · **Bun** (runtime) |
| Persistence | JPA · `JpaRepository` · DevLoader 기반 dev 시드 |
| Auth | Spring Security · `RequestLogin` / `RequestRegister` / `RequestPasswordReset` DTO |
| API 도메인 | Auth · Building · Cafeteria · Club · Dorms · Reservation · Room · Admin · User |

---

## 🙋 My Contributions (by [@Knockcha](https://github.com/Knockcha))

> 단일 영역이 아니라 **풀스택 전반(DTO · Controller · Repository · Frontend · DevLoader 인프라)**을 횡단하며 16건의 PR을 머지했습니다.
> 그중 **동아리 모듈은 사실상 단독 구현**(`feature/club-page` 브랜치 주도, 5 PR).

### 기능 단위 정리

| 영역 | PR | 핵심 작업 |
| --- | --- | --- |
| **동아리 (단독 구현)** | #14 · #17 · #19 · #20 · #21 | 프론트엔드 전체 구현 + 회장 NPE fix + 회장 자동 `ClubMember` 등록 + 마이페이지 동아리 탭 |
| 식당 | #1 · #2 | 식당 페이지 (오늘의 학식 + 푸드코트) |
| 기숙사 | #2 · #15 · #16 | 신청 / 층 순서 버그 / 신청인 이름 표시 |
| 시설·상담 예약 | #3 · #4 | 시설예약 DB 연동, `ROLE_ADMIN`, 상담 예약 |
| 도서관 | #6 · #10 | 도서관 기능 추가, 보완, 삭제 조건 완화 |
| 마이페이지 | #2 · #10 | 마이페이지 예약, 관리자 예약관리, 네이밍 통일 |
| **DevLoader 인프라** | #4 · #5 · #7 | DevLoader 양식 통일, unload 미정리 fix, dev profile 기본 활성화, 키 불일치 fix |
| QA / 권한 | #13 | QA 버그 일괄 수정 + 예약 취소 + 교수 역할 + 관리자 보강 |

### 어필 포인트

- ✅ **풀스택 횡단** — DTO·Controller·Repository·Frontend·인프라까지 동시에 다룸
- ✅ **모듈 단독 구현 경험** — 동아리 모듈을 5 PR에 걸쳐 단독 설계/구현
- ✅ **버그 fix·QA 비중** — NPE / 키 불일치 / 데이터 정합 문제를 협업 중 잡아냄
- ✅ **리팩터링 의식** — DevLoader 양식 통일 등 코드 품질 작업 직접 주도

---

## 🚀 Run

```bash
# Backend
./gradlew bootRun

# Frontend
cd frontend
bun install
bun run dev
```
