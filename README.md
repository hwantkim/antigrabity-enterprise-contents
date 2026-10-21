# Antigravity for Enterprise — 핵심 내용 정리

> Google Cloud의 에이전트 우선(Agent-First) 개발 플랫폼인 **Antigravity**를 엔터프라이즈 환경에 도입하고 확장하기 위한 7개 모듈 학습 내용을 요약·정리한 문서임.
> - 읽기 편하도록 GitHub 내용을 웹페이지로 정리: [엔터프라이즈 환경을 위한 Antigravity 플랫폼 아키텍처 및 거버넌스 가이드](https://cdmstr.kr/mod/forum/discuss.php?d=41)

## 목차

* [M00 — Antigravity for Enterprise Introduction](./M00%20Antigravity_for_Enterprise_Introduction.ipynb)
* [M01 — Antigravity Foundations (Platform Foundations)](./M01%20Antigravity_Foundations.ipynb)
* [M02 — Antigravity Workflows (Agentic Workflows)](./M02%20Antigravity_Workflows.ipynb)
* [M03 — Antigravity at Scale (Enterprise Scale)](./M03%20Antigravity_at_Scale.ipynb)
* [M04 — Antigravity Guardrails (Enterprise Guardrails)](./M04%20Antigravity_Guardrails.ipynb)
* [M05 — Responsible Vibe Coding](./M05%20Responsible_Vibe_Coding.ipynb)
* [M06 — Antigravity for Regulated Environments](./M06%20Antigravity_for_Regulated_Environments.ipynb)
* [모듈별 핵심 역량 요약](#모듈별-핵심-역량-요약)

---

## 코스 개요

본 코스는 단순 코드 자동완성 수준의 도구를 넘어, 엔터프라이즈 환경에서 자율적 소프트웨어 엔지니어링을 수행하는 **통합 서버사이드 에이전틱 하네스(Server-Side Agentic Harness)** 로의 패러다임 전환을 다룸. 각 모듈은 가상 기업 사례 연구를 통해 실제 비즈니스 마찰 요소를 정의하고, 이를 Antigravity 아키텍처로 해결하는 과정을 기술함.

### 핵심 아키텍처 3대 기둥

| 기둥 (Pillar) | 기술 메커니즘 | 엔터프라이즈 가치 |
| :--- | :--- | :--- |
| **Agentic Harness** | 자연어 요구사항을 멀티 파일 엔지니어링 액션으로 변환 | 작업 단위의 end-to-end 개발 자동화 |
| **Deterministic Control** | 구조화된 실행 계획, 실행 원장, 비주얼 diff 제공 | 변경 내역 사전 검증 및 거버넌스 확보 |
| **Server-Side Runtimes** | 빌드·분석·테스트 연산을 클라우드 샌드박스로 오프로드 | 로컬 자원 절약 및 일관된 실행 환경 |

### Prompt-to-Diff 3단계 실행 생명주기

1. **Reasoning Plan** — 자연어 프롬프트를 다단계 작업 로드맵으로 세분화 및 의존성 분석
2. **Execution Diff** — 격리된 샌드박스에서 파일 수정 사항 빌드 및 포맷팅
3. **Human Approval** — 시각적 diff 검증 후 로컬 파일에 최종 반영

---

## 모듈 로드맵

### M00 — Antigravity for Enterprise Introduction

- > **소주제:** 플랫폼 아키텍처 개요, Zero-to-Prompt 온보딩, 토큰 이코노믹스

Antigravity의 전체 아키텍처와 첫 온보딩 가이드를 정리한 기술 문서임. 3대 핵심 아키텍처 기둥(Agentic Harness · Deterministic Control · Server-Side Runtimes), Zero-to-Prompt 3단계 온보딩(설치 → SSO 연동 → 프로젝트 바인딩), 그리고 3대 사용자 인터페이스(CLI `agy` · IDE Extensions · Web Command Center)의 운영 범위와 활용 시나리오를 다룸. 추가로 토큰 이코노믹스 최적화 원칙과 초기 장애 대응 트러블슈팅 가이드를 제공함.

### M01 — Antigravity Foundations (Platform Foundations)

- > **소주제:** Cymbal Bank 사례, 레거시 플러그인 한계, 서버사이드 하네스, 소버린 보안 경계<br>
- > **학습 목표:** 플랫폼 모델 심층 분석 및 최적 타겟 배포 환경 매핑

금융 서비스 산업의 Cymbal Bank 사례를 통해 기존 로컬 AI 플러그인의 한계(보일러플레이트 부담, 섀도우 코드 위험, 시스템 사일로)를 분석하고, Antigravity의 통합 에이전트 우선 플랫폼으로의 전환을 다룸. 서버사이드 하네스 아키텍처, 소버린 보안 경계(Enterprise Identity · Project Isolation), 그리고 4대 진입 접점(Antigravity 2.0 · `agy` CLI · SDK · Agentic-Native Workspace)의 역할을 정의함.

### M02 — Antigravity Workflows (Agentic Workflows)

- > **소주제:** Cymbal Labs 사례, Context Connectors, Command Center 병렬 관제, 연산 크레딧 최적화
- > **학습 목표:** 일상적 에이전트 주도 작업 위임 및 일일 워크플로우 실행

제약·바이오테크 기업 Cymbal Labs의 멀티 사이트 공급망 추적 시스템을 벤치마크로 삼아, 컨텍스트 인지형 에이전트 워크플로우를 체계화함. 3대 마찰 요소(설정 혼란 · 컨텍스트 파편화 · 배포 지연)를 진단하고, `Context Connectors`(Jira · GitHub/GitLab · Confluence 실시간 연결), `Command Center`를 통한 병렬 에이전트 관제, 그리고 연산 크레딧 최적화 전략으로 해결하는 과정을 기술함.

### M03 — Antigravity at Scale (Enterprise Scale)

- > **소주제:** Cymbal Superstore 사례, Shared Memory Substrate, A2A 프로토콜, HITL 프레임워크, Production Readiness Checklist
- > **학습 목표:** 멀티 팀 간 오케스트레이션 전략 아키텍처 설계

전국 단위 리테일 기업 Cymbal Superstore의 50개 이상 엔지니어링 스쿼드 확장 사례를 통해, 개별 개발자 단위 도입에서 전사적 멀티 팀 규모로 확장하기 위한 오케스트레이션 아키텍처를 다룸. 팀 사일로 · 거버넌스 병목 · 지식 유실 문제를 해결하기 위해 **Shared Memory Substrate**, **A2A (Agent-to-Agent) 프로토콜**, 세분화된 **RBAC**, **Human-in-the-Loop (HITL)** 개입 설계, 그리고 **Production Readiness Checklist**(보안 검증 및 Fail-Safe 시뮬레이션)를 체계적으로 정의함.

### M04 — Antigravity Guardrails (Enterprise Guardrails)

- > **소주제:** Cymbal Investments 사례, Policy-as-Code, Strict Mode, Shadow Code 방지, 멀티 리전 정책 동기화, CoE 구축
- > **학습 목표:** 보안 정책 및 거버넌스 가이드라인 강제

글로벌 자산 운용사 Cymbal Investments의 초고빈도 AI 트레이딩 환경을 사례로, 극한의 보안 요구사항과 가속화된 모델 배포 간의 균형을 다룸. **Policy-as-Code**, **Strict Mode** 런타임 통제, **Shadow Code 방지용 동적 훅(Dynamic Hooks)**, 멀티 리전 정책 동기화 메커니즘을 기술하고, 전사 조직의 안전한 에이전트 도입을 이끄는 **변화 관리 플레이북(Change Management Playbook)** 및 **Center of Excellence (CoE)** 구축 방안을 제시함.

### M05 — Responsible Vibe Coding

- > **소주제:** Cymbal Direct 사례, 인지적 경계(Cognitive Boundary), Assisted vs Autonomous Mode, 에이전트 드리프트 감지, Kill Switch SOP
- > **학습 목표:** 비기술 사용자를 위한 안전한 프로토타이핑 설계 및 실행 강도 관리

디지털 네이티브 의류 브랜드 Cymbal Direct의 생성형 광고 카피 플랫폼 구축 사례를 통해, 비개발자 빌더와 시티즌 개발자가 프로덕션 안정성을 해치지 않으면서 창의적 실험(Vibe Coding)을 수행할 수 있는 거버넌스 체계를 다룸. **Assisted Mode**(보조)와 **Autonomous Mode**(자율)의 실행 강도 분리, 3대 안전장치(Safeguards), 샌드박스 격리, 에이전트 드리프트(Agent Drift) 조기 감지 및 세션 강제 종료(Kill Switch) SOP를 정의함.

### M06 — Antigravity for Regulated Environments

- > **소주제:** Cymbal Health 사례, PII/PHI 마스킹, 에이전틱 데이터 계보, 결정론적 감사 추적, 컴플라이언스 드리프트 감지
- > **학습 목표:** 규정 준수 및 감사 가능성 제어 검증

가상 헬스케어 네트워크 Cymbal Health의 AI 기반 진단 보조 서비스 구축 사례를 통해, 의료·금융 등 고위험 규제 환경에서 자율 에이전트 소프트웨어를 안전하게 구축·배포·거버넌스하는 프레임워크를 다룸. **PII/PHI 마스킹 및 데이터 격리**, **에이전틱 데이터 계보(Agentic Lineage) 및 출처(Provenance) 추적**, **결정론적 감사 추적(Deterministic Audit Trails)**, 그리고 **실시간 컴플라이언스 드리프트(Compliance Drift) 탐지 및 에스컬레이션 SOP**를 체계적으로 정리함.

---

## 모듈별 핵심 역량 요약

| 모듈 | 역량 영역 | 핵심 산출물 |
| :--- | :--- | :--- |
| **M00** | 플랫폼 개요 및 온보딩 | 아키텍처 기둥 정의, Zero-to-Prompt 가이드, 토큰 최적화 원칙 |
| **M01** | Platform Foundations | 서버사이드 하네스 설계, 소버린 보안 경계, 4대 인터페이스 매핑 |
| **M02** | Agentic Workflows | Context Connectors 통합, Command Center 병렬 관제, 크레딧 최적화 |
| **M03** | Enterprise Scale | Shared Memory Substrate, A2A 프로토콜, HITL 프레임워크, Readiness Checklist |
| **M04** | Enterprise Guardrails | Policy-as-Code, Strict Mode 런타임 통제, Shadow Code 방지, CoE 구축 |
| **M05** | Responsible Vibe Coding | 인지적 경계 설계, 실행 강도 분리, 에이전트 드리프트 감지, Kill Switch |
| **M06** | Regulated Environments | PII/PHI 마스킹, 에이전틱 계보 추적, 결정론적 감사 추적, 컴플라이언스 드리프트 감지 |
