# Evidence

This section provides guidance on submitting qualifications, tasks/awards evidence and bug/issue reports for participants in GoN Phase 1 Incentivized Testing.

> In order to verify the authenticity of identity, ensure fairness of the game, and protect participants' rights in receiving points and claiming rewards, please make sure to submit evidence as required.

Given the registration threshold for phase 1, we assume that participants already have a basic understanding of Git operations, including submitting evidence through PR.

The `gon-evidence/template` includes a `template.xlsx` file, which serves as a template for submitting basic information and evidence for game participation.

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

Firstly, participants are required to fill the `Info` sheet in the `evidence.xlsx file` with team names, new address created for each test chain, discord handle, and their community (if applicable), and then submit PRs to `gon-evidence`. The organizers will verify and merge eligible PRs. It is important to note that simply copying another participant's address will not be sufficient proof of ownership.

> *Please note that all submissions will be public, so please make sure to **create new addresses of test chains** to participate in the public testing.*

Examples
| TeamName | IRISnetAddress | StargazeAddress | JunoAddress | UptickAddrss | OmniflixAddress | DiscordHandle | Community(If applicable) |
| -------- | -------------- | --------------- | ----------- | ------------ | --------------- | ------------- | ------------------------ |
| GoNer    | iaa1           | stars1          | juno1       | uptick1      | omniflix1       | GoNer#0000    | Cosmos Hub               |

Additionally, participants must not modify the `evidence.xlsx` files of other participants. Any attempts to do so will result in disqualification. Furthermore, participants should avoid causing merge conflicts and can only add new content to their own `{USERNAME}/evidence.xlsx` files.

## Task Evidence Submission

During the testing, participants are required to add task evidence into their own Info sheet in the `evidence.xlsx` file and then submit PRs to `gon-evidence` for verification and scoring.

To ensure the integrity of the process, we will guide participants through the tasks and provide instructions on how to record their identity on the chain to prove ownership of their addresses. It is important to note that simply copying another participant's address will not be sufficient proof of ownership.

More details will be coming soon...

## Bug Submission

Coming soon...

## Rewards Claim

Coming soon...
