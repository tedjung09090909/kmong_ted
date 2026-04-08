---
name: prd-to-mermaid
description: PRD나 요구사항 텍스트를 분석하여 Mermaid.js 다이어그램(Flowchart, Sequence, ERD, State)을 생성합니다. 기획서나 로직 설명 후 "다이어그램 그려줘" 요청 시 사용하세요.
---

# PRD-to-Mermaid

## 워크플로우

1. **입력 분석**: 제공된 PRD 또는 요구사항에서 주요 액터, 프로세스, 데이터 구조를 파악합니다.
2. **다이어그램 유형 선택**:
   - **Flowchart (`graph TD`)**: 비즈니스 로직, 유저 플로우, 의사결정 흐름에 사용
   - **Sequence Diagram**: 유저↔시스템 또는 마이크로서비스 간 인터랙션에 사용
   - **ER Diagram (`erDiagram`)**: DB 스키마 시각화 및 데이터 관계에 사용
   - **State Diagram (`stateDiagram-v2`)**: 특정 엔티티의 상태 생명주기 추적에 사용 (예: 주문 상태)
3. **Mermaid 코드 생성**: 아래 문법 레퍼런스를 참고하여 올바른 구문으로 작성합니다.
4. **컨텍스트 제공**: 다이어그램 구조 선택 이유를 코드 하단에 간략히 설명합니다.

## 가이드라인

- 다이어그램은 단순하고 읽기 쉽게 유지합니다. 과도한 중첩을 피합니다.
- 노드와 엣지에 설명적인 레이블을 사용합니다.
- 구문이 유효한지 확인하여 사용자가 Mermaid 에디터([Mermaid Live Editor](https://mermaid.live/))에 바로 붙여넣을 수 있도록 합니다.
- VS Code에서 `Cmd + Shift + V`로 즉시 미리보기 가능합니다.

---

## Mermaid 문법 레퍼런스

### Flowchart
\`\`\`mermaid
graph TD
    A[Start] --> B{Is it true?}
    B -- Yes --> C[Correct]
    B -- No --> D[Incorrect]
\`\`\`

### Sequence Diagram
\`\`\`mermaid
sequenceDiagram
    participant User
    participant System
    User->>System: Request
    System-->>User: Response
\`\`\`

### Entity Relationship (ERD)
\`\`\`mermaid
erDiagram
    CUSTOMER ||--o{ ORDER : places
    ORDER ||--|{ LINE-ITEM : contains
\`\`\`

### State Diagram
\`\`\`mermaid
stateDiagram-v2
    [*] --> Idle
    Idle --> Moving : Key Pressed
    Moving --> Idle : Key Released
\`\`\`
