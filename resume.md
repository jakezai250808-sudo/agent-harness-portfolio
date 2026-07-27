---
layout: page
title: Engineering Profile
permalink: /resume/
---

<div class="profile-hero">
  <span class="eyebrow">PUBLIC ENGINEERING PROFILE</span>
  <h1>把 AI 模型和 Agent 变成可运行、可治理、可恢复的工程系统</h1>
  <p class="profile-lead">4+ 年平台与后端工程经验，主线聚焦 <strong>AI Infra / LLM Serving / Agent Runtime</strong>；具备自动驾驶感知部署与车联网数据平台实践。</p>
  <div class="profile-meta">
    <span>📍 杭州 / 上海 / Remote</span>
    <span>🎯 AI Infra · Agent Runtime · 平台后端</span>
  </div>
</div>

<div class="quick-scan">
  <div><strong>百卡规模</strong><span>GPU 推理与模型服务</span></div>
  <div><strong>端到端</strong><span>从部署、网关到可观测性</span></div>
  <div><strong>生产导向</strong><span>权限、恢复、成本与验证</span></div>
</div>

## 一分钟了解我

我的核心能力不是训练某一个模型，而是补齐模型和 Agent 进入真实环境后的工程链路：

- **让模型服务稳定运行**：处理 GPU 资源、模型兼容、推理入口、流量路由、监控告警与故障定位。
- **让 Agent 的结果可以相信**：设计任务 ownership、工具权限、运行时隔离、PASS / BLOCK gate、状态回读和失败恢复。
- **连接算法与业务系统**：以 Java / Spring Cloud 为主干，结合 Python、CUDA、ROS、消息与时序数据系统完成工程交付。

> 当前首选岗位：**AI Infra / LLM Serving / Agent Runtime**。自动驾驶平台、AI 平台后端也是高度匹配方向。

## 代表性工程

<section class="project-block" id="llm-serving">
<div class="project-title">
  <h3>GPU 推理与模型服务平台</h3>
  <span class="status production">生产实践</span>
</div>

**问题**：多类模型运行在百卡规模 GPU 集群上，模型架构、CUDA/驱动和依赖组合复杂；“能启动”并不等于能稳定提供服务。

**我负责的工程链路**

- 使用 vLLM、LiteLLM 与 Nginx 组织兼容 OpenAI API 的统一入口，覆盖模型路由、健康检查、访问控制和降级。
- 处理 CUDA、驱动、Transformers 与模型架构之间的兼容矩阵，把排障结论固化为镜像、版本约束和部署规范。
- 以 DCGM Exporter、Prometheus、Grafana 建立 GPU、请求与服务级指标，支持容量判断与故障定位。
- 持续关注吞吐、首 Token 延迟、显存利用率、缓存命中和恢复时间，而不是只验证进程是否存活。

**工程价值**：把零散模型部署转化为可复用、可观察、可治理的服务能力。

<div class="stack-line">vLLM · LiteLLM · CUDA · Docker · Nginx · Prometheus · Grafana</div>
</section>

<section class="project-block" id="agent-runtime">
<div class="project-title">
  <h3>Fleet-to-PR / Coding Agent 工程平台</h3>
  <span class="status prototype">原型与工程验证</span>
</div>

**问题**：Coding Agent 会生成代码，但长流程中容易出现上下文过期、重复执行、验证失真、资源残留和“看似完成”。

**我设计的关键机制**

- 把任务拆分、ownership、上下文预检、工具调用、执行记录、验证结果和交付证据组织成可追踪流程。
- 设计 PASS / BLOCK gate，区分“生成完成、CI 通过、评审通过、契约满足、真实运行通过”。
- 针对 stale context、失败 handoff、重复执行与中断恢复设计显式状态和恢复路径。
- 将运行时资源、密钥句柄、路由绑定、readback 与生命周期抽象为 control plane 能力。

**工程判断**：Agent Harness 负责约束行为，Runtime Control Plane 负责承载真实运行；二者共同决定 Agent 能否从 demo 走向工程交付。

<div class="evidence-links">
  <a href="{{ site.baseurl }}/docs/architecture.html">架构笔记 →</a>
  <a href="{{ site.baseurl }}/cases/failure-cases.html">失败案例 →</a>
  <a href="{{ site.baseurl }}/docs/benchmark.html">评测维度 →</a>
</div>

<div class="stack-line">Agent Harness · Multi-Agent · Tool Governance · Runtime Isolation · Control Plane</div>
</section>

<section class="project-block" id="autonomous-driving">
<div class="project-title">
  <h3>自动驾驶感知与部署链路</h3>
  <span class="status production">工程实践</span>
</div>

**问题**：多传感器模型进入车辆或场景后，故障可能来自数据、模型、GPU 环境、进程组织或 ROS 消息链路。

- 参与 LiDAR、图像与 BEV 融合模型的部署和集成，覆盖检测、分割、占用等任务。
- 处理多模型并行、GPU 资源、ROS 进程与消息链路，并通过 Foxglove、RViz 和日志指标定位问题。
- 使用 torchrun / DDP / NCCL 处理训练和多卡运行，关注数据、模型与运行环境的一致性。

**工程价值**：能够在算法、推理环境和机器人中间件之间定位跨层问题。

<div class="stack-line">BEV · Sensor Fusion · ROS / ROS2 · PyTorch · DDP · NCCL · Foxglove</div>
</section>

<section class="project-block" id="tesla-saas">
<div class="project-title">
  <h3>Tesla 车辆数据多租户 SaaS</h3>
  <span class="status building">构建中</span>
</div>

**目标**：为非开发者车主提供兼容 TeslaMate 生态的低成本托管服务，并保留共享托管与独享部署。

**已经形成的系统设计**

- Telemetry、Owner API、Fleet API 多通道接入与迁移路径，降低上游接口变化造成的单点风险。
- 围绕车辆状态机、事件流、时序数据、MQTT、只读兼容接口划分服务边界。
- 把租户隔离、凭证安全、最小权限、审计和数据生命周期设为基础约束。
- 以共享基础设施、分层存储和资源配额控制单位成本；以独享实例覆盖高隐私诉求。
- 在技术之外，用留存、续费、毛利与支持成本验证它是否是一门可持续的 SaaS 生意。

**状态说明**：该项目仍处于构建与验证阶段；这里展示的是已完成的架构判断，不把规划表述成上线成果。

<div class="stack-line">Java · Spring Cloud · Multi-Tenant SaaS · TeslaMate · MQTT · Time-Series Data</div>
</section>

## 技术能力地图

| 领域 | 能力与技术 |
|---|---|
| AI Serving | vLLM、LiteLLM、PyTorch、CUDA、Transformers、模型兼容与性能指标 |
| Agent Systems | Agent Harness、Tool Calling、MCP、Runtime Isolation、Control Plane |
| Backend | Java、Spring Cloud、Python、FastAPI、REST、SSE、事件驱动 |
| Platform | Docker、Nginx、GitHub Actions、Linux、Prometheus、Grafana |
| Autonomous Driving | ROS / ROS2、BEV、DDP、NCCL、Foxglove、RViz |
| Data & SaaS | PostgreSQL、SQLite、MQTT、时序数据、多租户、成本治理 |

## 我的工程取向

我更关心系统能否在真实环境中长期运行：上游变化时能否迁移，Agent 失败时能否恢复，GPU 服务异常时能否定位，多租户数据是否真正隔离，以及成本是否允许产品持续经营。

这是一份公开脱敏资料，不包含联系方式、雇主内部信息或未公开业务数据。
