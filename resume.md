---
layout: page
title: Engineering Profile
permalink: /resume/
---

# AI Engineering Profile

> 面向真实生产环境的 AI 基础设施、Agent Runtime 与自动驾驶数据系统工程。

**求职方向**：AI Infra / LLM Serving / Agent Runtime & Harness / 自动驾驶平台工程  
**工作地点**：杭州 / 上海 / Remote

这是一份公开、脱敏的工程履历。它只呈现可以讨论的技术问题、系统设计与项目实践，不包含个人联系方式、雇主内部信息或未公开业务数据。

## Engineering Focus

- **AI Infra**：GPU 推理服务、模型部署、资源调度、网关与流量治理、可观测性、稳定性工程。
- **Agent Runtime**：多 Agent 任务编排、工具与权限边界、运行时隔离、状态回读、失败恢复与证据化交付。
- **平台后端**：Java / Spring Cloud、Python / FastAPI、微服务、事件驱动、时序数据、多租户与成本治理。
- **自动驾驶工程**：ROS / ROS2、BEV 感知、模型部署、传感器数据链路与车云协同。
- **交付方式**：从问题定义、架构设计和实现，到部署、监控、故障定位与持续验证。

## Selected Engineering Work

### GPU 推理与模型服务平台

面向多模型、多 GPU 节点的内部推理场景，参与构建从模型接入到线上运行的服务化链路。

- 使用 vLLM、LiteLLM 与 Nginx 组织兼容 OpenAI API 的推理入口，处理模型路由、健康检查、访问控制与服务降级。
- 围绕 CUDA、驱动、Transformers 与不同模型架构的兼容矩阵处理部署问题，并把一次性排障沉淀为可复用的镜像与运行约束。
- 使用 DCGM Exporter、Prometheus 与 Grafana 建立 GPU、请求和服务级可观测性。
- 关注吞吐、首 Token 延迟、缓存命中、显存利用率与故障恢复，而不只以“模型能够启动”作为交付标准。

**关键词**：LLM Serving · vLLM · LiteLLM · CUDA · Docker · Prometheus · Grafana · GPU Observability

### Fleet-to-PR / Agent Engineering Platform

探索让 Coding Agent 从任务接收走到可审查工程产物的完整链路，而不是停留在聊天或代码片段生成。

- 将任务拆分、ownership、上下文预检、工具调用、执行记录、验证结果与交付证据组织成可追踪流程。
- 设计 PASS / BLOCK gate，区分代码生成完成、CI 通过、评审通过、契约满足和真实运行验证。
- 处理 stale context、失败 handoff、重复执行、资源残留与恢复路径等 Agent 长流程问题。
- 将运行时资源、密钥句柄、路由绑定和生命周期管理抽象为 control plane 能力。

**关键词**：Agent Harness · Runtime Control Plane · Multi-Agent · Tool Governance · Evidence · Recovery

### Tesla 车辆数据多租户 SaaS（构建中）

面向非开发者车主设计低成本托管服务，兼容 TeslaMate 生态，同时保留共享托管与独享部署两种交付方式。

- 规划 Telemetry、Owner API 与 Fleet API 的多通道接入和迁移路径，降低上游接口变化带来的单点风险。
- 围绕车辆状态机、流式事件、时序数据、MQTT、只读兼容接口和客户端适配设计服务边界。
- 以租户隔离、凭证安全、最小权限、审计与数据生命周期作为基础约束，而不是后置补丁。
- 通过共享基础设施、分层存储和资源配额控制单位用户成本，并保留独享实例以满足更高隐私要求。
- 将产品验证纳入工程设计：兼容既有客户端、支持自部署迁移，并以留存、续费和支持成本检验是否是一门可持续的 SaaS 生意。

**关键词**：Multi-Tenant SaaS · TeslaMate · Telemetry · Fleet API · MQTT · Time-Series Data · Privacy

### 自动驾驶感知与部署链路

围绕多传感器感知模型在真实车辆/场景中的运行，连接算法、推理环境和 ROS 工程链路。

- 参与 LiDAR、图像与 BEV 融合相关模型的部署和工程集成，覆盖检测、分割与占用等任务。
- 处理多模型并行、GPU 资源、进程组织、ROS 消息链路与可视化调试。
- 使用 torchrun / DDP / NCCL 等组件处理训练与多卡运行问题，关注数据、模型和运行环境的一致性。
- 通过 Foxglove、RViz 与日志指标定位从传感器输入到模型输出之间的系统问题。

**关键词**：BEV · Sensor Fusion · ROS · PyTorch · DDP · NCCL · Foxglove · RViz

### 城市母婴室地图

从公开与合作数据构建城市级母婴设施地图，覆盖数据整理、POI 融合、地图展示和产品审核流程。

- 将多来源 POI 清洗、去重和结构化，形成可持续更新的数据资产。
- 完成小程序端的位置检索、地图展示与基础产品闭环。
- 用真实用户使用情况和维护成本评估项目价值，而不是只交付演示页面。

**关键词**：Data Pipeline · POI · Mini Program · Product Engineering

## Technical Toolkit

| Area | Technologies |
|---|---|
| Backend | Java, Spring Cloud, Python, FastAPI, REST, SSE |
| AI Serving | vLLM, LiteLLM, PyTorch, CUDA, Transformers |
| Agent Systems | Agent Harness, Tool Calling, MCP, Runtime Isolation, Control Plane |
| Platform | Docker, Nginx, GitHub Actions, Linux, Prometheus, Grafana |
| Autonomous Driving | ROS / ROS2, BEV, DDP, NCCL, Foxglove, RViz |
| Data | PostgreSQL, SQLite, MQTT, Time-Series Data, Multi-Tenant Design |

## What I Optimize For

我更关心系统能否在真实环境中长期运行：接口变化时能否迁移，Agent 失败时能否恢复，GPU 服务异常时能否定位，多租户数据是否真正隔离，以及成本是否允许产品持续经营。

适合一起讨论的问题包括：推理平台、Agent Runtime、Coding Agent 工程化、自动驾驶平台，以及车辆数据 SaaS。
