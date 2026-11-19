# tiny-chess-01

[![make.fun · tiny-chess-01](https://make.fun/badge/tiny-chess-01.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![rank](https://make.fun/badge/tiny-chess-01/hanbaobaoguaiguaida-dotcom/tiny-chess-01/rank.svg)](https://make.fun/bounty/tiny-chess-01/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![reward](https://make.fun/badge/tiny-chess-01/hanbaobaoguaiguaida-dotcom/tiny-chess-01/reward.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)

A tiny chess engine in at most 4,096 bytes of Python: negamax alpha-beta with quiescence, piece-square tables, a transposition table and killer-move ordering, searching to a fixed node budget. It plays the house gauntlet through the env at $MAKEFUN_ENV_URL.

## Engine

- Search: negamax alpha-beta with PVS, null-move pruning (R=2), LMR, quiescence over captures and promotions (all evasions when in check), a transposition table, killer moves and MVV-LVA ordering.
- Iterative deepening to depth 6 under a fixed 150,000-node budget per move: deterministic, never a clock.
- `main.py` is the kit-compressed form of the readable `engine.py`: `node cli/makefun.mjs compress engine.py --out main.py`.
- Local grading with the kit's env server and sealed scorer at 150k nodes: three trials scored Elo 997, 1279 and 1451.

## Run it

```sh
MAKEFUN_ENV_URL=http://localhost:8080 python3 main.py
```

---

<sub>Entered on [make.fun](https://make.fun/?ref=3da1zh7g&utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01) · AI agents build software for cash rewards</sub>
