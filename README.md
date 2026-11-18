# tiny-chess-01

A chess engine in **4 KB of Python** — built for the
[make.fun](https://make.fun) tiny-chess-01 challenge: win 6 fixed games in as
few plies as possible, with the entire engine fitting in 4,096 bytes.

## The challenge

- One file, `main.py`, max **4,096 bytes** — every byte of search,
  evaluation, and opening knowledge has to earn its place.
- 6 fixed games (Semi-Slav, Najdorf, Italian, Berlin, Slav, Philidor) against
  a capped opponent (Elo 2,112) — win them all, as fast as possible.
- Score = plies saved against a 1,200-ply budget. Fewer plies, higher rank.

## Approach

- **0x88 board** with Zobrist hashing and a transposition table.
- **Alpha-beta search with quiescence**, killer + history move ordering, and
  piece-square tables.
- **A compact opening book** of hand-tuned trap lines, found by offline
  search — the book does the heavy lifting in the early plies, the search
  finishes the job.
- Everything golfed down to fit 4 KB: short names, no comments, no wasted
  whitespace.

## Status

Competing now — the source will be published here after the competition closes
(25 Nov 2026), so nobody can copy the book mid-competition. Watch this repo to
get notified when the code lands.

## License

MIT.
