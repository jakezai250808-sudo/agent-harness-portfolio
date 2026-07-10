# agent-sandbox-control-plane

目标：做一个最小 Agent Runtime Control Plane demo。

## v0.1 Scope

- create / readback / stop / start / delete lifecycle;
- Host / Carrier abstraction;
- Key / Route binding;
- Record / Bind state;
- Runtime Ready check;
- cleanup and orphan=0 verification.

## Interview Value

这个项目服务 Agent Infra 面试：它要证明一个 Agent 从创建、可见、运行、停止、恢复、删除到清理的完整资源生命周期。

## Next

- 定义本地 fake provider。
- 定义 lifecycle journal。
- 写 create -> visible -> delete -> orphan=0 的最小 smoke。
