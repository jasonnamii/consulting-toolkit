# consulting-toolkit

> 🇺🇸 [English README](./README.md)

**컨설팅 5계열 25기술 자동 라우팅. 자연어→구조화·문제해결·질문·설득·실행 기술 선택·적용. 트리거 외울 필요 없음. 진단·적용·설계 3모드.**

## 사전 요구

- **Claude Cowork 또는 Claude Code** 환경

## 목표

MECE·SCQA·5Whys·Pyramid 같은 컨설팅 기술은 강력하지만, 어느 상황에 뭘 꺼낼지 외우기 어려운 게 병목이다. 본 스킬은 형의 자연어 의도를 파싱해서 5계열 × 5기술 = 25개 도구 중 맞는 것을 자동 선택하고, 입력→처리→출력 정형으로 적용한다.

## 사용 시점 & 방법

트리거 단어 명시(MECE·SCQA·5Whys·Pyramid·Pareto·Stakeholder Mapping·Nudging 등) 또는 자연어 의도("구조화해줘", "왜 안돼", "임원 설득") 양쪽 다 발동한다. 1~3개 기술을 선택해서 고정 순서(구조화→문제해결→질문→설득→실행)로 적용하고, 결과 상단에 "적용 기술: {계열}.{기술}" 1줄을 박아 학습 가능하게 만든다.

## 사용 사례

| 상황 | 프롬프트 | 동작 |
|---|---|---|
| 사업 부진 진단 | `"왜 매출이 안 오르는지 분석해줘"` | 이슈트리 → 5Whys → 파레토로 우선순위 |
| 임원 1페이지 자료 | `"이사회 한 장짜리 준비해줘"` | Pyramid + SCQA + Executive Summary |
| 팀 교착 해소 | `"기술 스택 결정 못 하고 있어"` | Alignment Building → Decision Framework |
| 고객 인터뷰 설계 | `"잠재고객 인터뷰 어떻게?"` | Funneling → Active Listening → Probing |
| 혁신 접근 탐색 | `"기존 방식 안 돼"` | 제1원리 → How-Tree |

## 주요 기능

- **트리거 단어 외우기 불필요** — 자연어만으로 작동
- **5×5 기술 카탈로그** — 맥킨지·BCG 표준 25기술, 각각 입력→처리→출력 정형
- **고정 실행 순서** — 구조화→문제해결→질문→설득→실행. 역순 차단
- **확신도 병기** — 모든 출력에 높음90/보통70/낮음50 + 근거 1줄
- **3모드** — 진단(추천), 적용(실행), 설계(Phase 체인)
- **[trigger-dictionary](https://github.com/jasonnamii/trigger-dictionary)와 경계 선언** — 중복 4쌍(제1원리·넛지·백본·스켈레톤)은 단어 명시 호출 시 trigger-dictionary로, 자연어 호출 시 본 스킬로 라우팅

## 연동 스킬

- **[trigger-dictionary](https://github.com/jasonnamii/trigger-dictionary)** — 24개 사고도구(홈즈·오컴·프리모르템). 단어 명시 진입점, 본 스킬은 자연어 진입점
- **[biz-skill](https://github.com/jasonnamii/biz-skill)** — 18축 사업전략 패턴 (도메인 특화)
- **[meeting-engine](https://github.com/jasonnamii/meeting-engine)** — 회의 전주기 (아젠다→회의록→액션아이템)

## 설치

```bash
git clone https://github.com/jasonnamii/consulting-toolkit.git ~/.claude/skills/consulting-toolkit
```

## 업데이트

```bash
cd ~/.claude/skills/consulting-toolkit && git pull
```

`~/.claude/skills/`에 배치된 스킬은 Claude Code 및 Cowork 세션에서 자동으로 사용 가능합니다.

## Cowork Skills

25개 이상의 커스텀 스킬 중 하나입니다. 전체 카탈로그: [github.com/jasonnamii/cowork-skills](https://github.com/jasonnamii/cowork-skills)

## 라이선스

MIT License — 자유롭게 사용, 수정, 공유 가능합니다.
