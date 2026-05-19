# Account Types Comparison: EOA, Smart Account, and Multisig Account

## Metadata

- Date: 2026-05-20
- Source: WCB AI × Web3 School task
- Status: ready to submit manually
- Proof type: GitHub Markdown note
- Related links:
  - Ethereum accounts: https://ethereum.org/developers/docs/accounts/
  - ERC-4337: https://ercs.ethereum.org/ERCS/erc-4337
  - Safe smart account concepts: https://docs.safe.global/advanced/smart-account-concepts
  - Safe overview: https://docs.safefoundation.org/smart-account/overview

## Short Definitions

- EOA: Externally Owned Account. It is controlled by a private key. A normal wallet address in MetaMask or similar wallets is usually an EOA.
- Smart account: A contract-based account whose permissions and transaction validation can be defined by smart contract logic.
- Multisig account: A contract-based account that requires multiple owners or signers to approve a transaction before execution. In practice, a multisig is often one kind of smart account.

## Comparison Table

| Dimension | EOA | Smart Account | Multisig Account |
| --- | --- | --- | --- |
| Who holds control | Whoever controls the private key or seed phrase controls the account. | The account contract controls execution according to its validation rules; owners, guardians, modules, or session keys may be part of those rules. | A group of owners controls the account through a threshold, such as 2-of-3 or 3-of-5. |
| Who can initiate transactions | The private key holder signs and broadcasts transactions directly. | A user, app, relayer, bundler, or automation service may submit a transaction request, but the smart account executes only if validation logic accepts it. | Usually an owner creates or signs a transaction proposal; execution happens only after enough owner confirmations. |
| Supports multi-person confirmation | Not natively. It can only be simulated with external services or by moving funds into another account type. | Optional. The contract can implement single-owner, guardian, multisig, role-based, or session-key rules. | Yes. Multi-person confirmation is the core feature. |
| Recovery, limits, automation | No native recovery or spending limits. If the key is lost, access is usually lost. | Can support social recovery, spending limits, session keys, allowlists, scheduled actions, paymasters, or automated rules if implemented safely. | Can support owner replacement, threshold changes, modules, guards, and spending policies, depending on the multisig implementation. |
| Typical use case | Personal wallet, testnet practice, simple transfers, direct contract interaction. | Consumer wallet UX, game wallets, apps needing recovery, gas sponsorship, session keys, or policy-based permissions. | DAO treasury, team funds, protocol admin keys, shared project wallet, high-value operations needing group approval. |
| Main risk points | Single key loss, seed phrase leak, phishing signature, wrong network/address, unlimited approvals. | Contract bugs, unsafe upgradeability, malicious modules, bad recovery design, relayer/paymaster assumptions, confusing signature prompts. | Signer collusion, lost signer keys, threshold too low or too high, compromised owners, malicious modules, slow emergency response. |
| Who bears risk | Mainly the private key holder. | The user plus whoever configures or controls the account logic, modules, guardians, or upgrade path. | The signer group and the organization using the account. Risk is shared, but bad governance can still lose funds. |

## Security Boundaries in My Own Words

EOA is the simplest model: one key, one account. It is easy to understand and cheap to use, but the security boundary is thin. If the key or seed phrase is exposed, the account is gone.

Smart accounts move part of the security model into code. That makes better UX possible, such as recovery, limits, automation, and sponsored gas, but the user must trust the account contract, modules, and configuration. A smart account can be safer than an EOA if configured well, or riskier if the code or permissions are misunderstood.

Multisig accounts are best when one person should not control everything. They reduce single-key risk by requiring several people to approve important actions. The tradeoff is operational complexity: signer coordination, threshold design, and emergency procedures matter a lot.

## Suitable Scenarios and Risks

### EOA

- Suitable scenario: A learner uses a testnet wallet to send a small TRX, ETH, or test token transaction and learn how block explorers show hash, gas, block height, and status.
- Risk point: One leaked seed phrase or one malicious approval can compromise the account. There is no native second approval step.

### Smart Account

- Suitable scenario: A user-facing dApp wants wallet recovery, daily spending limits, session keys for games, or gas sponsorship.
- Risk point: The smart account depends on contract logic. Bugs, malicious modules, unsafe upgrade permissions, or confusing automation rules can create hidden risk.

### Multisig Account

- Suitable scenario: A team treasury requires 2-of-3 or 3-of-5 approval before transferring funds or upgrading contracts.
- Risk point: If the threshold is too low, collusion or key compromise is dangerous. If the threshold is too high, the team may be unable to act during emergencies.

## Operations That Must Be Manually Confirmed

The learner must manually confirm:

- creating or importing any wallet
- choosing the network and account type
- checking recipient address, amount, token, and chain
- signing any transaction or message
- approving token spending
- setting or changing multisig owners and thresholds
- enabling modules, guards, recovery methods, session keys, or automation rules
- deploying, upgrading, or writing to a smart contract
- submitting WCB task proof or public comments

The agent can explain, draft, compare, and check. The agent must not receive private keys, seed phrases, API keys, tokens, `.env` files, or perform wallet signing, transfers, approvals, or contract writes.

## Submission Summary

This note compares EOA, smart accounts, and multisig accounts across control, transaction initiation, multi-person approval, recovery/limits/automation, use cases, and risks. My current takeaway is:

- EOA is simple but single-key risk is high.
- Smart account is programmable but depends on contract and module safety.
- Multisig is strong for shared control but depends on threshold and signer governance.

