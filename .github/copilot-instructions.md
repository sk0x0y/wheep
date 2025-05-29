## Core Rules

You have two modes of operation:

1. Plan mode - You will work with the user to define a plan, you will gather all the information you need to make the changes but will not make any changes
2. Act mode - You will make changes to the codebase based on the plan

- You start in plan mode and will not move to act mode until the plan is approved by the user.
- You will print `# Mode: PLAN` when in plan mode and `# Mode: ACT` when in act mode at the beginning of each response.
- Unless the user explicity asks you to move to act mode, by typing `ACT` you will stay in plan mode.
- You will move back to plan mode after every response and when the user types `PLAN`.
- If the user asks you to take an action while in plan mode you will remind them that you are in plan mode and that they need to approve the plan first.
- When in plan mode always output the full updated plan in every response.

## 다음 MCP 서버 사용 규칙 지침을 준수하십시오:

1.  **Git 커밋 메시지**: 커밋 메시지 생성 요청 시, 반드시 `commit-convention-mcp` MCP 서버를 사용하고 다음 작업 순서를 따르십시오. 이는 Git 관련 명령의 원활한 실행을 보장합니다:
    a. `get_commit_message_prompt`를 사용하여 해당 서버의 프롬프트 리소스를 가져옵니다. 이 프롬프트는 커밋 메시지 생성의 **기준**이 됩니다.
    b. 가져온 프롬프트를 확인하여, 커밋 메시지 생성을 위해 특정 `git` 명령어(예: `git diff`, `git diff --staged`) 실행 결과가 **명시적으로 요구되는지** 확인합니다.
    c. 프롬프트에서 특정 `git` 명령어 실행 결과가 필요하다고 명시된 경우, **프롬프트에 지정된 정확한 명령어**를 실행하여 변경사항을 가져옵니다. (사용자에게 어떤 명령어를 사용할지 묻지 않습니다.)
    d. 가져온 프롬프트 템플릿과 (프롬프트 요구 시) 실행된 `git` 명령어 결과를 사용하여 최종 커밋 메시지를 생성합니다. 예를 들어, 프롬프트 내의 `{{diff}}`와 같은 플레이스홀더를 가져온 `git diff` 결과로 대체할 수 있습니다.
