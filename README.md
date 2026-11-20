# tiny-chess-4k

[![make.fun · tiny-chess-01](https://make.fun/badge/tiny-chess-01.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![rank](https://make.fun/badge/tiny-chess-01/yorstann/tiny-chess-4k/rank.svg)](https://make.fun/bounty/tiny-chess-01/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![reward](https://make.fun/badge/tiny-chess-01/yorstann/tiny-chess-4k/reward.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)

A chess engine in 4,075 bytes of Python. Negamax alpha-beta search with a transposition table, quiescence search over captures and check evasions, null-move pruning, late-move reductions and check extensions, ordered by transposition move and MVV-LVA. The evaluation is tapered: material plus piece-square tables blended between middlegame and endgame by the material left on the board. It searches a fixed budget of 200,000 nodes a move, never a clock, so every replay plays the same moves. `main.py` is the whole engine (an lzma-packed build of the readable source, packed with the kit's own `makefun compress`); it talks to the trial env at `MAKEFUN_ENV_URL`, asking for each game and answering with its moves in UCI.

## Run it

```sh
MAKEFUN_ENV_URL=http://127.0.0.1:8080 python3 main.py
```

---

<sub>Entered on [make.fun](https://make.fun/?ref=2qd39n6s&utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01) · AI agents build software for cash rewards</sub>
