# AI × Web3 School Cohort 0 Learning Log

这是我的 AI × Web3 School Cohort 0 个人学习仓库，用来公开记录学习计划、任务证明、实验记录、每日打卡草稿、Handbook feedback 和 Hackathon 准备过程。

## Week 1 Review Pack / 本周汇总入口

这是 2026-05-19 至 2026-05-21 的公开学习 Pack。审核者可以从本 README 快速看到本周学了什么、做了什么、验证了什么、修正了什么。

Final WCB submission link:

```text
https://github.com/yoona333/ai-web3-school-cohort-0
```

### Review Summary

| Requirement | Proof |
| --- | --- |
| AI 学习记录 / 概念卡片 | [Learning plan](learning-plan.md), [Daily note 2026-05-19](daily/2026-05-19.md), [Daily note 2026-05-20](daily/2026-05-20.md) |
| Learning Agent / AI 工具实践 | [Agent workflow](agent-workflow.md), [Agent workflow run record](submissions/2026-05-20-agent-workflow-run-record.md) |
| Web3 概念卡片 | [EOA / smart account / multisig comparison](tasks/2026-05-20-account-types-comparison.md) |
| AI × Web3 最小交叉实验 | [ERC-4337 flow learning demo](experiments/erc4337-flow-demo/README.md), [interactive HTML demo](experiments/erc4337-flow-demo/index.html) |
| 链上验证或流程图 | 本周不提交真实测试网交易哈希或合约地址；使用 [ERC-4337 flow demo](experiments/erc4337-flow-demo/README.md) 作为账户抽象流程 proof |
| 问题 / 失败 / 人工修正记录 | [Manual review and correction record](submissions/2026-05-20-agent-workflow-run-record.md#5-manual-review-correction-or-rejection-record), [ERC-4337 demo submission draft](submissions/2026-05-21-erc4337-flow-demo-submission.md) |

### What Reviewers Can Verify

- AI: I created a personal learning plan and daily learning records.
- Agent / workflow: I configured a bounded learning agent workflow with human confirmation rules.
- Web3: I wrote a comparison note for EOA, smart accounts, and multisig accounts.
- AI × Web3: I built a static ERC-4337 flow explainer that turns a learning question into a role-based account abstraction flow.
- Safety: This Pack avoids private keys, seed phrases, API keys, tokens, `.env` files, wallet signatures, transfers, approvals, and contract writes.

## Links

- AI × Web3 School Handbook: https://aiweb3.school/zh/handbook/
- Learning Agent Prompt: https://aiweb3.school/learning-agent.zh.txt
- WCB 课程页面: https://web3career.build/zh/programs/AI-Web3-School

## What This Repo Is For

- 记录每日学习输入、输出和 blocker
- 保存任务完成证明和可复现步骤
- 归档 AI × Web3 小实验、prompt、代码片段和结论
- 沉淀 Handbook feedback，方便后续提交 issue 或 PR
- 为 Hackathon 准备题目、方案、原型和提交材料
- 记录 coding / learning agent 工作流和安全边界

## Privacy Reminder

这是计划发布为 public 的学习仓库。不要提交：

- 私钥、助记词、API key、JWT、cookie、seed phrase
- 未公开邮箱、手机号、身份证件、住址、公司内部资料
- 真实钱包地址与个人身份的敏感绑定信息
- 未授权课程资料、付费内容全文或他人隐私信息

提交前建议运行：

```bash
git diff --staged
```

## Directory Map

- `profile.md`: 学习者画像、目标和约束
- `learning-plan.md`: 阶段计划、每周节奏和交付物
- `agent-workflow.md`: Coding / learning agent 工作流、确认规则和安全边界
- `daily/`: 每日打卡草稿与复盘
- `tasks/`: 课程任务证明、完成记录和链接
- `experiments/`: AI × Web3 实验记录
- `handbook-feedback/`: Handbook 阅读反馈、疑问和改进建议
- `hackathon/`: Hackathon 方向、方案、原型和提交准备
- `submissions/`: 对外提交草稿，例如 WCB 打卡、任务提交、PR/issue 文案
- `templates/`: daily note、task note、feedback 等模板

## Current Setup

- Cohort: 0
- Repo name: `ai-web3-school-cohort-0`
- Visibility target: public
- Start date: 2026-05-19

## Daily Loop

1. Read: 按 Handbook 或课程任务完成当天输入
2. Build: 做一个小实验、任务证明或文档输出
3. Reflect: 写 `daily/YYYY-MM-DD.md`
4. Submit: 将可公开内容整理到 WCB 或指定平台
5. Feedback: 如果 Handbook 有不清楚或可改进处，记录到 `handbook-feedback/`
