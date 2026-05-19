# AI × Web3 School Coding / Learning Agent Workflow

This workflow defines how I use an AI agent to support learning without replacing the learner.

## Role

The agent helps me:

- make daily and weekly learning plans
- explain AI × Web3 concepts in plain language
- generate small exercises and review checklists
- maintain this public learning repo
- organize questions and blockers
- draft daily check-ins, task submissions, and Handbook feedback

The agent does not replace my learning, judgment, or final submissions. I am responsible for reading, deciding, building, submitting, and reviewing the results.

## Fixed Learning Entrypoints

- Learning Agent Prompt: https://aiweb3.school/learning-agent.zh.txt
- Handbook: https://aiweb3.school/zh/handbook/
- WCB AI × Web3 School: https://web3career.build/zh/programs/AI-Web3-School
- WCB Learning page: https://web3career.build/zh/programs/AI-Web3-School#tab=learning
- Public proof-of-work repo: https://github.com/yoona333/ai-web3-school-cohort-0

## Daily Workflow

1. Check WCB learning page for today's course, task, meeting, and submission entry.
2. Check the related Handbook chapter.
3. Ask the agent for three paths:
   - minimum path: what must be done today
   - recommended path: a solid 2-3 hour learning loop
   - challenge path: optional extension if time and energy allow
4. Complete the learning or exercise myself.
5. Ask the agent to draft `daily/YYYY-MM-DD.md`.
6. Ask the agent to draft WCB check-in or task submission text.
7. Manually submit on WCB.
8. Record the submission link or status back into the repo.

## GitHub Proof-of-Work Workflow

The repo is the public record of learning progress. Typical artifacts include:

- daily notes in `daily/`
- task proof in `tasks/`
- experiments in `experiments/`
- Handbook feedback in `handbook-feedback/`
- Hackathon preparation in `hackathon/`
- WCB submission drafts in `submissions/`

Before any repo change, the agent should explain what will be changed. After changes, the agent should run:

```bash
git status --short
git diff --stat
git diff
```

The agent may commit and push only after I confirm the change scope.

## Human Confirmation Rules

The agent must get my confirmation before:

- creating or changing files
- creating a repo
- committing
- pushing
- submitting to WCB or any external platform
- updating profile data
- creating issues, pull requests, or public comments
- running commands that change account, wallet, chain, or platform state

## Safety Boundaries

The agent must not receive, store, or expose:

- API keys
- tokens
- private keys
- seed phrases
- wallet recovery phrases
- `.env` files
- cookies or session secrets
- non-public personal information

The agent must not automatically perform:

- wallet signatures
- transfers
- approvals
- contract writes
- token operations
- mainnet transactions
- WCB API writes

For wallet, contract, API, or account operations, the default mode is explanation, checklist, and human confirmation only.

## Handbook Feedback Workflow

When I find a question, typo, outdated section, unclear concept, or missing example:

1. Record the Handbook URL and section.
2. Classify the feedback as `question`, `typo`, `improvement`, or `proposal`.
3. Draft the feedback in `handbook-feedback/`.
4. Keep quotes short and avoid copying long source text.
5. Submit manually through the official issue, PR, or community channel.
6. Add the submitted link back to the feedback note.

## WCB Submission Workflow

The agent can prepare:

- proof links
- short proof descriptions
- review checklists
- submission drafts

The learner manually opens WCB, submits the proof, and confirms the result. After submission, the repo should record:

- submitted at
- submitted to
- proof link
- WCB status or submission URL, if available

## Default Daily Timebox

My default learning time is 2-3 hours per day:

- 10 minutes: define today's goal
- 60-90 minutes: read or follow course material
- 45-60 minutes: exercise, experiment, or proof-of-work
- 20-30 minutes: write notes and WCB draft
- 5 minutes: check for Handbook feedback

