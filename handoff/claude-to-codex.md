# Claude → Codex 交接（第 1 轮）

- 日期：2026-11-06（检索与核实均在截止日 2026-11-07 前完成）
- 分支：`claude/literature-review`
- 性质：阶段一资料（计划表 + 已核实文献库），**不是最终报告**；未代写任何个人反思。

## 0. 需要 Codex 首先确认：研究范围已变更

AGENTS.md、CLAUDE.md、README.md 写的题目是"水下机器人"。本轮学生（自选题目）在比较可写性后，**决定改为 VLA 自动驾驶**：

- 水下方向做过一轮完整检索（AUV/ROV 多传感器融合定位）。近期正式论文能满足要求，但多数顶级来源不在近 12 个月内，实验条件差异大、难以做同基准比较。该轮资料只在学生本地归档（`archive/`，已加入 .gitignore），**不入库**。
- 按 AGENTS.md"新的研究范围由 Codex 协调确认"，请 Codex 确认新题目，并视需要更新 AGENTS.md、CLAUDE.md、README.md 中的题目描述。Claude 没有修改这三个文件。

## 1. 推荐研究题目及边界（建议，待确认）

**Vision-Language-Action Models for End-to-End Autonomous Driving: A Comparison of Action Generation and Reasoning Mechanisms**

研究问题、比较方案、比较维度、分工与进度见 `research/plan.md`；边界见 `research/scope.md`。

## 2. 近期论文及日期证据

口径：2025-11-07 至 2026-11-06。会议论文以会议日期为准，并核对论文出现在官方论文集、OpenReview 或会议官网；预印本不计入。

| 编号 | 论文 | 会议（日期） | 日期证据 | 论文出处核验 |
|---|---|---|---|---|
| V01 | DriveVLA-W0: World Models Amplify Data Scaling Law in Autonomous Driving | ICLR 2026（2026-04-23~25） | https://iclr.cc/Conferences/2026/Dates | ICLR 官方论文集 PDF |
| V02 | ReCogDrive: A Reinforced Cognitive Framework for End-to-End Autonomous Driving | ICLR 2026 | 同上 | ICLR 虚拟会议页 + OpenReview JoXwhGbuMi |
| V03 | Discrete Diffusion for Reflective Vision-Language-Action Models in Autonomous Driving | ICLR 2026 | 同上 | OpenReview XJxXSMLDoZ |
| V04 | AutoDrive-R²: Incentivizing Reasoning and Self-Reflection Capacity for VLA Model in Autonomous Driving | ICLR 2026 | 同上 | OpenReview KVWaCzJrrq |
| V05 | AutoVLA: A Vision-Language-Action Model for End-to-End Autonomous Driving with Adaptive Reasoning and Reinforcement Fine-Tuning | NeurIPS 2025（2025-12-03~05） | https://nips.cc/Conferences/2025/Dates | NeurIPS 官网海报页 + OpenReview 28qUA2bSe5 |
| V06 | Unifying Language-Action Understanding and Generation for Autonomous Driving（LinkVLA） | CVPR 2026（2026-06-05~07） | https://cvpr.thecvf.com/Conferences/2026/Dates | CVF Open Access，pp. 25193–25203 |
| V07 | DriveMoE: Mixture-of-Experts for Vision-Language-Action Model in End-to-End Autonomous Driving | CVPR 2026 | 同上 | CVF Open Access，pp. 10678–10688 |

V08（CVPR 2026 Findings）、V09（CVPR 2026，作者未核验）暂不计入。

## 3. 代表方案、比较标准和最有力的证据

- S1 DriveVLA-W0（V01）、S2 ReCogDrive（V02）、S3 AutoVLA（V05）、S4 LinkVLA 或 DriveMoE（V06/V07），以及 S5 Alpamayo-R1（V10，NVIDIA 预印本 + 开源模型 + 实车测试）。非 VLA 对照：DiffusionDrive（V12）。
- 主比较基准：NAVSIM PDMS/EPDMS（V15）；闭环比较：Bench2Drive DS/SR（V16），两者分开比较。
- 目前读到的数值 [作者报告]：
  - V01：NAVSIM v1 PDMS 93.0（best-of-6）/ 88.4（query 专家，实时版本）；v2 EPDMS 86.1；延迟 117.8→74.3 ms（Table 1、2，Sec. 4.5）。
  - V02：NAVSIM PDMS 90.8；Bench2Drive DS 71.36。来源为官方 GitHub README，尚未对照论文表格。

## 4. 未核验信息、未获取全文与不可比条件

- 除 V01 的结果表外，其余论文只读了摘要或仓库说明，数值待深读时对照 PDF。
- V01 的 OpenReview id 未补；V09 作者未核验；V08 是否收入正式论文集未核验。
- V06、V13（DriveVLM）、V03 都有作者 Kun Zhan、XianPeng Lang，可能与理想汽车有关，**所属机构未核验**，报告中不要直接写成"理想汽车论文"。
- 理想 MindVLA（V17）只有新闻转述；小鹏、Wayve、特斯拉没有找到可核验的技术材料。
- NAVSIM 分数设置不一致（best-of-6 / 单次输出、额外预训练数据、相机数量），直接排序前须逐项核对。

## 5. 文件变更路径清单（本分支相对 main）

| 操作 | 路径 |
|---|---|
| 新增 | `research/plan.md` |
| 新增 | `research/scope.md` |
| 新增 | `research/search-log.md` |
| 新增 | `research/literature.csv` |
| 新增 | `research/references.bib` |
| 新增 | `handoff/claude-to-codex.md` |
| 修改 | `LOCATIONS.md`（登记以上文件，并标注三份规则文件的题目待更新） |
| 修改 | `.gitignore`（追加 `archive/`） |
| 未改 | `README.md`、`AGENTS.md`、`CLAUDE.md`、`docs/`、`prompts/`、`research/README.md`、`handoff/README.md` |

本地索引（外部课程项目 LOCATIONS.md、工作区 PROJECT_LOCATIONS.md）**未同步**，Claude 无法访问，请 Codex 导入。

## 6. 检查、分支与推送状态

- 已检查：CSV 共 17 行、16 列，表头符合 research/README.md 的建议；BibTeX 键 V01–V17 与 CSV 编号一一对应；各 md 文件引用的编号都在 CSV 中。
- 历史：首个提交 `edbae5b` 是在 main 规则文件出现之前，从空仓库视角创建的独立根提交。之后以合并提交并入 main（允许无关历史；README.md 与 .gitignore 采用 main 版本），再加本修正提交。**没有强制推送，也没有改写历史。**
- 推送：由学生在本机终端推送，用学生的 GitHub 账号。

## 7. Codex 下一步

1. 确认题目变更，必要时更新 AGENTS.md、CLAUDE.md、README.md。
2. 阶段二：深读 S1–S5，填写 `research/evidence-notes.md`、`comparison.md`、`gaps.md`（见 plan.md §6）。
3. 审核合并到 main。
4. 学习收获与职业兴趣由学生本人撰写。
