---
layout: default
title: AI 系统工程师简历
permalink: /resume/
description: 大模型推理、Agent Infra 与机器人 AI 系统方向的公开工程简历。
---

<article class="resume">
  <header class="resume-header">
    <div class="resume-kicker">AI SYSTEMS ENGINEER · HANGZHOU</div>
    <div class="resume-heading">
      <div>
        <h1>AI 系统工程师｜大模型推理 × Agent Infra × 机器人部署</h1>
        <p class="resume-summary">4+ 年平台与后端工程经验，长期处理 AI 从模型代码进入真实系统后的难题：GPU 环境与推理服务、Agent 长任务运行时、ROS/多传感器模型部署，以及跨组件故障定位。能够在算法、平台和业务之间完成工程闭环。</p>
      </div>
      <div class="resume-target">
        <span>目标岗位</span>
        <strong>AI Infra / LLM Serving</strong>
        <strong>Agent Infra / Runtime</strong>
        <strong>机器人 AI 平台</strong>
      </div>
    </div>
    <div class="resume-meta">
      <span>杭州优先 · 上海 / Remote</span>
      <span>Java · Python · CUDA · ROS</span>
      <span>4+ 年平台工程</span>
    </div>
  </header>

  <section class="resume-section">
    <h2>为什么值得进一步聊</h2>
    <div class="signal-grid">
      <div><strong>做过真实规模</strong><p>参与百卡规模 GPU 推理与模型服务平台，不止停留在单机 Demo 和 API 封装。</p></div>
      <div><strong>能跨越模型与系统</strong><p>连接 Python/PyTorch、CUDA/GPU、Java 后端、容器、监控与 ROS 运行链路。</p></div>
      <div><strong>关注失败路径</strong><p>把兼容性、超时、降级、状态回读、故障恢复和交付证据作为系统的一部分。</p></div>
    </div>
  </section>

  <section class="resume-section">
    <div class="section-title-row">
      <h2>目标团队匹配</h2>
      <span>用已验证的工程能力回应岗位要求</span>
    </div>
    <div class="skill-rows">
      <div><strong>大模型系统 / AI Infra</strong><span>多模型统一服务、推理吞吐与延迟、GPU 可观测性、版本兼容、健康检查与故障降级</span></div>
      <div><strong>Agent Infra / AI Coding</strong><span>任务状态机、工具调用治理、上下文预检、执行隔离、PASS / BLOCK 验证与失败恢复</span></div>
      <div><strong>具身智能 / 机器人平台</strong><span>感知模型部署、ROS 消息链路、多模型 GPU 运行、仿真与现场观测、云端平台能力</span></div>
    </div>
  </section>

  <section class="resume-section">
    <div class="section-title-row">
      <h2>代表项目</h2>
      <span>生产实践、工程验证与构建中明确区分</span>
    </div>

    <article class="resume-project" id="llm-serving">
      <div class="project-side">
        <span class="status production">生产实践</span>
        <span class="project-domain">AI INFRA</span>
      </div>
      <div class="project-main">
        <h3>百卡规模 GPU 推理与模型服务平台</h3>
        <p class="project-brief">面向多模型、异构 GPU 与多团队使用场景，把零散部署收敛为统一、可观察、可治理的推理服务能力。</p>
        <ul>
          <li>基于 vLLM、LiteLLM、Nginx 建设兼容 OpenAI API 的统一入口，覆盖模型路由、健康检查、访问控制与故障降级。</li>
          <li>处理 CUDA、驱动、Transformers、量化方案和模型架构的兼容矩阵，将排障经验固化为镜像、版本约束与部署规范。</li>
          <li>通过 DCGM Exporter、Prometheus、Grafana 建立 GPU、请求和服务指标，支持容量判断、异常定位与恢复。</li>
          <li>以吞吐、首 Token 延迟、显存利用率、缓存命中率和恢复时间评价服务质量，而非只验证进程存活。</li>
        </ul>
        <div class="result"><b>技术信号</b> 具备从模型运行、GPU 环境到服务治理和平台观测的完整视角，可继续深入分布式推理、调度与性能优化。</div>
        <div class="tech-tags"><span>vLLM</span><span>LiteLLM</span><span>PyTorch</span><span>CUDA</span><span>Docker</span><span>Prometheus</span></div>
      </div>
    </article>

    <article class="resume-project" id="agent-runtime">
      <div class="project-side">
        <span class="status prototype">工程验证</span>
        <span class="project-domain">AGENT INFRA</span>
      </div>
      <div class="project-main">
        <h3>Fleet-to-PR / Coding Agent 工程平台</h3>
        <p class="project-brief">面向 Coding Agent 长流程中的上下文过期、重复执行、验证失真和资源残留，设计可追踪、可恢复的交付闭环。</p>
        <ul>
          <li>组织任务拆分、ownership、上下文预检、工具调用、执行记录、验证结果与交付证据。</li>
          <li>设计 PASS / BLOCK gate，区分“生成完成”、CI 通过、评审通过、契约满足和真实运行通过。</li>
          <li>针对 stale context、失败 handoff、重复执行与中断恢复建立显式状态、幂等边界和恢复路径。</li>
          <li>将运行时资源、密钥句柄、路由绑定、readback 与生命周期抽象为 control plane 能力。</li>
        </ul>
        <div class="result"><b>技术判断</b> Harness 约束 Agent 行为，Runtime Control Plane 承载真实运行；模型能力之外，状态、权限、环境与验证决定 Agent 能否持续交付。</div>
        <div class="project-links"><a href="{{ site.baseurl }}/docs/architecture.html">架构</a><a href="{{ site.baseurl }}/cases/failure-cases.html">失败案例</a><a href="{{ site.baseurl }}/docs/benchmark.html">评测</a></div>
        <div class="tech-tags"><span>Agent Harness</span><span>Multi-Agent</span><span>Tool Governance</span><span>Control Plane</span><span>MCP</span></div>
      </div>
    </article>

    <article class="resume-project" id="autonomous-driving">
      <div class="project-side">
        <span class="status production">工程实践</span>
        <span class="project-domain">EMBODIED AI</span>
      </div>
      <div class="project-main">
        <h3>自动驾驶感知与机器人运行链路</h3>
        <p class="project-brief">在感知算法、GPU 环境、机器人中间件与真实设备之间完成多传感器模型部署，处理实验环境之外的跨层问题。</p>
        <ul>
          <li>参与 LiDAR、图像与 BEV 融合模型的部署集成，覆盖检测、分割与 Occupancy 等任务。</li>
          <li>组织多模型并行、GPU 资源、ROS 进程和消息链路，使用 Foxglove、RViz、日志与指标定位现场问题。</li>
          <li>使用 torchrun、DDP、NCCL 支持训练与多卡运行，关注数据、模型、依赖和运行环境的一致性。</li>
          <li>能够与算法、平台和设备侧协作，将“模型效果问题”拆解为数据、算子、资源、消息或系统生命周期问题。</li>
        </ul>
        <div class="result"><b>具身方向价值</b> 已具备模型上机器人、ROS 链路与 GPU 平台的交叉经验，适合承担机器人 AI 基础设施、模型部署平台和系统集成角色。</div>
        <div class="tech-tags"><span>BEV</span><span>ROS / ROS2</span><span>PyTorch</span><span>DDP</span><span>NCCL</span><span>Foxglove</span></div>
      </div>
    </article>

    <article class="resume-project" id="tesla-saas">
      <div class="project-side">
        <span class="status building">构建中</span>
        <span class="project-domain">AI-NATIVE SAAS</span>
      </div>
      <div class="project-main">
        <h3>Tesla 车辆数据多租户 SaaS</h3>
        <p class="project-brief">面向非开发者车主的 TeslaMate 兼容托管服务，以产品方式验证设备数据接入、流式状态、租户隔离和低成本交付。</p>
        <ul>
          <li>设计 Telemetry、Owner API、Fleet API 多通道接入与迁移路径，降低上游接口变化风险。</li>
          <li>围绕车辆状态机、事件流、时序数据、MQTT 与只读兼容接口划分服务边界。</li>
          <li>把租户隔离、凭证安全、最小权限、审计和数据生命周期作为基础约束。</li>
          <li>同时用留存、续费、毛利和支持成本验证产品，而不是只完成技术原型。</li>
        </ul>
        <div class="result"><b>状态</b> 正在构建与验证；公开内容仅陈述已形成的系统设计，不将规划包装为上线成果。</div>
        <div class="tech-tags"><span>Java</span><span>Spring Cloud</span><span>MQTT</span><span>Multi-Tenant SaaS</span><span>Time-Series Data</span></div>
      </div>
    </article>
  </section>

  <section class="resume-section">
    <h2>技术能力地图</h2>
    <div class="skill-rows">
      <div><strong>LLM Serving</strong><span>vLLM · LiteLLM · PyTorch · CUDA · Transformers · 量化部署</span></div>
      <div><strong>Agent Systems</strong><span>Agent Harness · Tool Calling · MCP · Runtime Isolation · Control Plane</span></div>
      <div><strong>Backend & Platform</strong><span>Java · Spring Cloud · Python · FastAPI · Docker · Nginx · GitHub Actions</span></div>
      <div><strong>Observability</strong><span>DCGM Exporter · Prometheus · Grafana · Sentry</span></div>
      <div><strong>Robotics</strong><span>ROS / ROS2 · BEV · Multi-Sensor Fusion · DDP · NCCL · Foxglove · RViz</span></div>
    </div>
  </section>

  <section class="resume-section">
    <h2>希望解决的问题</h2>
    <div class="signal-grid">
      <div><strong>推理效率与稳定性</strong><p>让模型在真实资源、真实流量和复杂依赖下稳定运行，并持续改善性能。</p></div>
      <div><strong>Agent 可控交付</strong><p>让长任务 Agent 有状态、有权限边界、有验证证据，也能从失败中恢复。</p></div>
      <div><strong>模型进入物理世界</strong><p>连接训练、部署、ROS、设备与云平台，使机器人能力成为可迭代的产品系统。</p></div>
    </div>
  </section>

  <footer class="resume-note">公开脱敏版｜不包含联系方式、薪资及雇主内部信息。项目规模采用不泄露内部细节的概括表达。</footer>
</article>
