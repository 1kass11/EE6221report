# EE6221 CA2 — Underwater Robotics Review

水下机器人前沿文献调研与比较评价。课程作业提交截止日期为 **2026 年 11 月 7 日**，具体时刻以 NTULearn 为准，最终提交 PDF。

## 当前状态
仓库框架与研究提示词已建立。文献检索尚未开始，具体子题和最佳方案尚未确定。空白研究记录不能视为研究成果。

## 阅读入口
1. [作业要求与验收清单](docs/assignment-requirements.md)
2. [发给 Claude 的完整检索提示词](prompts/claude-literature-search.md)
3. [项目规则](AGENTS.md) 与 [Claude 协作规则](CLAUDE.md)
4. [研究资料说明](research/README.md)
5. [交接流程](handoff/README.md)
6. [文件位置与状态](LOCATIONS.md)

## 分工与流程
- **Codex**：主要负责人，审核子题、来源与实验数据，建立比较框架，整合最终报告。
- **Claude**：检索文献，记录元数据与证据，提出候选比较方案，通过 `claude/literature-review` 分支交接。
- **学生**：确认个人学习收获与职业兴趣，完成课程平台提交。

Claude 开始前先拉取仓库最新内容。研究成果在独立分支提交；Codex 审核后整合进主分支。每次文件变更都应同步 LOCATIONS.md。

## 研究原则
选择一类水下机器人或一项技术，明确场景与比较标准。至少核验两篇最近 12 个月内发表的相关文章。论文、产品规格与演示分开记录；缺少统一实验条件时不得简单排名。当前仓库不包含已核验的参考文献。
