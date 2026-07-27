---
layout: default
title: AI 工程师简历
permalink: /resume/
description: AI Infra、LLM 推理平台与 Agent Runtime 方向的公开工程简历。
---

<article class="resume">
  <header class="resume-header">
    <div class="resume-kicker">AI ENGINEER · PUBLIC RESUME</div>
    <div class="resume-heading">
      <div>
        <h1>AI Infra / Agent Runtime 工程师</h1>
        <p class="resume-summary">4+ 年平台与后端工程经验，从 Java 平台工程延伸到大模型推理、Agent 工程化与自动驾驶部署。擅长把模型和 Agent 接入真实业务系统，补齐部署、治理、观测与恢复链路。</p>
      </div>
      <div class="resume-target">
        <span>求职方向</span>
        <strong>AI Infra</strong>
        <strong>LLM Serving</strong>
        <strong>Agent Runtime</strong>
      </div>
    </div>
    <div class="resume-meta">
      <span>杭州 / 上海 / Remote</span>
      <span>Java · Python · CUDA · ROS</span>
      <span>公开脱敏版</span>
    </div>
  </header>

  <section class="resume-section">
    <h2>核心优势</h2>
    <div class="signal-grid">
      <div><strong>百卡规模实践</strong><p>参与 GPU 推理与模型服务平台建设，覆盖服务入口、部署兼容和可观测性。</p></div>
      <div><strong>AI 工程闭环</strong><p>不止让模型“能跑”，也关注吞吐、延迟、权限、故障定位和恢复。</p></div>
      <div><strong>跨栈交付能力</strong><p>连接 Java 后端、Python 推理、CUDA/GPU、ROS 与数据链路。</p></div>
    </div>
  </section>

  <section class="resume-section">
    <div class="section-title-row">
      <h2>代表项目</h2>
      <span>按成熟度区分生产实践、工程验证与构建中</span>
    </div>

    <article class="resume-project" id="llm-serving">
      <div class="project-side">
        <span class="status production">生产实践</span>
        <span class="project-domain">AI INFRA</span>
      </div>
      <div class="project-main">
        <h3>GPU 推理与模型服务平台</h3>
        <p class="project-brief">面向多模型和百卡规模 GPU 资源，建设统一、可观察、可治理的推理服务能力。</p>
        <ul>
          <li>以 vLLM、LiteLLM、Nginx 组织兼容 OpenAI API 的统一服务入口，覆盖模型路由、健康检查、访问控制与降级。</li>
          <li>处理 CUDA、驱动、Transformers 和模型架构的兼容矩阵，把排障经验固化为镜像、版本约束与部署规范。</li>
          <li>通过 DCGM Exporter、Prometheus、Grafana 建立 GPU、请求和服务级指标，支持容量判断与故障定位。</li>
          <li>围绕吞吐、首 Token 延迟、显存利用率、缓存命中率和恢复时间评估服务，而非只验证进程存活。</li>
        </ul>
        <div class="result"><b>价值</b> 将零散模型部署沉淀为可复用的内部平台能力。</div>
        <div class="tech-tags"><span>vLLM</span><span>LiteLLM</span><span>CUDA</span><span>Docker</span><span>Prometheus</span></div>
      </div>
    </article>

    <article class="resume-project" id="agent-runtime">
      <div class="project-side">
        <span class="status prototype">工程验证</span>
        <span class="project-domain">AGENT SYSTEM</span>
      </div>
      <div class="project-main">
        <h3>Fleet-to-PR / Coding Agent 工程平台</h3>
        <p class="project-brief">面向 Coding Agent 长流程中的上下文过期、重复执行、验证失真和资源残留问题，设计可追踪的交付闭环。</p>
        <ul>
          <li>组织任务拆分、ownership、上下文预检、工具调用、执行记录、验证结果与交付证据。</li>
          <li>设计 PASS / BLOCK gate，区分生成完成、CI 通过、评审通过、契约满足和真实运行通过。</li>
          <li>针对 stale context、失败 handoff、重复执行与中断恢复建立显式状态和恢复路径。</li>
          <li>将运行时资源、密钥句柄、路由绑定、readback 与生命周期抽象为 control plane 能力。</li>
        </ul>
        <div class="result"><b>判断</b> Harness 约束 Agent 行为，Runtime Control Plane 承载真实运行，二者共同决定 Agent 能否工程交付。</div>
        <div class="project-links"><a href="{{ site.baseurl }}/docs/architecture.html">架构</a><a href="{{ site.baseurl }}/cases/failure-cases.html">失败案例</a><a href="{{ site.baseurl }}/docs/benchmark.html">评测</a></div>
        <div class="tech-tags"><span>Agent Harness</span><span>Multi-Agent</span><span>Tool Governance</span><span>Control Plane</span></div>
      </div>
    </article>

    <article class="resume-project" id="autonomous-driving">
      <div class="project-side">
        <span class="status production">工程实践</span>
        <span class="project-domain">AUTONOMOUS</span>
      </div>
      <div class="project-main">
        <h3>自动驾驶感知与部署链路</h3>
        <p class="project-brief">在算法、GPU 环境和机器人中间件之间完成多传感器模型部署，并定位跨层问题。</p>
        <ul>
          <li>参与 LiDAR、图像与 BEV 融合模型的部署集成，覆盖检测、分割与 Occupancy 等任务。</li>
          <li>处理多模型并行、GPU 资源、ROS 进程和消息链路，结合 Foxglove、RViz 与日志指标排障。</li>
          <li>使用 torchrun、DDP、NCCL 支持训练和多卡运行，关注数据、模型与运行环境的一致性。</li>
        </ul>
        <div class="tech-tags"><span>BEV</span><span>ROS / ROS2</span><span>PyTorch</span><span>DDP</span><span>NCCL</span></div>
      </div>
    </article>

    <article class="resume-project" id="tesla-saas">
      <div class="project-side">
        <span class="status building">构建中</span>
        <span class="project-domain">SAAS PRODUCT</span>
      </div>
      <div class="project-main">
        <h3>Tesla 车辆数据多租户 SaaS</h3>
        <p class="project-brief">面向非开发者车主的 TeslaMate 兼容托管服务，探索共享托管与独享部署两种交付模式。</p>
        <ul>
          <li>设计 Telemetry、Owner API、Fleet API 多通道接入与迁移路径，降低上游接口变化风险。</li>
          <li>围绕车辆状态机、事件流、时序数据、MQTT 与只读兼容接口划分服务边界。</li>
          <li>把租户隔离、凭证安全、最小权限、审计和数据生命周期作为基础约束。</li>
          <li>同时用留存、续费、毛利和支持成本验证产品的商业可持续性。</li>
        </ul>
        <div class="result"><b>状态</b> 正在构建与验证；当前展示已形成的系统设计，不将规划包装为上线成果。</div>
        <div class="tech-tags"><span>Java</span><span>Spring Cloud</span><span>Multi-Tenant SaaS</span><span>MQTT</span><span>Time-Series Data</span></div>
      </div>
    </article>
  </section>

  <section class="resume-section">
    <h2>技术栈</h2>
    <div class="skill-rows">
      <div><strong>AI Serving</strong><span>vLLM · LiteLLM · PyTorch · CUDA · Transformers</span></div>
      <div><strong>Agent Systems</strong><span>Agent Harness · Tool Calling · MCP · Runtime Isolation · Control Plane</span></div>
      <div><strong>Backend & Platform</strong><span>Java · Spring Cloud · Python · FastAPI · Docker · Nginx · GitHub Actions</span></div>
      <div><strong>Observability</strong><span>DCGM Exporter · Prometheus · Grafana · Sentry</span></div>
      <div><strong>Autonomous Driving</strong><span>ROS / ROS2 · BEV · DDP · NCCL · Foxglove · RViz</span></div>
    </div>
  </section>

  <footer class="resume-note">本页为公开脱敏简历，只展示求职方向、工程能力与项目证据，不包含联系方式、薪资及雇主内部信息。</footer>
</article>
