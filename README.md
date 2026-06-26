# Agent Skills Hub

> 个人精选技能库。基于实际工作场景（BNPL 产品经理 / 内容创作 / 数据分析）评估优先级，记录每个 skill 的能力边界和最佳使用时机。

---

## 优先级总览

| 层级 | Skill | 理由 |
|---|---|---|
| 🔴 每周必用 | html-anything | 已在做 HTML 看板，直接升级工作流 |
| 🔴 每周必用 | baoyu-skills | BRD 流程图 / 信息图 / 看板封面全覆盖 |
| 🟠 高频有用 | guizang-ppt-skill | 周报、BRD 评审、策略汇报时产出演示稿 |
| 🟠 高频有用 | content-research-writer | 写 BRD / 竞品调研 / 产品方案时的结构化辅助 |
| 🟡 按需使用 | guizang-social-card-skill | 有公众号/外部分享需求时 |
| 🟡 按需使用 | dbskill | 产品策略诊断 / 内容选题 / 决策梳理 |
| 🟡 按需使用 | khazix-skills (hv-analysis) | 写竞品研究报告、用户分层等重型分析 |
| 🔵 低频备用 | ian-xiaohei-illustrations | 写外部文章时配图 |
| 🔵 低频备用 | Humanizer-zh | 内部文档 AI 痕迹不敏感，暂时用处不大 |

---

## 🔴 每周必用

### 1. html-anything
**→ [nexu-io/html-anything](https://github.com/nexu-io/html-anything)**

**一句话**：任意内容（Markdown / CSV / JSON / 文字）→ 杂志文章 / PPT / 海报 / 数据报告 / 小红书卡，单文件 HTML 输出，可一键发布。

**为什么每周用**：你已经在手动写 bnpl-dashboard.html、all-work-dashboard.html、product-requirements-dashboard.html，这个 skill 可以把「把内容转成漂亮 HTML」变成一个对话命令。适用：
- 周报 → 可分享的 HTML 周报卡
- 数据分析结论 → 海报 / 信息图
- BRD 摘要 → 演示页面

**核心能力**：
- 75 个模板，覆盖 9 种输出类型（magazine / deck / poster / 小红书 / 数据报告等）
- 兼容主流 agent runtime，不需要额外 API key
- CJK 字体优化 + 8px 网格 + ≥4.5 对比度设计约束
- SSE 流式预览，改完即看

**安装**：
```bash
git clone https://github.com/nexu-io/html-anything
cd html-anything && pnpm install && pnpm -F @html-anything/next dev
# → http://localhost:3000
```

**使用场景示例**：
```
把这份 BNPL 周报总结转成杂志风 HTML 一页纸
把这个数据表格转成数据报告风格的 HTML
```

---

### 2. baoyu-skills
**→ [JimLiu/baoyu-skills](https://github.com/JimLiu/baoyu-skills)**

**一句话**：20+ 个模块工具箱，核心价值在 SVG 流程图、信息图、文章封面，另有一键发布微信/X/微博。

**为什么每周用**：你写 BRD 需要流程图、用户旅程图；做数据看板需要信息图；偶尔发公众号需要封面和一键发布。这一个 repo 解决多个日常输出场景。

**核心 Skills（按你的使用频率排）**：

| Skill | 功能 | 你的场景 |
|---|---|---|
| `baoyu-diagram` | SVG 流程图 / 序列图 / 架构图，手动布局数学，轻重模式均支持 | BRD 业务流程 / 跳端引导链路图 |
| `baoyu-infographic` | 信息图，21 种布局 × 17 种风格 | 数据结论可视化 / 周报配图 |
| `baoyu-cover-image` | 文章封面，5 维定制系统 | 公众号封面 / 内部报告封面 |
| `baoyu-xhs-images` | 小红书卡片，12 种画风 × 5 种布局 | 外部内容分发 |
| `baoyu-post-to-wechat` | 公众号一键发布（API / 浏览器两种方式） | 发布工作流自动化 |
| `baoyu-comic` | 知识漫画，5 种画风 | 产品概念解释 / 培训材料 |

**安装**：
```bash
npx skills add jimliu/baoyu-skills
# 推荐按需安装，避免全量加载增加 context 开销：
npx skills add jimliu/baoyu-skills --skill baoyu-diagram
npx skills add jimliu/baoyu-skills --skill baoyu-infographic
```

---

## 🟠 高频有用

### 3. guizang-ppt-skill
**→ [op7418/guizang-ppt-skill](https://github.com/op7418/guizang-ppt-skill)**

**一句话**：文章/大纲 → 杂志风或瑞士风 HTML 演讲幻灯片，单文件输出，键盘/触屏翻页。

**为什么高频**：你有 BRD 评审、策略汇报、周会、跨团队对齐等场景，需要快速把文字结论变成「能展示的东西」。比传统 PPT 快，比纯文字专业。

**两种风格**：
- **风格 A（电子杂志×电子墨水）**：衬线标题 + 流体 WebGL 背景 + 暖色，适合对外分享 / 产品故事
- **风格 B（瑞士国际主义）**：无衬线 + 网格点阵 + 高亮色块，适合数据汇报 / 策略评审

**使用场景**：
```
把这份 BNPL 跳端方案 BRD 的核心逻辑做成瑞士风 PPT，供评审会用
把本周业务总结做成杂志风 HTML 演示，发给老板
```

**安装**：
```bash
npx skills add op7418/guizang-ppt-skill
```

---

### 4. content-research-writer
**→ [ComposioHQ/awesome-skills](https://github.com/ComposioHQ/awesome-claude-skills/tree/master/content-research-writer)**

**一句话**：调研 → 提纲 → 逐节写作 → 引用整理，保留你的写作风格。

**为什么高频**：你有大量结构化文档产出：BRD、产品方案、竞品分析、实验复盘。这个 skill 的「协作提纲 → 分节写 → 引用管理」流程跟你写 BRD 的实际节奏高度吻合。

**工作流程**：
1. 给出主题和已有材料
2. 共同确认提纲结构
3. 逐节撰写，获取反馈（优点 / 改进 / 具体示例）
4. 整合引用和数据来源

**安装**：在对应目录里单独取用，或直接引用该目录下的 SKILL.md。

---

## 🟡 按需使用

### 5. guizang-social-card-skill
**→ [op7418/guizang-social-card-skill](https://github.com/op7418/guizang-social-card-skill)**

**一句话**：文章 / 截图 / 笔记 → 小红书竖版轮播卡 + 公众号 21:9+1:1 封面对，Editorial × Swiss 两套风格。

**何时用**：有公众号文章要发或对外分享内容时。

**核心能力**：
- 28 种布局 × 10 种主题调色板
- 自动生成小红书图文组（3:4）+ 公众号封面对（21:9 + 1:1）
- HTML 渲染后导出 PNG

**安装**：
```bash
npx skills add op7418/guizang-social-card-skill
```

---

### 6. dbskill
**→ [dontbesilent2025/dbskill](https://github.com/dontbesilent2025/dbskill)**

**一句话**：商业诊断全流程工具，21 个子命令覆盖选题、标题、内容诊断、决策、目标梳理。

**何时用**：做产品策略梳理 / 内容规划 / 复杂决策时。最有用的几个命令：

| 命令 | 适合你的场景 |
|---|---|
| `/dbs-diagnosis` | 产品商业模式诊断，梳理 BNPL 某渠道的增长逻辑 |
| `/dbs-decision` | 需要在多个方案间做决策时（如流量层级设定） |
| `/dbs-content` | 内容选题诊断，如写公众号选题前 |
| `/dbs-xhs-title` | 小红书标题优化 |
| `/dbs-goal` | 目标清晰化，OKR 拆解辅助 |

**安装**：
```bash
npx -y skills add dontbesilent2025/dbskill -g --all
```

---

### 7. khazix-skills
**→ [KKKKhazix/Khazix-Skills](https://github.com/KKKKhazix/Khazix-Skills)**

**一句话**：6 个工具：磁盘清理 / AI 资讯 / 文档同步 / 万字研究报告 / 个人风格写作。

**最值得关注的**：
- **`hv-analysis`**：自动生成 10K–30K 字 PDF 研究报告。适合：用户分层分析（T044）、TEMU 竞品专项、行业调研
- **`neat-freak`**：每次 session 结束后自动同步代码变更到文档和 agent memory。适合维护工作文档一致性（对应你的 T047 模板体系）

**安装**（按需单装）：
```bash
# 安装 hv-analysis
帮我安装 skill：https://github.com/KKKKhazix/khazix-skills/tree/main/hv-analysis
# 安装 neat-freak
帮我安装 skill：https://github.com/KKKKhazix/khazix-skills/tree/main/neat-freak
```

---

## 🔵 低频备用

### 8. ian-xiaohei-illustrations
**→ [helloianneo/ian-xiaohei-illustrations](https://github.com/helloianneo/ian-xiaohei-illustrations)**

**一句话**：文章 → 小黑怪诞风正文配图，白底手绘 16:9，少量红橙蓝批注，4–8 张/篇。

**何时用**：如果你写对外文章（公众号/知乎）需要正文插图时。对 DiDi 内部文档用处不大。

**安装**：`Use $ian-xiaohei-illustrations` 触发（需先安装 skill）

---

### 9. Humanizer-zh
**→ [op7418/Humanizer-zh](https://github.com/op7418/Humanizer-zh)**

**一句话**：去除 AI 写作痕迹（24 种模式检测），对改写后文本打分（满分 50）。

**何时用**：写对外公众号文章、外部报告时。内部 BRD / 产品文档 AI 痕迹不敏感，暂时用处不大。

**安装**：
```bash
npx skills add op7418/Humanizer-zh
```

---

## 安装优先顺序（建议）

```bash
# 第一批：每周必用
git clone https://github.com/nexu-io/html-anything  # html-anything（本地 server）
npx skills add jimliu/baoyu-skills --skill baoyu-diagram
npx skills add jimliu/baoyu-skills --skill baoyu-infographic

# 第二批：高频有用
npx skills add op7418/guizang-ppt-skill
# content-research-writer: 手动复制 SKILL.md 到 ~/.agents/skills/

# 按需安装
npx skills add op7418/guizang-social-card-skill
npx -y skills add dontbesilent2025/dbskill -g --all
npx skills add op7418/Humanizer-zh
```

---

## 关联资料

- GitHub Stars 列表 — 可在自己的 GitHub 账号 `Stars` 页面查看已收藏的 skill repo
- [Awesome Skills 列表](https://github.com/travisvn/awesome-claude-skills) — 社区精选列表
- [官方 Skills 集合](https://github.com/anthropics/skills) — 官方维护的 skill 集合

---

*Last updated: 2026-06-25 | 基于实际工作场景评估，优先级会随工作重心调整*
