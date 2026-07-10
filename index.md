---
layout: default
title: Agent Harness Portfolio
---

<section class="hero">
  <span class="tagline">Agent Harness / Runtime Infra / Interview Evidence</span>
  <h1>把真实多 Agent 工程协作，沉淀成可展示、可面试、可持续迭代的作品集。</h1>
  <p>
    这里不是 chatbot demo，而是围绕 Agent 如何可靠工作来组织：任务 ownership、history preflight、subagent 分工、
    PASS/BLOCK gate、runtime lifecycle、readback、rollback 和 orphan cleanup。
  </p>
  <div class="actions">
    <a class="button primary" href="{{ site.baseurl }}{% post_url 2026-07-09-cloud-agent-teams-to-agent-harness-infra %}">阅读第一篇文章</a>
    <a class="button" href="{{ site.baseurl }}/projects/mini-multi-agent-harness/">Harness 项目</a>
    <a class="button" href="{{ site.baseurl }}/projects/agent-sandbox-control-plane/">Infra 项目</a>
  </div>
</section>
<section class="section">
  <h2>当前定位</h2>
  <div class="grid">
    <article class="card">
      <h3>Agent Harness</h3>
      <p>让 Agent 在长任务、多角色、多工具、多上下文里可靠执行，而不是只生成回答。</p>
      <a href="{{ site.baseurl }}/docs/architecture.html">看架构拆分</a>
    </article>
    <article class="card">
      <h3>Agent Runtime Infra</h3>
      <p>把 create/start/stop/delete、secret、route、carrier、readback 和 cleanup 变成可验证流程。</p>
      <a href="{{ site.baseurl }}/projects/agent-sandbox-control-plane/">看控制面项目</a>
    </article>
    <article class="card">
      <h3>Interview Evidence</h3>
      <p>把真实 failure case、benchmark、PR/review/readback 证据转成面试能讲清楚的材料。</p>
      <a href="{{ site.baseurl }}/cases/failure-cases.html">看 failure cases</a>
    </article>
  </div>
</section>

<section class="section">
  <h2>第一篇文章</h2>
  <div class="evidence">
    <h3><a href="{{ site.baseurl }}{% post_url 2026-07-09-cloud-agent-teams-to-agent-harness-infra %}">从 Cloud Agent Teams 到 Agent Harness / Infra</a></h3>
    <p>
      今天的文章先把主线讲清楚：Agent 不是 prompt/chatbot；Harness 解决行为治理；
      Runtime Infra 解决真实运行；面试表达要站在两者交叉层。
    </p>
  </div>
</section>

<section class="section">
  <h2>两个公开项目</h2>
  <div class="grid">
    <article class="card">
      <h3>mini-multi-agent-harness</h3>
      <p>最小可运行 Harness：planner / executor / reviewer、memory preflight、PASS/BLOCK、fake-green detector。</p>
      <a href="{{ site.baseurl }}/projects/mini-multi-agent-harness/">打开项目说明</a>
    </article>
    <article class="card">
      <h3>agent-sandbox-control-plane</h3>
      <p>最小 Runtime Control Plane：Host/Carrier、Key/Route、Record/Bind、Lifecycle、Runtime Ready。</p>
      <a href="{{ site.baseurl }}/projects/agent-sandbox-control-plane/">打开项目说明</a>
    </article>
  </div>
</section>

<section class="section">
  <h2>下一轮迭代</h2>
  <div class="evidence">
    <ul>
      <li>补一张 Harness + Runtime Control Plane 架构图。</li>
      <li>写 3 个真实 failure case：stale context、假绿、runtime readback 缺失。</li>
      <li>把 benchmark 表从计划改成第一版数据结构。</li>
      <li>把两个项目 README 从 v0.1 提升到可执行 v0.2。</li>
    </ul>
  </div>
</section>
