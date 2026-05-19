# WCB Submission Draft: Account Types Comparison

## Proof Link

```text
https://github.com/yoona333/ai-web3-school-cohort-0/blob/main/tasks/2026-05-20-account-types-comparison.md
```

## Text Explanation

```text
我完成了一份 EOA、智能账户和多签账户的权限差异比较笔记，重点理解“谁能发起交易、谁能批准、谁承担风险”。

笔记比较了控制权、谁可以发起交易、是否支持多人确认、是否支持恢复/限额/自动化、典型使用场景、主要风险点和风险承担者。每类账户都包含至少一个适用场景和一个风险点。

我的结论是：EOA 简单但单私钥风险高；智能账户可编程，适合恢复、限额、session key 和自动化策略，但依赖合约与模块安全；多签账户适合团队金库和合约管理，能降低单点控制风险，但要认真设计 owner 和 threshold。

我也列出了必须人工确认的操作：创建/导入钱包、选择网络、检查收款地址和金额、签名、授权、变更多签 owner/threshold、启用模块/恢复/自动化、部署或写入合约、提交 WCB proof。笔记不包含私钥、助记词、API Key、token、.env 文件或真实资产敏感信息。
```

## Submission Checklist

- [ ] Open WCB task page.
- [ ] Paste the proof link.
- [ ] Paste the text explanation if a notes field is available.
- [ ] Submit manually.
- [ ] Record WCB submission status here.

## Submission Record

- Submitted at: TODO
- WCB submission link / status: TODO

