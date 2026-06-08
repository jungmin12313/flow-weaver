# flow-weaver

## 소개

이 프로젝트는 사용자의 자연어 요구사항을 분석하여 서로 다른 웹 서비스, 노코드 툴(Make, AppSheet 등), 그리고 데이터베이스(Firebase, SQL) 간의 복잡한 연동 시나리오를 동적으로 생성하고 실행하는 오픈소스 AI 에이전트 오케스트레이터(Orchestrator)입니다.
기존의 하드코딩된 API 연동이나 복잡한 웹훅 설정을 자동화하여, 누구나 말하듯 인프라와 워크플로우를 시스템화할 수 있도록 돕는 가교 역할을 합니다.

## 주요 기능

* **자연어 기반 워크플로우 설계**: "구글 폼 응답이 오면 Firebase를 업데이트하고 외부 API로 알림을 보내줘"와 같은 명령을 해석하여 실행 가능한 JSON 시나리오 맵 생성
* **다이나믹 스키마 매핑 (Dynamic Schema Mapping)**: 이기종 플랫폼 간의 데이터 규격(Payload)을 AI가 실시간으로 분석하여 적절한 필드로 자동 변환 및 라우팅
* **에이전틱 웹훅 엔진 (Agentic Webhook Engine)**: 고정된 엔드포인트가 아닌, 이벤트 조건에 따라 트리거 조건과 데이터 흐름을 동적으로 변경하는 스마트 웹훅 관리

## 사용 방법

### 1. 다운로드

본 저장소를 클론하고 프로젝트에 필요한 의존성 라이브러리를 설치합니다.

```bash
git clone https://github.com/jungmin12313/flow-weaver.git
cd flow-weaver
npm install

```

### 2. 실행

환경 변수(`.env`) 파일에 OpenAI API Key 및 필요한 통합 플랫폼의 크레덴셜을 설정한 후 엔진을 구동합니다.

```bash
# 개발 모드로 오케스트레이터 엔진 실행
npm run dev

# CLI를 통한 자연어 자동화 시나리오 테스트 실행
npm run weaver -- --prompt "Connect my registration form webhook to the centralized database"

```

## 라이선스

MIT License
