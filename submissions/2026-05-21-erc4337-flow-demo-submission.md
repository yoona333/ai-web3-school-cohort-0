# WCB Submission Draft: ERC-4337 Flow Learning Demo

## Demo Link

```text
https://github.com/yoona333/ai-web3-school-cohort-0/tree/main/experiments/erc4337-flow-demo
```

## Direct Demo File

```text
https://github.com/yoona333/ai-web3-school-cohort-0/blob/main/experiments/erc4337-flow-demo/index.html
```

## Text Explanation

```text
我做了一个最小可交互 AI 学习产物：ERC-4337 流程解释器。它解决的学习问题是：初学者很容易把 UserOperation、Bundler、EntryPoint、Paymaster、Smart Account 混在一起，不知道一次账户抽象操作到底如何从用户意图走到链上执行。

用户可以在静态网页中输入自己的问题，选择观察角色（学习者、DApp 开发者、Bundler 运营者、Paymaster 设计者）、解释难度，并开启或关闭 Paymaster 分支。网页会输出一句话解释、6 步 ERC-4337 流程、角色责任、风险提醒和 3 道自测题。整个 demo 不需要 API Key，不连接钱包，不请求 RPC，也不会发送交易。

输入示例：我不懂为什么 ERC-4337 需要 Bundler。

输出示例：ERC-4337 需要 Bundler，是因为 UserOperation 不是普通以太坊交易；Bundler 负责在链下收集和模拟验证，再把一组有效 UserOperation 通过 EntryPoint 提交到链上。开启 Paymaster 分支时，流程还会显示 Paymaster 验证、押金和失败付费风险。

AI 辅助生成的部分：概念解释模板、流程步骤文案、角色责任表、风险提醒、自测题和提交草稿。

我人工修改 / 验证的部分：核对核心流程是否符合 ERC-4337 官方资料；删除容易让人误以为 demo 会真实调用钱包或链上服务的表述；确认仓库和 demo 不包含 API Key、token、私钥、助记词、.env 文件或真实钱包敏感信息。

限制和下一步：当前 demo 是离线模板组合，不会实时调用 LLM，也不会读取真实 UserOperation。下一步可以加入 UserOperation JSON 解析器、错误案例解释和流程图截图导出。
```

## Submission Checklist

- [ ] Open WCB task page.
- [ ] Paste the demo link.
- [ ] Paste the direct demo file link if a link field or notes field is available.
- [ ] Paste the text explanation if a notes field is available.
- [ ] Submit manually.
- [ ] Record WCB submission link or status here.

## Submission Record

- Submitted at: TODO
- WCB submission link / status: TODO
