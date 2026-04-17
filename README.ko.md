**한국어** | [English](README.md)

# 사이클링 프레임워크

8개의 근거 기반 프레임워크로 구성된 데이터 중심 사이클링 코칭 시스템. 훈련, 영양, 장비, 이벤트 관련 질문을 자동으로 최적 프레임워크로 라우팅합니다. Coggan 파워존, Friel 주기화, Seiler 분극화 훈련 등을 기반으로 하며, 한국 사이클리스트 맥락(즈위프트, 브레베, 그란폰도 문화)이 내장되어 있습니다.

> 의료 조언이 아닙니다. 건강 문제는 스포츠 의학 전문가와 상담하세요.

## 설치

```bash
claude plugin install ironyjk/cycling-framework
```

## 단축 커맨드 설정

설치 후 `/ride` 래퍼 커맨드를 추가하세요:

```markdown
# ~/.claude/commands/ride.md
---
description: "Cycling coaching — 8 frameworks. Shortcut for /cycling-framework:ride"
---
Invoke the skill `cycling-framework:ride` with these arguments: $ARGUMENTS
```

자세한 내용은 [마켓플레이스 래퍼 가이드](https://github.com/ironyjk/claude-frameworks-marketplace)를 참조하세요.

## 프레임워크

| 커맨드 | 프레임워크 | 저자 / 방법론 |
|--------|------------|--------------|
| `/ride` | 메타 라우터 | 최적 서브 프레임워크 1~3개 자동 선택 |
| `power-zones` | 파워존 훈련 | Coggan 7존 모델, FTP, TSS/CTL/ATL/TSB |
| `periodization` | 훈련 주기화 | Friel, 선형/블록/역주기화 |
| `polarized-training` | 분극화 훈련 | Seiler 80/20, Z2 베이스, Zone 5 인터벌 |
| `nutrition-fueling` | 사이클링 영양 | 탄수화물 로딩, 라이딩 중 보급, 수분 관리 |
| `bike-fit-equipment` | 바이크핏·장비 | 안장 높이, 클릿 각도, 에어로 포지션 |
| `indoor-training` | 실내 훈련 | 즈위프트, 구조화 워크아웃, ERG 모드 |
| `endurance-events` | 장거리 이벤트 | 브레베, 그란폰도, 멀티데이 준비 |
| `injury-prevention` | 부상 예방 | 과사용 부상, 회복, 이동성 |

## 사용 예시

```
/ride  8주 후 200km 브레베 참가 예정. FTP 220W, 주 10시간 훈련 중.
/ride  장거리 라이딩 후마다 무릎이 아파요. 원인이 뭔가요?
/ride  5시간 그란폰도의 최적 영양 전략은?
```

## 라이선스

[CC-BY-NC 4.0](LICENSE) — 개인/교육 목적 무료. 상업적 이용 문의: ironyjk@gmail.com

## 관련 프레임워크

- `/fit` ([health-framework](https://github.com/ironyjk/health-framework)) — 일반 건강, 근력, 영양
- `/think` ([strategy-frameworks](https://github.com/ironyjk/strategy-frameworks)) — 의사결정 프레임워크
- [claude-frameworks-marketplace](https://github.com/ironyjk/claude-frameworks-marketplace) — 전체 프레임워크 목록
