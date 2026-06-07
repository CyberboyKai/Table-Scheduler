# 🍽️ Table Scheduler

음식점 호스트를 위한 테이블(손님) 배정 도구. 손님이 들어올 때마다 어느 서버에게 배정할지 자동으로 추천해서, 서버 간 손님 수를 공평하게 유지합니다.

A party-assignment tool for restaurant hosts. Suggests which server should take each incoming party, keeping guest counts balanced across servers.

**▶ 바로 사용하기 / Live app:** https://cyberboykai.github.io/Table-Scheduler/

## 배정 규칙 / Assignment Rules

1. **출근 순서 우선** — 오늘 첫 손님을 아직 못 받은 서버가 출근 순서대로 먼저 배정받습니다.
2. **헤드카운트 균형** — 이후에는 현재 앉아있는 손님 수가 가장 적은 서버에게 배정합니다.
3. **노는 서버 방지** — 손님 수가 같으면 마지막 배정이 가장 오래된 서버가 우선입니다.

> 1. Servers who haven't had a party yet go first, in clock-in order.
> 2. After that, the server with the fewest seated guests gets the next party.
> 3. Ties go to whoever has waited longest since their last seating.

## 주요 기능 / Features

- ⚡ **원탭 배정** — 인원수 입력 후 Enter 한 번이면 추천 서버에게 즉시 배정
- ☕ **브레이크** — 휴식 중인 서버는 추천에서 자동 제외 (수동 배정은 가능)
- ⭐ **예외배정** — 단골 요청 등 호스트 판단으로 서버 직접 지정
- 📋 **배정 기록 사이드바** — 실수한 배정 취소, 퇴장 취소(복구) 가능
- 🌐 **한국어 / English** 전환
- 💾 설치·서버 불필요 — 브라우저(localStorage)에 자동 저장

## 사용 방법 / How to Use

1. **설정** 탭에서 직원 명단 등록
2. 매일 아침 **플로어** 탭에서 출근 순서대로 출근 처리
3. 손님이 오면 인원수 입력 → 추천 서버에게 배정 (Enter)
4. 손님이 가면 서버 카드의 초록 팀 칩을 눌러 퇴장 처리
5. 하루가 끝나면 **설정 → 새 영업일 시작**으로 초기화

## 기술 / Tech

단일 `index.html` 파일 — 프레임워크·빌드·백엔드 없음. 데이터는 기기별 브라우저 localStorage에 저장됩니다 (기기 간 동기화 없음).

Single `index.html` — no framework, no build step, no backend. Data lives in the browser's localStorage (per-device, no sync).
