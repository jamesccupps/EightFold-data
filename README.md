# Eightfold play data

This repository holds only data. The game is at [jamesccupps/EightFold](https://github.com/jamesccupps/EightFold); its relay files play records and leaderboard scores here with a token that can write to this repository and nothing else. Until 2026-11-25 the same files lived on the `play-data` branch of the game's repository.

Play records from the public copy of [Eightfold](https://jamesccupps.github.io/EightFold/), filed here by the relay in [`relay/`](https://github.com/jamesccupps/EightFold/tree/main/relay) on the main branch while the game is being tuned.

```
sessions/<YYYY-MM-DD>/<session>.json     one visit: the machine in broad terms, options, the trail through the menus, and every attempt
```

Each attempt has the course, how and where it ended, every press (position and move), timing, score and frame rate. There are no names or addresses in it. `node tools/replay.js <folder>` on the main branch plays the runs back.

```
scores/<YYYY-MM-DD>/<player>-<board>-<stamp>.json   a run posted for the leaderboard, presses included
boards/all.json                                      the leaderboards, built by the action in .github/workflows/boards.yml
boards/checked.json                                  what each posted run came to when it was played back
```

## Boards before 2026-11-25

The game's engine changed on 2026-11-25 (risk routes, ring gaps, new pickups), so every leaderboard started again. The boards as they stood, and the scores behind them, are kept in `archive/engine-c39af8186c/`. A player is identified here only by a one-way hash of the random code their browser keeps (`pid`), in every file, older ones included.
