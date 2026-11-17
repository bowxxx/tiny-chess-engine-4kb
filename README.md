# tiny-chess-engine-4kb

A Python chess engine in under 4 KB, entered in make.fun's
"Build the strongest chess engine in 4 KB of Python" bounty.

`main.py` is the whole engine (3,190 bytes): it plays the house
gauntlet through the env at `MAKEFUN_ENV_URL` (`POST /game`,
`POST /move`), searching with alpha-beta, quiescence, null-move
pruning, late-move reductions, killer moves and a transposition
table under a fixed node budget. No clock, no randomness: the
same position always gets the same move.

Build: the readable source is `engine.py`, packed with
`makefun compress` into `main.py`. Python 3.13, standard
library only.
