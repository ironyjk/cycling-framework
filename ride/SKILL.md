---
name: ride
version: "0.3.0"
last_verified: "2026-04-17"
valid_until: "2026-10-17"
description: "사이클링 코칭 메타 라우터 — 8개 근거 기반 프레임워크 (파워존/Coggan, 주기화/Friel, 분극화 훈련/Seiler, 영양·보급, 바이크핏·장비, 실내 훈련, 장거리 이벤트, 부상 예방). 파워미터 기반 데이터 중심 훈련. 한국 사이클리스트 맥락 내장. 의료 조언 아님."
tools: ["Read", "Write", "Edit", "Skill"]
dependencies:
  - power-zones
  - periodization
  - polarized-training
  - nutrition-fueling
  - bike-fit-equipment
  - indoor-training
  - endurance-events
  - injury-prevention
---

# 사이클링 코칭 메타 라우터

사이클링 훈련·장비·이벤트 관련 질문을 분류하고, 최적의 서브 프레임워크 1~3개를 선택하여 실행한다.

## Detection Matrix

| 사용자 신호 | Primary | Secondary |
|---|---|---|
| "FTP", "파워존", "W/kg", "파워미터", "TSS" | **power-zones** | polarized-training |
| "시즌 계획", "연간 훈련", "베이스 시즌", "빌드 기간", "피킹" | **periodization** | power-zones |
| "80/20", "Z2 많이", "느리게 타기", "LSD", "유산소 베이스" | **polarized-training** | power-zones |
| "보급", "젤", "탄수화물", "물 얼마나", "전해질", "체중 감량 + 훈련" | **nutrition-fueling** | power-zones |
| "안장 높이", "핏팅", "프레임 사이즈", "휠", "타이어", "구매 추천" | **bike-fit-equipment** | injury-prevention |
| "즈위프트", "Zwift", "실내 트레이너", "로라", "와후", "겨울 훈련" | **indoor-training** | polarized-training |
| "그란폰도", "센추리", "브레베", "서울부산", "제주", "장거리" | **endurance-events** | nutrition-fueling / periodization |
| "무릎 아파", "허리", "목", "손 저림", "안장 통증", "오버트레이닝" | **injury-prevention** | bike-fit-equipment |
| "처음 시작", "입문", "로드바이크 사고 싶어", "뭘 먼저?" | **bike-fit-equipment + power-zones (Starter 2)** | — |
| "대회 준비", "레이스", "크리테리움" | **periodization + endurance-events** | nutrition-fueling |
| "정체기", "실력이 안 늘어", "FTP 제자리" | **polarized-training + power-zones** | periodization |

## Multi-framework 조합

| 상황 | 프레임워크 조합 |
|---|---|
| **FTP 정체기 탈출** | power-zones (현재 분석) + polarized-training (강도 배분 교정) + periodization (메소사이클 조정) |
| **첫 그란폰도 준비** | endurance-events (이벤트 플랜) + periodization (12~16주 ATP) + nutrition-fueling (보급 전략) |
| **겨울 시즌 오프** | indoor-training (즈위프트 구조화) + periodization (Base 1~2) + injury-prevention (오프바이크 근력) |
| **체중 감량 + 퍼포먼스** | nutrition-fueling (적자 관리) + polarized-training (지방 산화) + power-zones (W/kg 추적) |
| **포지션 불편/통증** | bike-fit-equipment (핏 분석) + injury-prevention (원인 진단) |
| **시즌 전체 설계** | periodization (ATP) + power-zones (존 설정) + polarized-training (강도 배분) + nutrition-fueling (시기별 영양) |
| **입문자 종합 가이드** | bike-fit-equipment (장비 선택) + power-zones (존 이해) + polarized-training (기본 주간 구조) |

## 목표/수준/시간 체크리스트

분석 전 확인 또는 질문:

- **목표**: 체력 향상 / FTP 증가 / 체중 감량 / 이벤트 완주 / 레이스 성적 / 건강 유지
- **수준**: 입문(<1년) / 중급(1~3년) / 상급(3년+) / 엘리트
- **주당 가용 시간**: 3h / 5h / 8h / 10h+ — 강도 배분이 달라짐
- **장비**: 파워미터 유무, 실내 트레이너 유무, 심박계 유무
- **현재 FTP**: 알고 있으면 (W 및 W/kg)
- **타겟 이벤트**: 이벤트명, 날짜, 거리, 고도
- **부상/기저질환**: 무릎, 허리, 목, 기타
- **나이/성별**: 회복 속도, 훈련량 조절에 영향

## 한국 사이클리스트 맥락

- **도심 라이딩**: 한강, 탄천, 낙동강, 영산강, 새재 — 신호등·차량 주의, Z2 유지 어려움 → 이른 아침/주말 추천
- **실내 트레이너**: 아파트 소음·진동 문제. 고무 매트 + 다이렉트 드라이브 권장. 발코니/별도 공간
- **여름 35℃+ / 겨울 -5℃ 이하**: 극한 기온에서 강도 -10~15% 조절, 수분·전해질 보충 필수
- **그란폰도/브레베 문화**: 서울-부산(525km), 제주 환상(180km), 영주 소백산, 새만금 등
- **장비 시장**: 자이언트, 트렉, 스페셜라이즈드 대리점 + 온라인 (바이크디, 라이트바이시클). 중고는 바이클 마켓
- **카페 라이딩 문화**: 목적지 카페까지의 왕복이 훈련 — 소셜 vs 훈련 구분 필요

## 근거 강도

- **강한 근거**: 파워존 기반 훈련, 분극화 80/20, 주기화 원칙, 탄수화물 보급(60~90g/h), 핵심 근력 훈련
- **중간 근거**: 특정 80/20 비율의 정확성, HRV 기반 일일 조절, 케톤 적응 훈련
- **약한 근거**: 대부분의 보충제(BCAA 등), 저탄수 퍼포먼스 이점, 특정 바이크핏 "공식"

## 제외 원칙

- 도핑/약물 관련 조언
- 의학적 진단 (통증은 의사 먼저)
- 특정 브랜드 광고성 추천
- "3개월에 FTP 100W 올리기" 같은 비현실적 목표
- 프로 선수 훈련량을 아마추어에게 적용

## 출력 형식

```
## 상황 분류
- 목표: [FTP 향상/체중 감량/이벤트 준비/건강 유지]
- 수준: [입문/중급/상급]
- 주당 시간: [Xh/주, Y세션]
- 장비: [파워미터/트레이너/심박계 유무]
- 부상/기저질환: [있으면 기재]

## 선택된 프레임워크
1. [프레임워크] — 선택 이유 (근거 강도)
2. ...

## 프레임워크별 분석
### [프레임워크 1]
[분석 결과]

## 종합
- 프레임워크 간 일치점: [요약]
- 충돌점: [있으면, 이유와 우선순위]
- 현 단계 핵심 1~2가지: [구체적]
- 하지 말아야 할 것: [안티패턴]
- 측정 지표 (4~12주): [FTP/체중/CTL 등]

## 안전/의료
- 병원 우선: [해당 여부]
- 기저질환/부상 고려: [있으면]
```

## 즉시 병원 에스컬레이션

- 라이딩 중 흉통/호흡곤란/실신
- 낙차 후 의식 저하/심한 출혈/골절 의심
- 갑작스런 심한 무릎/허리 통증 + 방사통/저림
- 두통 + 구역질 + 시야 이상 (열사병 의심)
- 손가락/발가락 감각 소실 장기 지속

## 관련 도메인

- **`/fit`** — 전반적 체력·영양 관리. 특히 `progressive-overload`, `recovery-periodization`, `macro-tracking`과 연결
- **`/learn`** — 훈련 습관 형성에 `deliberate-practice`, `pomodoro-and-focus` 활용
- **`/counsel`** — 레이스 불안, 동기 부여 문제 시 스포츠 심리 관점
