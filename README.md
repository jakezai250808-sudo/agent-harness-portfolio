# Agent Harness Portfolio

这个仓库用于沉淀 Agent Harness / Agent Runtime Infra 方向的公开作品集、博客和面试证据。

核心围绕三条线：

1. **Agent Harness**：多 Agent 任务 ownership、memory/history preflight、subagent 分工、证据化汇报、PASS/BLOCK gate、失败恢复。
2. **Agent Runtime Infra**：control plane、Host/Carrier、Key/Route、Record/Bind、Runtime Ready、secret handle、gateway/MCP 路由、readback、rollback、orphan cleanup。
3. **Interview Evidence**：failure case、benchmark、架构笔记、每周文章，把真实工程经历转成面试可表达材料。

## Projects

- [mini-multi-agent-harness](projects/mini-multi-agent-harness/README.md)
- [agent-sandbox-control-plane](projects/agent-sandbox-control-plane/README.md)

## Blog

博客通过 GitHub Pages 发布。

第一篇文章：

- [2026-07-09: 从 Cloud Agent Teams 到 Agent Harness / Infra](./_posts/2026-07-09-cloud-agent-teams-to-agent-harness-infra.md)

## Operating Principle

目标不是展示一个 chatbot demo，而是展示 Agent 如何在真实工程流程里可靠工作：

- 行动前读取正确上下文；
- 先 claim 再执行；
- 有明确工具和权限边界；
- 用证据汇报，而不是靠感觉；
- 区分 CI pass、review pass、contract pass 和 real runtime smoke；
- 能从 stale context 和失败 handoff 中恢复；
- 能清理资源并证明 orphan count 为 0。
