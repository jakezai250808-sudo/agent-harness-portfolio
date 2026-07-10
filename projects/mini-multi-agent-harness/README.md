# mini-multi-agent-harness

目标：做一个最小可运行的 Agent Harness demo，展示多个 Agent 如何围绕真实工程任务协作。

## v0.1 Scope

- planner / executor / reviewer roles;
- task ownership;
- memory/history preflight;
- tool call log;
- PASS/BLOCK report;
- fake-green detector;
- recovery note when context is stale.

## Interview Value

这个项目服务 Agent Harness 面试：它要证明 Agent reliability 是系统设计问题，不只是 prompt 设计问题。

## Next

- 设计任务状态机。
- 加入最小 memory preflight。
- 输出第一版 PASS/BLOCK 报告样例。
