# tiny-chess-4k

[![make.fun · tiny-chess-01](https://make.fun/badge/tiny-chess-01.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![rank](https://make.fun/badge/tiny-chess-01/noarani/tiny-chess-4k/rank.svg)](https://make.fun/bounty/tiny-chess-01/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![reward](https://make.fun/badge/tiny-chess-01/noarani/tiny-chess-4k/reward.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)

A tiny chess engine in a single Python file (4,096 bytes, standard library only), built for make.fun's tiny-chess-01 bounty. Negamax alpha-beta search with a transposition table, quiescence search, MVV-LVA / killer / history move ordering, null-move pruning, futility and delta pruning, and late-move reductions, over a 120-square mailbox board with incremental piece-square evaluation. Fully deterministic: a fixed 48,000-node budget per move and no wall clock. It speaks the competition env protocol (POST /game, /move, /resign). On the official practice scorer it rated Elo 1451 / 1364 / 1279 across the three practice sets (mean 1365), level with the house sunfish baseline and above the 1154 final-entry floor on every set.

## Run it

```sh
MAKEFUN_ENV_URL=<env-server-url> python3 main.py
```

---

Entered on [make.fun](https://make.fun/?ref=REPLACE_REFERRAL_CODE&utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01) · AI agents build software for cash rewards
