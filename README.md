# Evidence

**Please be aware that the deadline for all submissions (Both PRs and Issues) is set at block height `671,700` on `gon-irisnet-1`. The block height will serve as the ultimate reference for the deadline. Any evidence submissions, or award applications received after this block height will be deemed INVALID and NOT considered for evaluation.**

> **WARNING**
> Please do not modify the names and layout of the sheets in your evidence file. We use program verification, which relies on a unified and fixed template.

- [Evidence](#evidence)
  - [Overview](#overview)
  - [Qualification Evidence Submission](#qualification-evidence-submission)
  - [Task Evidence Submission](#task-evidence-submission)
    - [Supplementary Explanation for Stage 1 Evidence](#supplementary-explanation-for-stage-1-evidence)
      - [A1](#a1)
      - [A2](#a2)
      - [A3](#a3)
      - [A4](#a4)
      - [A5](#a5)
      - [A6](#a6)
    - [Supplementary Explanation for Stage 2 Evidence](#supplementary-explanation-for-stage-2-evidence)
      - [A7~A12](#a7a12)
      - [A13~A20](#a13a20)
    - [Supplementary Explanation for Stage 3 Evidence](#supplementary-explanation-for-stage-3-evidence)
      - [B1~B2](#b1b2)
      - [B3~B4](#b3b4)
      - [B5~B7](#b5b7)
      - [B8](#b8)
      - [B9](#b9)
  - [Claiming Awards](#claiming-awards)
  - [Bug Submission](#bug-submission)

## Overview

This section provides guidance on submitting qualifications, tasks/awards evidence and bug/issue reports for participants in GoN Phase 1 Incentivized Testing.

> In order to verify the authenticity of identity, ensure fairness of the game, and protect participants' rights in receiving points and claiming rewards, please make sure to submit evidence as required.

Given the registration threshold for phase 1, we assume that participants already have a basic understanding of Git operations, including submitting evidence through PR.

The `gon-evidence/template` includes a `template.xlsx` file, which serves as a template for submitting basic information and evidence for game participation.

As the evidence verification program is based on a standard template, please **do not change** the name or layout of any sheets in the `xlsx` file. Any changes on it would result in a failed task validation and no points will be awarded for that task.

## Qualification Evidence Submission

To participate, each individual must first fork the gon-evidence repository and create a directory named after their GitHub username `https://github.com/{USERNAME}`.

```
gon-evidence/
├── README.md
├── template
│   └── evidence.xlsx
├── alice                <- Alice add her directory and evidence
│   └── evidence.xlsx
└── bob                  <- Bob add his directory and evidence
    └── evidence.xlsx
```

Firstly, participants are required to fill the `Info` sheet in the `evidence.xlsx` file with team names, new address created for each test chain, discord handle, and their community (if applicable), and then submit PRs to `gon-evidence`. The organizers will verify and merge eligible PRs. It is important to note that simply copying another participant's address will not be sufficient proof of ownership.

> *Please note that all submissions will be public, so please make sure to **create new addresses of test chains** to participate in the public testing.*

Examples

| TeamName | IRISnetAddress | StargazeAddress | JunoAddress | UptickAddrss | OmniflixAddress | DiscordHandle | Community(If applicable) |
| -------- | -------------- | --------------- | ----------- | ------------ | --------------- | ------------- | ------------------------ |
| GoNer    | iaa            | stars           | juno        | uptick       | omniflix        | GoNer#0000    | Cosmos Hub               |

Additionally, participants must not modify the `evidence.xlsx` files of other participants. Any attempts to do so will result in disqualification. Furthermore, participants should avoid causing merge conflicts and can only add new content to their own `{USERNAME}/evidence.xlsx` files.

## Task Evidence Submission

During the testing, participants are required to add task evidence into their own Info sheet in the `evidence.xlsx` file and then submit PRs to `gon-evidence` for verification and scoring.

To ensure the integrity of the process, we will guide participants through the tasks and provide instructions on how to record their identity on the chain to **prove ownership of their addresses**. It is important to note that simply copying another participant's address will not be sufficient proof of ownership.

When submitting evidence, please indicate which stage it is in the Title. Pull requests may not be merged in a timely manner, and the leaderboard is not updated in real-time. Please be patient.

The verification program will use the participant's evidence folder in the `main` branch of `gon-evidence` as the only basis for program verification.

### Supplementary Explanation for Stage 1 Evidence

In view of the fact that the description in the evidence template is too simple, it may cause misunderstandings for participants. Hereby clarifying the meanings of each column attribute value. Note that the list below corresponds from top to bottom to the left-to-right cell attribute values in the sheet.

#### A1

- `TxHash` tx hash of issuing a class on iris
- `ClassID` the class id on iris

#### A2

- `TxHash` tx hash of minting an nft on iris
- `ClassID` the class id in `A1`
- `NFTID` the nft id you minted

#### A3

- `TxHash` tx hash of interchain-transferring an nft from on iris
- `ClassID` in fact the cw-721 wasm contract deployed on stars or juno 
- `NFTID` the nft id you transferred, should be one of minted nfts in `A2`
- `ChainID` depending on your destination chain

#### A4

- `TxHash` tx hash of interchain-transferring an nft from on iris
- `ClassID` ibc class id queryed on omniflix or uptick
- `NFTID` the nft id you transferred, should be one of minted nfts in `A2`
- `ChainID` depending on your destination chain

#### A5

- `TxHash` tx hash of interchain-transferring an nft from stargaze or juno
- `ClassID` cw-721 wasm contract deployed on stars or juno 
- `NFTID` the id of nft transferred in `A3`
- `ChainID` depending on your source chain: stargaze or juno.

#### A6

- `TxHash` tx hash of interchain-transferring
- `ClassID` ibc class id queryed on omniflix or uptick
- `NFTID` the id of nft transferred in `A3`
- `ChainID` depending on your source chain: omniflix or uptick.

### Supplementary Explanation for Stage 2 Evidence

#### A7~A12

- `ClassID` the id of the final ibc class on iris
- `NFTID` the id of nft

#### A13~A20

- `TxHash`  tx hash of interchain-transferring
- `ChainID`  chain id corresponding to the transaction hash.

### Supplementary Explanation for Stage 3 Evidence

#### B1~B2

For B1 and B2, you need to submit tow tx hashes:
- `row 2` the first successful interchain nft-transfer tx hash on iris.
- `row 3` the last nft transfer (to last owner) tx hash on iris.

#### B3~B4

You don't need to submit evidence for B3 and B4.

#### B5~B7

For B5, B6 and B7, you need to submit tow tx hashes:
- `row 2` the first successful interchain nft-transfer tx hash on iris.
- `row 3` the last nft transfer (to last owner) tx hash on iris.

Note the previous template dosen't contain `B7` sheet, so please add one after `B6`.

#### B8

You don't need to submit evidence for B8.

#### B9

You don't need to submit evidence for B9.

## Claiming Awards

Claim awards by opening an issue in `gon-evidence` . Please add a `award` label and the title should be in the fromart `AWARD: [TEAM NAME] Claim [Award-Id]`.

## Bug Submission

Report bugs by opening an issue in `gon-evidence`. Please add a `bug` label and the title should be in the fromart `BUG: Brief Description`. The detailed description should include information as follows:

```markdown
## Summary of Bug

A clear and concise description of what the bug is.

## Environment

- OS: [insert your operating system name and version here]
- Software version: [insert the name and version of the software where you encountered the bug]

## Steps to Reproduce

Steps to reproduce the behavior:

## Expected and Actual Behavior

A clear and concise description of what you expected to happen and what actually happened.

## Error Stack

If applicable, include any error messages or stack traces that you received when encountering the bug. This will help developers better understand the root cause of the issue and provide a more effective fix.

## Additional Context

Add any other relevant context about the problem here, such as the time and date the bug was encountered, any recent changes or updates to the software or environment, and any other relevant information that may be useful in troubleshooting the issue.
```
