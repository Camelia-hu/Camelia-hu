<!--
  用法：整段复制到 Camelia-hu/Camelia-hu 仓库根目录的 README.md。
  替换点只有一处：# 联系方式 里的邮箱已经填好（简历上的 QQ 邮箱），不想公开就改成别的或删掉。
  配色：背景 0D1117 / 主色 4E8CF7 / 辅色 8E6EF7。改主题时这几处要一起改，否则会出现白底卡片。
  图片 URL 里的中文已做百分号编码，直接手改会变成乱码——要改中文就改正文，别改 URL。
-->

<div align="center">
  <img width="100%" src="https://capsule-render.vercel.app/api?type=waving&color=0:4E8CF7,100:8E6EF7&height=130&section=header" alt="" />
</div>

<h1 align="center">胡小兵 <sub><code>Camelia-hu</code></sub></h1>

<p align="center">
  <b>后端开发 · Go / Java · 2027 届</b><br/>
  <sub>重庆邮电大学 · 计算机科学与技术 · 2023 – 2027</sub>
</p>

<div align="center">
  <a href="https://git.io/typing-svg">
    <img src="https://readme-typing-svg.demolab.com?font=JetBrains+Mono&weight=600&size=18&pause=1200&color=4E8CF7&center=true&vCenter=true&width=760&lines=Go%20%C2%B7%20Java%20%C2%B7%20%E5%88%86%E5%B8%83%E5%BC%8F%E7%B3%BB%E7%BB%9F%3B%E4%BA%91%E6%95%B0%E6%8D%AE%E5%BA%93%E6%8E%A7%E5%88%B6%E9%9D%A2%20%2F%20AI%20%E9%99%AA%E4%BC%B4%20%2F%20Feed%20%E6%B5%81%3B%E7%8E%B0%E5%9C%A8%E5%9C%A8%E5%86%99%EF%BC%9A%E8%AE%A9%20Agent%20%E8%87%AA%E5%B7%B1%E6%89%BE%E6%A0%B9%E5%9B%A0%3B2027%20%E5%B1%8A%20%C2%B7%20%E4%B8%89%E6%AE%B5%E5%90%8E%E7%AB%AF%E5%AE%9E%E4%B9%A0" alt="" />
  </a>
  <p>
    <img src="https://komarev.com/ghpvc/?username=Camelia-hu&label=profile%20views&color=4E8CF7&style=flat" alt="" />
    <img src="https://img.shields.io/badge/%E5%9C%A8%E6%89%BE-2027%20%E5%B1%8A%E6%A0%A1%E6%8B%9B%E5%90%8E%E7%AB%AF%E5%B2%97-8E6EF7?style=flat&labelColor=0d1117" alt="" />
    <img src="https://img.shields.io/badge/%E6%96%B9%E5%90%91-Go%20%C2%B7%20Java%20%C2%B7%20AIOps-4E8CF7?style=flat&labelColor=0d1117" alt="" />
  </p>
</div>

---

后端开发，Go 为主、Java 为辅。做过**云数据库控制面**的跨可用区迁移与节点诊断，做过**AI 陪伴产品**的语音链路与记忆系统，也做过**社交产品**的 Feed 流与榜单。三段实习，三种完全不同的负载形状。

现在主要精力在 **AIOps**：让 Agent 自己读指标、日志、链路和拓扑，把根因找出来——而且每条结论都必须绑着证据，能被复现、能被评测。

<br/>

## 🛠 技术栈

<div align="center">
  <img src="https://skillicons.dev/icons?i=go,java,python,mysql,redis,mongodb,docker,kubernetes,linux,git,githubactions,prometheus,grafana,nginx&theme=dark&perline=14" alt="技术栈" />
</div>

- **语言** — Go · Java · Python · SQL
- **存储** — MySQL（索引与事务）· Redis · MongoDB · Elasticsearch
- **中间件** — NSQ · Kafka · RabbitMQ · Asynq
- **云原生与可观测** — Docker / Compose · Kubernetes（kind / Helm）· Prometheus · Loki · Tempo · Grafana · OpenTelemetry / Jaeger
- **AI 工程** — ReAct Agent 运行时 · 工具调用 · RAG（Milvus / Qdrant）· 多智能体协作 · ASR 流式接入

<br/>

## 🧭 经历

| 时间 | 在哪 | 做了什么 |
|---|---|---|
| 2026.05 – 2026.09 | **飞轮数据** · 云产品研发（Java） | SelectDB 云研发：跨可用区迁移工作流、集群变配适配、实例级 `HostAliases`、容器日志采集链路（线上通过率 >98%）、告警 → 抓日志 → 建单 → AI 分析的运维闭环 |
| 2025.10 – 2025.12 | **天创进** · 后端（Go） | HelloTalk 社区 Feed 流：帖子拉取与发布、多策略优先级冲突梳理、文生视频服务的 MongoDB 建模与异步计数、榜单生命周期与分页 |
| 2025.05 – 2025.08 | **塔心科技** · AI 开发（Go） | 二次元 AI 陪伴产品：ASR 改全双工异步流式（2s → 1s）、三层记忆写入链路、Asynq 解耦耗时任务（60s → 20s，吞吐 +50%）、OpenTelemetry 链路追踪 |
| 2023 – 今 | **红岩网校** · 技术社团 | 参与「掌上重邮」后端迭代，日活 2000+，覆盖全体师生 |

<br/>

## 🚀 项目

### OpsAgent — 告警驱动的 AIOps 根因诊断 Agent
`2026.06 – 2026.10` · Go

面向 SRE 的自主根因诊断系统，接入指标 / 日志 / 链路 / 拓扑四类数据，打通「告警触发 → 多智能体取证 → 根因定位 → 结论回写」。核心不是"能答"，而是**结论可复现、可量化评测**。

- **多智能体 RCA** — 自研 ReAct 循环 + 协调者 / 专家双 Agent；按拓扑展开影响面，关联四类数据的异常，收敛到根因并绑定证据
- **告警侧治理** — `dedupe_key` 归并 + 状态机 + 静默冷却；有界 worker 池做背压，积压时丢任务而不是阻塞告警链路
- **多源取证** — PromQL / LogQL / TraceQL / 拓扑四类查询；源码检索固定 commit SHA，缺版本宁可报错也不回退 HEAD
- **工具治理与审批** — 装饰器链承载超时 / 审计 / 限流 / 审批；写操作在审批前封存闭包 + 一次性令牌，防重复执行
- **预算与状态恢复** — 并发调用前原子预占预算、只读同参复用；会话按 `tool_call_id` 重配对恢复

### feedsystem_video_go — 短视频 Feed 流系统
Go · Gin · MySQL · Redis · RabbitMQ

<table>
  <tr>
    <td width="50%" valign="top">
      <a href="https://github.com/Camelia-hu/feedsystem_video_go-medium">
        <img width="100%" src="https://github-readme-stats.vercel.app/api/pin/?username=Camelia-hu&repo=feedsystem_video_go-medium&theme=tokyonight&hide_border=true&bg_color=0D1117&title_color=4E8CF7&icon_color=8E6EF7&text_color=C9D1D9" alt="feedsystem_video_go" />
      </a>
    </td>
    <td width="50%" valign="top">
      <sub>
        · 推拉混合扩散，按粉丝数阈值切分大 V 读扩散与普通作者写扩散<br/>
        · 多级缓存，并做过一次有意的缓存击穿实验<br/>
        · Redis ZSET 预乘时间权重实现热度衰减，读时 O(log N) 取 TopK<br/>
        · 正在拆成 4 个微服务上 kind 集群，配故障注入开关 + k6 压测对比<br/>
        · <a href="https://www.bilibili.com/video/BV1Dti7B9E6Y">项目演示视频</a>
      </sub>
    </td>
  </tr>
</table>

<br/>

## 🌱 开源

**[ongrid](https://github.com/ongridio/ongrid)** · Go · AIOps Agent（1.2k ★）

围绕 IM 长连接的状态可见性：1 个 issue + 3 个 PR。

- [`#517`](https://github.com/ongridio/ongrid/issues/517) 飞书长连接卡死会让所有 IM 应用停止调度（维护者采纳并修复）
- [`#522`](https://github.com/ongridio/ongrid/pull/522) 把 stream 运行状态透出到 Channels 页面：运行中 / 重连中 / 已停止 + 最后错误
- [`#537`](https://github.com/ongridio/ongrid/pull/537) Slack 客户端取消不生效，关闭 socket 才能解阻
- [`#538`](https://github.com/ongridio/ongrid/pull/538) 修 #522 里状态抖动、时间戳被反复重置的问题

<br/>

## 📊 GitHub

<div align="center">
  <img height="160" src="https://github-readme-stats.vercel.app/api?username=Camelia-hu&show_icons=true&include_all_commits=true&theme=tokyonight&hide_border=true&bg_color=0D1117&title_color=4E8CF7&icon_color=8E6EF7&text_color=C9D1D9" alt="" />
  <img height="160" src="https://streak-stats.demolab.com?user=Camelia-hu&theme=tokyonight&hide_border=true&background=0D1117&ring=4E8CF7&fire=8E6EF7&currStreakLabel=4E8CF7&sideLabels=C9D1D9&dates=C9D1D9" alt="" />
  <img height="160" src="https://github-readme-stats.vercel.app/api/top-langs/?username=Camelia-hu&layout=compact&langs_count=8&theme=tokyonight&hide_border=true&bg_color=0D1117&title_color=4E8CF7&text_color=C9D1D9" alt="" />
  <img width="100%" src="https://github-readme-activity-graph.vercel.app/graph?username=Camelia-hu&bg_color=0D1117&color=C9D1D9&line=4E8CF7&point=8E6EF7&area=true&hide_border=true" alt="" />
</div>

<br/>

## 📫 联系

<div align="center">
  <a href="https://github.com/Camelia-hu"><img src="https://img.shields.io/badge/GitHub-Camelia--hu-4E8CF7?style=for-the-badge&logo=github&labelColor=0d1117" alt="GitHub" /></a>
  <a href="mailto:3225664565@qq.com"><img src="https://img.shields.io/badge/Email-3225664565%40qq.com-8E6EF7?style=for-the-badge&logo=gmail&logoColor=white&labelColor=0d1117" alt="Email" /></a>

<br/><br/>

<img width="100%" src="https://capsule-render.vercel.app/api?type=waving&color=0:8E6EF7,100:4E8CF7&height=100&section=footer" alt="" />
</div>
