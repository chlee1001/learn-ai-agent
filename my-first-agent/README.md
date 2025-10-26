# My First Agent

AI Agent 학습을 위한 첫 번째 프로젝트입니다.

## 📋 Changelog

### 2025-10-26 - Initial Setup

#### Environment Setup
- Python 3.13 환경 구성 (`.python-version`)
- UV 패키지 매니저를 사용한 프로젝트 초기화
- 가상환경 생성 (`.venv`)

#### Dependencies
 OpenAI Python SDK 설치 (`openai>=1.98.0`)
  - GPT 모델 API 사용을 위한 공식 클라이언트 라이브러리

#### Configuration Files
- `.env` 파일 생성 및 API 키 설정
  - `OPENAI_API_KEY`: OpenAI API 인증을 위한 키 등록
- `.gitignore` 설정
  - Python 빌드 파일 제외 (`__pycache__/`, `*.pyc`, `build/`, `dist/`)
  - 가상환경 제외 (`.venv`)
  - 환경변수 파일 제외 (`.env`)

#### Code Development
- `main.py`: 기본 엔트리포인트 생성
  - Hello World 수준의 초기 코드
- `main.ipynb`: Jupyter Notebook 실습 파일
  - OpenAI API 클라이언트 초기화
  - Function Calling 기본 개념 테스트
  - 날씨/환율/뉴스 함수 시뮬레이션 예제
  - GPT-5-nano 모델을 사용한 함수 호출 테스트

#### Learning Summary (from Video Tutorial)
- **AI Agent 핵심 개념 학습**
  - AI Agent = LLM + 도구(함수) 제공 + 실행 루프
  - LLM은 텍스트 예측 엔진이며, 코드를 직접 실행할 수 없음
  - 프롬프트 엔지니어링을 통해 함수 선택 패턴 구현

- **구현 패턴**
  1. 프롬프트에 사용 가능한 함수 목록 정의
  2. LLM에게 실행할 함수 선택 요청
  3. 개발자가 선택된 함수 실행
  4. 실행 결과를 LLM에 다시 전달
  5. LLM이 최종 응답 생성

- **실습 결과**
  - 질문: "What is the weather in Greece?"
  - LLM 응답: `get_weather('Greece')`
  - 올바른 함수와 인자 선택 성공!

## 🚀 Getting Started

### Prerequisites
```bash
# Python 3.13 이상 필요
python --version

# UV 패키지 매니저 설치
pip install uv
```

### Installation
```bash
# 가상환경 활성화
source .venv/bin/activate  # macOS/Linux
# or
.venv\Scripts\activate  # Windows

# 의존성 설치
uv sync
```

### Environment Variables
`.env` 파일에 다음 설정 필요:
```bash
OPENAI_API_KEY="your-api-key-here"
```

### Run
```bash
# Python 스크립트 실행
python main.py

# Jupyter Notebook 실행
jupyter notebook main.ipynb
```

## 📝 Notes
- Function Calling 패턴을 사용하여 AI가 적절한 함수를 선택하도록 학습 중
- GPT-5-nano 모델 사용 (reasoning tokens 포함)
- 실제 함수 구현은 아직 없으며, 함수 선택 로직만 테스트 완료

