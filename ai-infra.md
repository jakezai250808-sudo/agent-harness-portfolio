---
layout: default
title: AI Infra 工程师简历
permalink: /ai-infra/
description: 面向异构集群、训推平台、训练基建与系统性能方向的公开工程简历。
---

<article class="resume">
  <header class="resume-header">
    <div class="resume-kicker">AI INFRA ENGINEER · HANGZHOU</div>
    <div class="resume-heading">
      <div>
        <h1>AI Infra 工程师｜异构算力 × 训推平台 × 可观测性</h1>
        <p class="resume-summary">4+ 年平台与后端工程经验，参与百卡规模 GPU 模型服务，并在多卡训练、CUDA 环境、模型部署和监控排障中持续解决跨层问题。擅长把算法团队面对的算力、环境、服务与故障问题，沉淀为可复用的平台能力。</p>
      </div>
      <div class="resume-target">
        <span>目标方向</span>
        <strong>集群调度与资源平台</strong>
        <strong>训练 / 推理基础设施</strong>
        <strong>系统性能与稳定性</strong>
      </div>
    </div>
    <div class="resume-meta">
      <span>杭州优先 · 上海 / Remote</span>
      <span>百卡规模工程实践</span>
      <span>Java · Python · PyTorch · CUDA</span>
    </div>
  </header>

  <section class="resume-section">
    <h2>与岗位的直接匹配</h2>
    <div class="signal-grid">
      <div><strong>异构算力工程</strong><p>处理 A100 / V100 等 GPU、驱动、CUDA、框架与量化方案的兼容矩阵，并将经验固化为镜像和部署约束。</p></div>
      <div><strong>训推平台底座</strong><p>覆盖多卡训练、模型服务、统一入口、健康检查、访问控制、容量判断和故障恢复。</p></div>
      <div><strong>跨层问题定位</strong><p>能沿请求、容器、框架、CUDA、GPU 和 ROS / 业务链路拆解性能与稳定性问题。</p></div>
    </div>
  </section>

  <section class="resume-section">
    <div class="section-title-row">
      <h2>岗位要求与工程证据</h2>
      <span>围绕集群、训练、网络与模型协同</span>
    </div>
    <div class="skill-rows">
      <div><strong>集群调度</strong><span>具备异构 GPU 资源池、多模型服务和容量治理经验；关注拓扑感知、优先级、排队延迟、吞吐与利用率之间的系统权衡。</span></div>
      <div><strong>训练基建</strong><span>使用 Docker、PyTorch、torchrun、DDP、NCCL 组织训练与多卡运行；能将依赖兼容、镜像规范、指标和恢复流程平台化。</span></div>
      <div><strong>监控与可观测</strong><span>基于 DCGM Exporter、Prometheus、Grafana 建设 GPU 与服务观测，围绕吞吐、首 Token 延迟、显存、错误率和恢复时间定位问题。</span></div>
      <div><strong>系统性能</strong><span>从请求、模型、显存、框架、CUDA、GPU 与操作系统视角分析抖动和长尾；具备把单点故障经验转化为平台约束的意识。</span></div>
      <div><strong>高性能通信</strong><span>已有 NCCL 与多卡运行实践，理解计算、通信和数据路径需协同分析；希望进一步深入 RDMA、RoCEv2 / InfiniBand、拥塞控制与拓扑调优。</span></div>
      <div><strong>集群模型协同</strong><span>能够从模型架构、量化方式、显存占用、吞吐与延迟目标反推并行策略、运行环境和资源配置，并与算法团队完成落地。</span></div>
    </div>
  </section>

  <section class="resume-section">
    <div class="section-title-row">
      <h2>核心工程经历</h2>
      <span>只保留与 AI Infra 直接相关的证据</span>
    </div>

    <article class="resume-project" id="infra-serving">
      <div class="project-side">
        <span class="status production">生产实践</span>
        <span class="project-domain">MODEL SERVING</span>
      </div>
      <div class="project-main">
        <h3>百卡规模 GPU 推理与模型服务平台</h3>
        <p class="project-brief">面向多模型、异构 GPU 与多团队并发使用场景，将零散部署收敛为统一、可观察、可治理的模型服务能力。</p>
        <ul>
          <li>基于 vLLM、LiteLLM、Nginx 建设兼容 OpenAI API 的统一入口，覆盖路由、健康检查、访问控制和故障降级。</li>
          <li>处理驱动、CUDA、Transformers、量化方案与模型架构的兼容关系，将排障结果固化为镜像、版本约束和部署规范。</li>
          <li>以吞吐、首 Token 延迟、显存利用率、缓存命中和恢复时间评价服务质量，支持容量判断与性能优化。</li>
          <li>参与百卡规模算力环境的服务化使用，对资源供给、模型需求和服务稳定性之间的矛盾有真实工程认识。</li>
        </ul>
        <div class="result"><b>可承担的工作</b> 模型服务平台、异构 GPU 环境治理、资源与容量观测、推理性能分析及故障恢复。</div>
        <div class="tech-tags"><span>vLLM</span><span>LiteLLM</span><span>PyTorch</span><span>CUDA</span><span>Docker</span><span>Nginx</span></div>
      </div>
    </article>

    <article class="resume-project" id="infra-observability">
      <div class="project-side">
        <span class="status production">工程实践</span>
        <span class="project-domain">OBSERVABILITY</span>
      </div>
      <div class="project-main">
        <h3>GPU 监控、容量判断与跨组件排障</h3>
        <p class="project-brief">让 GPU 使用、模型服务质量和异常恢复从“依靠经验”转变为有指标、有路径、可复盘的工程过程。</p>
        <ul>
          <li>使用 DCGM Exporter、Prometheus、Grafana 采集和展示 GPU、主机与服务指标，支撑利用率分析和异常发现。</li>
          <li>将请求错误、服务健康、显存压力、GPU 状态与模型行为关联，缩短跨团队问题定位路径。</li>
          <li>围绕超时、降级、健康检查和恢复建立服务治理机制，避免仅用进程存活判断系统可用。</li>
          <li>关注性能抖动、慢节点、资源争用和依赖漂移等系统性问题，并推动经验进入部署规范与检查项。</li>
        </ul>
        <div class="result"><b>工程价值</b> 不把可观测性停留在仪表盘，而是让指标参与容量规划、故障判断和恢复闭环。</div>
        <div class="tech-tags"><span>DCGM Exporter</span><span>Prometheus</span><span>Grafana</span><span>Health Check</span><span>SRE</span></div>
      </div>
    </article>

    <article class="resume-project" id="infra-training">
      <div class="project-side">
        <span class="status production">工程实践</span>
        <span class="project-domain">DISTRIBUTED TRAINING</span>
      </div>
      <div class="project-main">
        <h3>多机多卡训练与感知模型部署链路</h3>
        <p class="project-brief">在自动驾驶感知场景中连接训练、GPU 环境、模型依赖和真实运行链路，处理实验环境之外的一致性与通信问题。</p>
        <ul>
          <li>使用 torchrun、DDP、NCCL 支持多卡训练与运行，关注数据、模型、依赖和环境的一致性。</li>
          <li>参与 LiDAR、图像、BEV 融合及检测、分割、Occupancy 等多模型的部署集成。</li>
          <li>结合 GPU、进程、日志、ROS 消息和可视化工具定位问题，将“模型异常”拆解到数据、通信、资源或生命周期层。</li>
          <li>与算法和系统团队协作，根据模型计算、显存和运行特征调整部署方式，而非把模型作为黑盒服务。</li>
        </ul>
        <div class="result"><b>可迁移价值</b> 具备从模型特征反推资源与运行方案的经验，可继续深入大规模训练调度、通信优化和自动容灾。</div>
        <div class="tech-tags"><span>torchrun</span><span>DDP</span><span>NCCL</span><span>BEV</span><span>ROS</span><span>Multi-GPU</span></div>
      </div>
    </article>
  </section>

  <section class="resume-section">
    <h2>技术能力</h2>
    <div class="skill-rows">
      <div><strong>计算与框架</strong><span>GPU · CUDA · PyTorch · vLLM · Transformers · 量化部署 · DDP · NCCL</span></div>
      <div><strong>平台工程</strong><span>Java · Spring Cloud · Python · FastAPI · Docker · Nginx · GitHub Actions</span></div>
      <div><strong>服务治理</strong><span>模型路由 · 健康检查 · 访问控制 · 降级恢复 · 容量与性能指标</span></div>
      <div><strong>可观测性</strong><span>DCGM Exporter · Prometheus · Grafana · 日志与跨组件问题定位</span></div>
      <div><strong>持续深入</strong><span>Kubernetes 调度 · 拓扑感知 · RDMA / RoCEv2 / InfiniBand · 大规模训练容灾</span></div>
    </div>
  </section>

  <section class="resume-section">
    <h2>适合进一步交流的问题</h2>
    <div class="signal-grid">
      <div><strong>资源利用率</strong><p>如何结合模型画像、拓扑和服务目标，提高异构算力利用率而不牺牲稳定性。</p></div>
      <div><strong>性能与长尾</strong><p>如何从模型、通信、GPU、主机和网络指标定位抖动、慢节点及长尾延迟。</p></div>
      <div><strong>平台化与容灾</strong><p>如何把镜像、监控、检查、恢复和调度策略组合成可演进的训推基础设施。</p></div>
    </div>
  </section>

  <footer class="resume-note">公开脱敏版｜专门用于 AI Infra、集群调度、训练基础设施与系统性能方向的技术交流。</footer>
</article>
