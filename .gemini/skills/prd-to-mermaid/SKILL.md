---
name: prd-to-mermaid
description: Analyze PRDs or business requirements and generate professional Mermaid.js diagrams (Flowcharts, Sequence, ERD). Use this skill whenever the user provides a product specification and requests a visual representation of logic or architecture.
---

# PRD-to-Mermaid Skill

## Workflow

1.  **Analyze the Input**: Identify the key actors, processes, and data structures in the provided PRD or requirement text.
2.  **Select the Best Diagram Type**:
    *   **Flowchart (graph TD)**: Use for business logic, user flows, and decision-making processes.
    *   **Sequence Diagram**: Use for interactions between a user and a system, or between multiple microservices.
    *   **ER Diagram (erDiagram)**: Use for database schema visualization and data relationships.
    *   **State Diagram**: Use for tracking the lifecycle of a specific entity (e.g., Order Status: Pending -> Paid -> Shipped).
3.  **Generate Mermaid Code**: Refer to [mermaid_guide.md](references/mermaid_guide.md) for correct syntax.
4.  **Provide context**: Explain the reasoning behind the diagram structure briefly after generating the code.

## Guidelines

- Keep diagrams simple and readable. Avoid overly complex nesting.
- Use descriptive labels for nodes and edges.
- Ensure the syntax is valid so the user can paste it into a Mermaid editor (like [Mermaid Live Editor](https://mermaid.live/)).
