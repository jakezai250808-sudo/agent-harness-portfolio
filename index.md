---
layout: default
title: Agent Harness Portfolio
---

<section class="home-intro">
  <span class="tagline">Agent Harness / Runtime Infra / Interview Evidence</span>
  <h1>Agent Harness Portfolio</h1>
  <p>
    这里记录我把 Cloud Agent Teams / Raft 多 Agent 协作经验，沉淀成 Agent Harness 与 Agent Runtime Infra 作品集的过程。
  </p>
  <p>
    风格目标是长期技术研究笔记：少一点宣传页，多一点问题定义、机制拆解、failure case、benchmark 和可核查证据。
  </p>
</section>
<section class="section">
  <h2>Posts</h2>
  <ul class="post-list-clean">
    <li>
      <h3><a href="{{ site.baseurl }}{% post_url 2026-07-09-cloud-agent-teams-to-agent-harness-infra %}">从 Cloud Agent Teams 到 Agent Harness / Infra</a></h3>
      <span class="post-meta">Date: July 9, 2026 | Topic: Agent Harness, Runtime Infra</span>
      <p>第一篇把主线讲清楚：Agent 不是 prompt/chatbot；Harness 解决行为治理；Runtime Infra 解决真实运行；面试表达要站在两者交叉层。</p>
    </li>
  </ul>
</section>

<section class="section">
  <h2>Research Tracks</h2>
  <div class="grid">
    <article class="card">
      <h3>Harness Engineering</h3>
      <p>任务 ownership、history preflight、subagent 分工、PASS/BLOCK gate、fresh readback。</p>
      <a href="{{ site.baseurl }}/docs/architecture.html">Architecture notes</a>
    </article>
    <article class="card">
      <h3>Runtime Control Plane</h3>
      <p>Host/Carrier、Key/Route、Record/Bind、Lifecycle、Runtime Ready、cleanup。</p>
      <a href="{{ site.baseurl }}/projects/agent-sandbox-control-plane/">Control-plane project</a>
    </article>
    <article class="card">
      <h3>Evidence & Interview</h3>
      <p>把真实 failure case、benchmark、PR/readback 证据转成面试可表达材料。</p>
      <a href="{{ site.baseurl }}/cases/failure-cases.html">Failure cases</a>
    </article>
  </div>
</section>

<section class="section">
  <h2>Projects</h2>
  <ul>
    <li><a href="{{ site.baseurl }}/projects/mini-multi-agent-harness/">mini-multi-agent-harness</a>：最小可运行 Harness demo。</li>
    <li><a href="{{ site.baseurl }}/projects/agent-sandbox-control-plane/">agent-sandbox-control-plane</a>：最小 Runtime Control Plane demo。</li>
  </ul>
</section>

<section class="section">
  <h2>Next Iteration</h2>
  <ul>
    <li>把第一篇改成更完整的研究笔记：摘要、目录、参考、图表。</li>
    <li>补 Harness + Runtime Control Plane 架构图。</li>
    <li>写 3 个真实 failure case。</li>
    <li>把 benchmark 从计划升级为第一版表格。</li>
  </ul>
</section>
