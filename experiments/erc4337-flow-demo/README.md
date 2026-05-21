# ERC-4337 Flow Learning Demo

## What It Is

这是一个最小可交互 AI 学习产物，主题是 ERC-4337 账户抽象流程。它帮助学习者理解：

- `UserOperation` 和普通交易的区别
- Bundler 为什么存在
- EntryPoint 的 `handleOps()` 在流程中的位置
- Paymaster 如何参与 gas sponsorship
- Smart Account、Bundler、EntryPoint、Paymaster 各自承担什么责任

## How to Use

直接打开：

```text
experiments/erc4337-flow-demo/index.html
```

页面不需要安装依赖、不需要 API Key、不连接钱包、不请求 RPC，也不会发送任何交易。

交互方式：

1. 在「学习问题」里输入自己的困惑。
2. 选择观察角色：学习者、DApp 开发者、Bundler 运营者或 Paymaster 设计者。
3. 选择解释难度：入门或进阶。
4. 开启或关闭 Paymaster 分支。
5. 查看生成的解释、6 步流程、角色责任、风险提醒和 3 道自测题。

## Example

输入：

```text
我不懂为什么 ERC-4337 需要 Bundler
```

输出摘要：

```text
ERC-4337 需要 Bundler，是因为 UserOperation 不是普通以太坊交易；Bundler 负责在链下收集和模拟验证，再把一组有效 UserOperation 通过 EntryPoint 提交到链上。
```

如果开启 Paymaster 分支，流程会显示 Paymaster 验证、押金和失败付费风险；关闭后只展示用户自行覆盖 gas 的路径。

## AI-Assisted vs Human-Verified

AI 辅助生成：

- 概念解释模板
- 流程步骤文案
- 角色责任表
- 风险提醒
- 3 道自测题
- WCB 提交草稿

人工修改 / 验证：

- 删除容易让人误以为 demo 会真实调用钱包或链上服务的表述
- 核对核心流程：用户提交 `UserOperation`，Bundler 模拟验证并打包，EntryPoint 通过 `handleOps()` 统一验证和执行，可选 Paymaster 参与 gas sponsorship
- 检查 demo 不包含 API Key、token、私钥、助记词、`.env` 文件或真实钱包敏感信息

## References

- ERC-4337 Documentation: https://docs.erc4337.io/core-standards/erc-4337
- ERC-4337 Spec: https://ercs.ethereum.org/ERCS/erc-4337
- EntryPoint Explainer: https://docs.erc4337.io/smart-accounts/entrypoint-explainer.html
- Bundlers: https://docs.erc4337.io/bundlers/index.html
- Paymasters: https://docs.erc4337.io/paymasters/index.html

## Limitations and Next Steps

- 当前 demo 是离线模板组合，不会实时调用 LLM。
- 当前 demo 不连接测试网，也不会读取真实 `UserOperation`。
- 下一步可以加入可粘贴的真实 UserOperation JSON 解析器。
- 下一步可以加入流程图导出截图，方便提交 proof-of-work。
- 下一步可以加入更多错误案例，例如 signature invalid、nonce mismatch、paymaster rejected。
