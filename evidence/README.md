# Evidence

This part tells participants how to qualify themselves as GoNers and earn points to win rewards by submitting evidence. 

At the beginning of the registration, we set a one-year Github account threshold for the participants. Thus we assume that the participants are familiar with the operation of Git, and the process of submitting evidence through PR will be a commonplace operation.

## Qualification Evidence

Under the `evidence/template` lies a `template.xlsx` file. It is a template for submitting your addresses and evidence.

Each participant must fork the `gon-testnets` repository and add a directory under `evidence` named by their **github handle(https://github.com/{YOUR-GITHUB-HANDLE})**.

```bash

evidence/
├── README.md
├── template
│   └── evidence.xlsx
├── alice  <- Alice add her directory and evidence
│   └── evidence.xlsx
└── bob    <- Bob add his directory and evidence
    └── evidence.xlsx
```

Participants are required to fill the `Info` sheet in the `evidence.xlsx` and then make their PRs to the `gon-testnets`. Organizers will verify your tasks result against your addresses and evidence submissions.

| TeamName | IRISnetAddress | StargazeAddress | JunoAddress | UptickAddrss | OmniflixAddress |
|----------|----------------|-----------------|-------------|--------------|-----------------|
| GoNer    | iaa1           | stars1          | juno1       | uptick1      | omniflix1       |


Please note that participants shall not modify any other participants' `evidence.xlsx` files. If such commits are found, they are deprived of qualification for rewards. Also, they shall not result in a merge conflict, thus they can only add new content to their own `participant/evidence.xlsx` files.

## Task Evidence Submission

Coming soon...

## Bug Submission

Coming soon...

## Rewards Claim

Coming soon...