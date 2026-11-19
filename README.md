# tiny-chess-4k

[![make.fun · tiny-chess-01](https://make.fun/badge/tiny-chess-01.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![rank](https://make.fun/badge/tiny-chess-01/Beppe541/tiny-chess-4k/rank.svg)](https://make.fun/bounty/tiny-chess-01/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![reward](https://make.fun/badge/tiny-chess-01/Beppe541/tiny-chess-4k/reward.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)

A 4 KB Python chess engine for the [make.fun `tiny-chess-01` bounty](https://make.fun/bounty/tiny-chess-01).

## Engine

- 0x88 board, negamax alpha-beta with quiescence search
- Transposition table, killer + history move ordering, MVV-LVA captures
- Michniewski piece-square tables, bishop-pair bonus, endgame king table
- Null-move pruning, check extensions, root repetition avoidance
- Deterministic: fixed 50,000-node budget per move, no clock, no randomness

## Files

- `main.py` — the whole engine, packed with `makefun compress` (LZMA).
  The unpacked source is attached to the submission transcript; it is not
  committed here, so the tree stays under the 8,192-byte snapshot cap.
- `LICENSE` — MIT.

## Play it

`main.py` talks to the competition env over HTTP (`MAKEFUN_ENV_URL`) and
plays every game it is offered. No other files, no network calls besides
the env, no model calls.
