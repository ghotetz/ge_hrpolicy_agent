# 📌 Google ADK HR Policy Agent
> 입사 연차 별 연차 일수 자동 계산 에이전트
>
> Google-ADK 를 활용한 AI Agent 사용 예시

## ⚡ 주요 기능 (Features)
> 법적 제공 연차(최대 25일, 최소 11일) 을 자동으로 계산

## 🛠 기술 스택 (Tech Stack)
- Google ADK, Python, Function-calling, Gemini-Enterprise, AI-Agent

## 💻 시작 가이드 (Getting Started)
- Google Cloud 인증
```bash
gcloud auth login
gcloud auth application-default login
gcloud config set project ax-gemini-lab
```

- Google ADK 설치
```bash
python -m venv .venv && source .venv/bin/activate
pip install google-adk litellm
```

- ADK 검증
```bash
adk web
127.0.0.1:8000
```

- Agent 동작 확인
```bash
2023-03-02 입사자의 올해 연차는 며칠이야? > 도구 호출 이벤트와 계산 결과가 보이는지 확인
```


- 검증 완료 후 Gemini Enterprise 에 에이전트로 등록
```bash
adk deploy agent_engine \
  --project="프로젝트명" \
  --region="리전명" \
  --display_name="에이전트명" \
  "에이전트 프로젝트 경로"
```
