---
name: power-zones
version: "0.1.0"
description: "파워존 기반 훈련 — Coggan 7존 모델, FTP 테스트, TSS/CTL/ATL/TSB 피로 관리. 파워미터 데이터 중심 사이클링 훈련의 기초."
---

# 파워존 기반 훈련 (Coggan Power Zones)

## 한줄 요약

**FTP(Functional Threshold Power)를 기준으로 7개 파워존을 설정하고, TSS/CTL/ATL/TSB로 훈련 부하와 피로를 정량 관리한다.** 파워미터가 있는 사이클리스트의 훈련 설계와 모니터링의 기초.

## 근거 강도

- Coggan 7존 모델: **강함** (실무 표준, TrainingPeaks/Zwift/WKO 등 모든 플랫폼 채택)
- FTP 기반 존 설정: **강함** (MLSS와 높은 상관)
- TSS/CTL/ATL/TSB 모델: **중간** (편리하지만 단순화. 개인차 큼)
- 20분 FTP 테스트 ×0.95: **중간** (개인차 있음, 과대/과소 추정 가능)

## 이론·근거 출처

- **Andrew Coggan, PhD** & **Hunter Allen** — *Training and Racing with a Power Meter* (2006, 3rd ed. 2019)
- **WKO5** — 파워 듀레이션 커브 분석
- **TrainingPeaks** — PMC(Performance Management Chart) 시스템

## 7개 파워존

| Zone | 이름 | %FTP | 시간 | 목적 | 체감 |
|---|---|---|---|---|---|
| Z1 | Active Recovery | <55% | 무제한 | 회복 | 매우 쉬움 |
| Z2 | Endurance | 56~75% | 2~6h | 유산소 베이스 | 대화 가능 |
| Z3 | Tempo | 76~90% | 1~3h | 지구력 | 짧은 문장 |
| Z4 | Lactate Threshold | 91~105% | 20~60min | FTP 향상 | 힘듦 |
| Z5 | VO2max | 106~120% | 3~8min | 최대산소섭취량 | 매우 힘듦 |
| Z6 | Anaerobic Capacity | 121~150% | 30s~2min | 무산소 용량 | 극한 |
| Z7 | Neuromuscular Power | >150% | <15s | 순발력 | 전력 |

## FTP 테스트 프로토콜

### 20분 테스트 (가장 보편적)
1. 워밍업 20분 (Z2 + 짧은 가속 3×1min)
2. 5분 전력 (다리 비움)
3. 10분 이지
4. **20분 전력** — 일정한 파워로 최대 유지
5. 쿨다운 10분
6. **FTP = 20분 평균 파워 × 0.95**

### 램프 테스트 (간편)
1. 100W에서 시작, 매분 20W씩 증가
2. 더 이상 못 버틸 때까지
3. **FTP = 마지막 1분 평균 × 0.75**
- 장점: 간편, 정신적 부담 적음
- 단점: 무산소 용량 큰 사람은 과대 추정

### 60분 테스트 (골드 스탠다드)
- 60분 타임트라이얼의 평균 파워 = FTP
- 가장 정확하지만 정신적으로 극히 어려움
- 대회 경험자에게만 추천

### 테스트 주기
- **4~8주마다** 재테스트 (또는 훈련 블록 전환 시)
- 존 설정이 오래되면 훈련 강도가 부정확해짐
- 급격한 체력 변화(복귀, 시즌 초) 시에는 더 자주

## W/kg 기준표

| 수준 | 남성 W/kg | 여성 W/kg | 설명 |
|---|---|---|---|
| 입문 | 1.5~2.5 | 1.2~2.0 | 시작한 지 1년 미만 |
| 중급 | 2.5~3.5 | 2.0~3.0 | 규칙적 훈련 1~3년 |
| 상급 | 3.5~4.5 | 3.0~3.8 | 체계적 훈련 3년+ |
| 엘리트/아마추어 레이서 | 4.5~5.5 | 3.8~4.5 | 대회 입상 수준 |
| 프로 | 5.5+ | 4.5+ | 월드투어 수준 |

> 체중이 줄면 W/kg은 올라감. 체중 관리와 FTP 향상을 병행하면 효과 배가.

## TSS/CTL/ATL/TSB — 훈련 부하 관리

### TSS (Training Stress Score)
- **공식**: TSS = (초 × NP × IF) / (FTP × 3600) × 100
- **IF** (Intensity Factor) = NP / FTP
- **NP** (Normalized Power) = 30초 이동평균의 4제곱근
- 대략적 기준:
  - Z2 1시간 ≈ 40~60 TSS
  - Z4 인터벌 1시간 ≈ 70~90 TSS
  - 레이스 1시간 ≈ 80~120 TSS

### CTL (Chronic Training Load) — "체력"
- 42일 지수가중 이동평균 of 일일 TSS
- 장기적 훈련 적응도를 반영
- 주당 CTL 증가 목표: **3~7 포인트** (과도한 증가 = 부상 위험)

### ATL (Acute Training Load) — "피로"
- 7일 지수가중 이동평균 of 일일 TSS
- 단기 피로 축적을 반영

### TSB (Training Stress Balance) — "컨디션"
- **TSB = CTL - ATL**
- 양수(+): 충분히 회복됨 → 레이스 가능
- 음수(-): 피로 축적 → 훈련 적응 중
- 레이스 당일 목표: TSB +10~+25 (피킹)
- 일상 훈련: TSB -10~-30 (적절한 과부하)

### PMC (Performance Management Chart)
```
CTL ──── 천천히 우상향 (체력 축적)
ATL ──── 파도처럼 오르내림 (훈련/휴식 사이클)
TSB ──── ATL이 높을 때 음수, 휴식 후 양수
```

## 파워 듀레이션 커브 (Power Profile)

- 5초 / 1분 / 5분 / 20분 / 60분 최대 파워를 기록
- 강점/약점 진단:
  - 5초 높고 5분 낮음 → 스프린터형 (크리테리움 강점)
  - 5분/20분 높고 5초 낮음 → 클라이머형
  - 20분/60분 높고 5분 낮음 → 타임트라이얼러형
- WKO5 또는 Intervals.icu에서 자동 분석

## 한국 사이클리스트 현실

- **파워미터 보급 확대**: Assioma, 4iiii, Stages 가격대 30~50만원. 가성비 최고 업그레이드
- **심박계만 있는 경우**: HR존으로 시작 가능하지만, HR은 지연·변동이 커서 인터벌 정확도 낮음
- **실내 트레이너**: 즈위프트에서 자동 파워 측정. ERG 모드로 정확한 존 훈련 가능
- **Strava/TrainingPeaks/Intervals.icu**: 무료~유료 플랫폼으로 PMC 관리

## 안티패턴

- **FTP 테스트 없이 감으로 존 설정** — 대부분 Z2가 너무 높아짐 (그레이존 함정)
- **항상 Z3~Z4로 타기** — "적당히 힘든" 강도는 최악의 적응/피로 비율
- **TSS만 추적, IF 무시** — 100TSS가 Z2 2시간과 Z5 인터벌 1시간은 완전히 다름
- **CTL 숫자에 집착** — CTL 100이 목표가 아님. 목표 이벤트에 맞는 피크 CTL이 중요
- **FTP 테스트를 너무 자주** — 스트레스·시간 낭비. 4~8주가 적절
- **NP를 평균 파워와 혼동** — 언덕+평지 라이딩에서 NP >> 평균. NP가 실제 부하를 더 정확히 반영

## 한계

1. FTP는 단일 지표 — 5초, 1분, 5분 파워를 함께 봐야 전체 프로필 파악
2. TSS 모델은 단순화 — 실제 피로·적응은 개인차 큼
3. 파워미터 없으면 적용 어려움 — HR+RPE로 대체 가능하나 정확도 떨어짐
4. FTP는 날씨·수면·영양·스트레스에 영향받음

## 함께 쓰면 좋은 프레임워크

- `polarized-training` — 존별 시간 배분 전략
- `periodization` — 시즌 내 FTP 테스트 타이밍과 존 조정
- `recovery-periodization` (`/fit`) — 피로 관리와 디로드

## 참고 문헌

- Coggan, A., Allen, H. *Training and Racing with a Power Meter* (3rd ed., 2019)
- Allen, H. *Power Meter Handbook* (2012)
- Coggan, A. "Power profiling." — TrainingPeaks Blog
- Intervals.icu — 무료 PMC 및 파워 분석
