---
layout: post
title: "从 Cloud Agent Teams 到 Agent Harness / Infra"
date: 2026-07-09
author: Cindy / Jake
categories: [agent-harness, agent-infra, portfolio]
---

今天开始把 Cloud Agent Teams 里的真实工作，整理成一个公开的 Agent Harness / Agent Runtime Infra 作品集。写这篇不是为了做一个项目宣传页，而是为了把一天里的判断、机制和证据沉淀成后续可以反复打磨的技术研究笔记。

核心判断很简单：让 Agent 真正有用，不只是写 prompt 或接一个模型 API。一个真实 Agent 系统需要治理机制、运行时基础设施、证据链、恢复能力，以及证明“事情真的完成了”的方法。

<div class="toc">
  <h2>Table of Contents</h2>
  <ul>
    <li><a href="#问题">问题</a></li>
    <li><a href="#harness-层">Harness 层</a></li>
    <li><a href="#runtime-infra-层">Runtime Infra 层</a></li>
    <li><a href="#为什么这对面试有价值">为什么这对面试有价值</a></li>
    <li><a href="#接下来公开构建什么">接下来公开构建什么</a></li>
    <li><a href="#发布节奏">发布节奏</a></li>
    <li><a href="#第一批-failure-case">第一批 Failure Case</a></li>
    <li><a href="#参考">参考</a></li>
  </ul>
</div>

<div class="note">
  <strong>今天的输出：</strong>搭建公开 GitHub Pages 作品集；明确 Harness 与 Runtime Infra 的交叉定位；确定两个公开项目；把 failure case / benchmark / weekly release note 放进后续迭代节奏。
</div>

## 问题

大多数 Agent demo 停在 happy path：

1. 用户给一个任务；
2. Agent 调用一个工具；
3. demo 展示一个成功输出。

这对真实工程工作远远不够。

在真实团队里，Agent 要处理长任务、变化的上下文、不完整交接、review gate、secret、runtime state、失败部署和资源清理。它还必须说清楚：哪些已经覆盖，哪些没有覆盖。

这就是 Agent Harness 和 Agent Runtime Infra 的交叉点。

## Harness 层

Harness 层解决的是 Agent 行为和协作问题。

在 Cloud Agent Teams 里，最重要的机制包括：

- task ownership 和 claim-before-work；
- thread-level execution context；
- 汇报前做 memory/history preflight；
- subagent role split；
- PASS/BLOCK review language；
- 用 fresh readback 替代 stale assumption；
- 明确说明哪些没有测试；
- 面向 owner 的可核查 summary。

这和普通 chat wrapper 不一样。难点不是生成文本，而是让 Agent 在长流程里像可靠队友一样工作。

## Runtime Infra 层

Runtime Infra 层解决的是 Agent 如何真实跑起来。

我现在采用的拆分方式是：

| 层级 | 关注点 | 面试表达 |
| --- | --- | --- |
| Host / Carrier | Agent 跑在哪里，运行时载体如何创建和回收 | 我能把 Agent 从“记录”推进到“真实可运行载体” |
| Key / Route | 模型 key、route、gateway 绑定 | 我关注 secret 不泄露、路由可读回、成本/权限可控 |
| Record / Bind | 资源状态如何持久化 | 我不会只依赖进程内状态，而是做 readback 和 journal |
| Lifecycle | create / stop / start / delete | 我把生命周期拆成可验证步骤 |
| Runtime Ready | 是否真的能工作 | 我用 visible reply / smoke / readback 证明不是假绿 |
| Cleanup | 删除和 orphan=0 | 我把清理作为验收，不当作事后补丁 |

对于 create agent 流程，“created” 不应该只是数据库里有一行记录。它应该意味着：Agent 可见，有正确 runtime binding，能使用预期 model route，能 stop/start，能 delete，最后没有 orphan resource。

所以 `create -> visible -> delete -> orphan=0` 比单元测试绿更接近真实验收。

## 为什么这对面试有价值

如果面 Agent Harness 岗位，核心表达是：

> 我做的是让 Agent 在多步骤工程任务里可靠工作：context preflight、task ownership、subagent coordination、evidence-based reporting、review gate、failure recovery。

如果面 Agent Infra 岗位，核心表达是：

> 我做的是让 Agent 安全运行的 control plane 和 runtime path：carrier、route、secret handle、lifecycle、readback、rollback、cleanup。

最强的位置是两者交叉：

> 我既懂 Agent 应该如何协作，也懂它要可靠运行需要什么基础设施。

## 接下来公开构建什么

这个作品集先通过两个公开项目增长。

### mini-multi-agent-harness

最小 Agent Harness demo，目标是展示：

- planner / executor / reviewer roles；
- memory preflight；
- task ownership；
- tool call logs；
- PASS/BLOCK reports；
- fake-green detection；
- stale context 之后的恢复。

### agent-sandbox-control-plane

最小 Agent Runtime Control Plane demo，目标是展示：

- create / readback / stop / start / delete lifecycle；
- Host / Carrier abstraction；
- Key / Route binding；
- secret handle pattern；
- runtime-ready check；
- cleanup 和 orphan detection。

## 发布节奏

这个作品集不会等到完美再发布。

每周循环是：

1. 推进一个小项目更新；
2. 发布一个 failure case；
3. 更新一个 benchmark 或 evidence table；
4. 写一篇短技术笔记；
5. 把一道面试题改造成项目证据支撑的回答。

重点是展示迭代过程，而不是只展示一个最终 polished artifact。

| 每周产物 | 目的 |
| --- | --- |
| 一个项目更新 | 证明项目持续推进 |
| 一个 failure case | 证明我理解 Agent 失败模式 |
| 一个 benchmark / evidence 更新 | 证明不是主观描述 |
| 一篇短文 | 训练公开表达和面试表达 |
| 一道题的项目答案 | 把面试题转成自己的经历 |

## 第一批 Failure Case

第一批公开 failure case 应该来自真实多 Agent 协作：

- Agent 没重读 thread，基于 stale context 汇报；
- CI 绿，但 real runtime smoke 没覆盖；
- review stamp 不是 current head 的 fresh stamp；
- secret/route 看起来配置了，但 runtime readback 证明缺失；
- task ownership 不清，多个 Agent 重复劳动。

这些案例的价值在于：它们能解释为什么需要 Harness。

## 下一步

下一步是把这个仓库变成可持续增长的 evidence base：

- 加架构图；
- 加第一张 benchmark 表；
- 写 3 个 failure case；
- 做最小可运行 Harness demo；
- 做最小 Runtime Control Plane demo。

目标不是停留在名词，而是让这些能力通过真实 artifact 讲得清楚。

## 参考

- Lilian Weng, [Harness Engineering for Self-Improvement](https://lilianweng.github.io/posts/2026-07-04-harness/).
- Lilian Weng, [LLM Powered Autonomous Agents](https://lilianweng.github.io/posts/2023-06-23-agent/).
- Hugo PaperMod, [Features](https://github.com/adityatelange/hugo-PaperMod/wiki/Features).
- Jekyll, [Themes](https://jekyllrb.com/docs/themes/).
