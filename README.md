# Assignment 7 - Consensus and Forks Lab 

## What this covers

Part A of the briefly covers the below:

- Simulate at least three nodes (A, B, C) that can hold potentially divergent chains.
- Create a fork (two valid competing blocks or chains) and resolve it using the longest-chain rule, or heaviest-work if cumulative proof-of-work is implemented.
- Document edge cases: ties, delayed block arrival, and what confirmation depth might mean for a payment of R10,000 equivalent.
- Submit one group PDF (4 to 6 pages) and one repository, including a short contribution statement per member.

## Contents

- `Assignment7_PartA_Consensus_and_Forks.ipynb` - the notebook used to build and demonstrate the consensus logic.
- `Assignment 7 - Group Assignment.pdf` - the PDF contains explainations how each sub-part of Part A is answered, as well as Part B and C.
- `requirements.txt` - Python dependencies needed to run the notebook.

## How to run

```bash
python -m venv .venv
source .venv/bin/activate      # Windows: .venv\Scripts\activate
pip install -r requirements.txt
jupyter notebook Assignment7_PartA_Consensus_and_Forks.ipynb
```

Run every cell in order. The notebook is fully self-contained and does not require any external services.

## Design decisions carried into the report

- Fork resolution rule: `chain_work` (cumulative proof-of-work difficulty), which coincides with the longest-chain rule under the notebook's uniform classroom difficulty.
- Tie-break policy: the chain with the lexicographically smaller tip hash wins, applied only when two or more valid chains have equal work.
- Confirmation depth: `k = H - h + 1`, where a payment is included at height `h` and the current tip is at height `H`.

## Contribution statement
- `<Thapelo Raseu and Lindokuhle Nsibande>`: Worked together on Part A.
- `<Ntumeleng Singo and SiphoKazi Magaga>`: Worked together on Part B.
- `<Ontshiametse Aphane>`: Worked on Part C

