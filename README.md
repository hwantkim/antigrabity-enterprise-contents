## 프롬프트 투 디프 생애주기 (The Prompt-to-Diff Lifecycle)
* **Phase 1: 추론 계획 (Reasoning Plan):** 에이전트가 자연어 프롬프트를 다단계 작업 로드맵으로 분해함.
* **Phase 2: 실행 디프 (Execution Diff):** 플랫폼이 샌드박스 상태에서 파일 수정을 빌드하고 포맷함.
* **Phase 3: 인간 승인 (Human Approval):** 변경 사항이 로컬 파일에 반영되기 전에 사이드바 방식의 코드 디프를 검토함.

---

## 사용자 인터페이스 탐색 (Navigating the User Interfaces)
* **CLI (`agy`):** 빠른 스크립트 생성 및 리팩토링 작업을 위해 터미널 네이티브로 실행함
* **IDE Extensions:** 인라인 계획 및 검토를 위해 매일 사용하는 편집기 내부에 임베디드된 패널임
* **Web Command Center:** 여러 스쿼드에 대한 광범위한 다중 관리 및 관리자 제어를 위한 중앙 집중형 브라우저 허브임

---

## 토큰 경제학 및 컨텍스트 마스터하기 (Mastering Token Economics & Context)
* **과도한 붙여넣기 방지:** 전체 코드 디렉토리를 프롬프트에 붙여넣지 말고, 에이전트가 파일을 동적으로 검색하도록 유도하는 것이 좋음.
* **성능 최적화:** 컨텍스트 창을 간소화하여 더 빠른 응답 시간과 높은 추론 정확도를 보장함.
* **참조 활용:** 대상 태그와 커넥터를 사용하여 에이전트를 관련 모듈에 직접 연결함.

---

## 첫 실행 문제 해결 (Troubleshooting First-Run Pitfalls)
* **인증 시간 초과 (Authentication Timeouts):** 기업 토큰이 만료된 경우 `agy login`을 통한 빠른 재인증을 진행함
* **권한 경고 (Permission Warnings):** 파일 액세스가 차단되었을 때 활성 Google Cloud 프로젝트 바인딩을 확인함
* **세션 리셋 (Session Resets):** 멈춘 에이전트 루프를 재시작하기 위해 로컬 캐시 상태를 안전하게 지움
