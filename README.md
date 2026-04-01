# 🚀 Kmong PO AI Workspace (`kmong_ted`)

이 레포지토리는 **Gemini CLI**를 활용하여 크몽 PO의 기획 업무(PRD 작성, 로직 시각화, 기술 검토 등)를 자동화하고 가속화하기 위한 AI 워크스페이스입니다.

## 🪄 주요 기능 (AI Skills)

### 1. `prd-to-mermaid` (기획서 다이어그램 생성기)
텍스트 형태의 PRD나 요구사항을 분석하여 **Mermaid.js** 기반의 전문적인 다이어그램을 자동으로 그려줍니다.
- **지원 다이어그램**: Flowchart, Sequence Diagram, ERD, State Diagram
- **사용 예시**: `"회원가입 로직 분석해서 시퀀스 다이어그램 그려줘"`

---

## 🛠️ 팀원 설치 가이드 (Quick Start)

동료 PO분들도 아래 단계를 통해 이 워크스페이스의 AI 기능을 즉시 사용할 수 있습니다.

### 1. Gemini CLI 설치
(Gemini CLI가 설치되어 있어야 합니다)

### 2. `prd-to-mermaid` 스킬 설치 (한 줄 복사)
```bash
gemini skills install https://github.com/tedjung09090909/kmong_ted/raw/psychedelic-cereal/prd-to-mermaid.skill --scope user
```

### 3. 스킬 활성화
Gemini CLI 세션에서 다음 명령어를 입력하세요.
```bash
/skills reload
```

---

## 📂 프로젝트 아카이브
현재 진행 중인 주요 프로젝트의 기획 및 기술 문서가 포함되어 있습니다.
- **[2026 AI 검색 추천]**: [PRD 보기](./ai-search-recommendation-prd.md) | [Tech Spec 보기](./tech-spec.md) | [다이어그램 모음](./docs/DIAGRAMS.md)

---

## 💡 사용 팁
- **다이어그램 미리보기**: VS Code에서 `Cmd + Shift + V`를 누르면 생성된 다이어그램을 즉시 시각화하여 볼 수 있습니다.
- **실시간 리서치**: "최신 이커머스 검색 추천 트렌드 조사해줘"와 같은 명령어로 리서치 업무를 병행하세요.

---
*마지막 업데이트: 2026-04-01*
