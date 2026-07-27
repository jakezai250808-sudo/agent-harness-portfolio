---
layout: default
title: AI Engineering Portfolio
---

<section class="home-intro">
  <span class="tagline">AI Infra / Agent Runtime / Autonomous Systems</span>
  <h1>Engineering systems that survive the real world.</h1>
  <p>
    这里记录 AI 基础设施、Agent Runtime、自动驾驶与车联网数据平台的工程实践。
    关注的不只是 demo，而是部署、权限、隔离、可观测性、失败恢复和成本。
  </p>
  <p>
    <strong>方向：</strong>AI Infra / LLM Serving / Agent Runtime & Harness / 自动驾驶平台<br>
    <strong>地点：</strong>杭州 / 上海 / Remote
  </p>
  <p><a href="{{ site.baseurl }}/resume/"><strong>查看公开工程履历 →</strong></a></p>
</section>

<section class="section">
  <h2>Selected Work</h2>
  <div class="grid">
    <article class="card">
      <h3>AI Infrastructure</h3>
      <p>GPU 推理服务、模型兼容、网关路由、可观测性与稳定性工程。</p>
    </article>
    <article class="card">
      <h3>Agent Runtime</h3>
      <p>任务 ownership、工具与权限、运行时控制面、证据交付和失败恢复。</p>
      <a href="{{ site.baseurl }}/docs/architecture.html">Architecture notes</a>
    </article>
    <article class="card">
      <h3>Tesla Data SaaS</h3>
      <p>多租户车辆数据托管、Telemetry / Fleet API 接入、时序数据与隐私隔离。</p>
      <a href="{{ site.baseurl }}/resume/#tesla-车辆数据多租户-saas构建中">Project overview</a>
    </article>
  </div>
</section>

<section class="section">
  <h2>Projects</h2>
  <ul>
    <li><a href="{{ site.baseurl }}/projects/mini-multi-agent-harness/">mini-multi-agent-harness</a>：最小可运行 Harness demo。</li>
    <li><a href="{{ site.baseurl }}/projects/agent-sandbox-control-plane/">agent-sandbox-control-plane</a>：最小 Runtime Control Plane demo。</li>
    <li><a href="{{ site.baseurl }}/resume/">Public engineering profile</a>：脱敏的项目、工程能力与求职方向。</li>
  </ul>
</section>

<section class="section">
  <h2>Writing</h2>
  <ul class="post-list-clean">
    <li>
      <h3><a href="{{ site.baseurl }}{% post_url 2026-07-09-cloud-agent-teams-to-agent-harness-infra %}">从 Cloud Agent Teams 到 Agent Harness / Infra</a></h3>
      <span class="post-meta">July 9, 2026 · Agent Harness · Runtime Infra</span>
      <p>Agent 不是 prompt/chatbot；Harness 解决行为治理；Runtime Infra 解决真实运行。</p>
    </li>
  </ul>
</section>
