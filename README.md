## 🦊 Digging through binaries, one burrow at a time

Hobbyist on one Linux box, with a few too many reverse-engineering tools. I run the test, show the work, and write it up in plain words.

Mostly I test other people's projects, so most repos here are forks I poke at. One is my own.

### My own

[a10e-firmware](https://github.com/CassieFox23/a10e-firmware) (GPL-3.0): Why my locked Galaxy A10e won't take LineageOS. Read from its stock firmware. Scripts and a full write-up, plus [the short version](https://github.com/morluto/rea/discussions/7872).

### What I poke at

| Project | What it is | My part |
|---|---|---|
| [REA](https://github.com/morluto/rea) (MIT) | Reverse engineering with AI agents | Linux tests and [203 code reviews](https://github.com/morluto/rea/pulls?q=is%3Apr+reviewed-by%3ACassieFox23+-author%3ACassieFox23) on PRs. [35 issues](https://github.com/morluto/rea/issues?q=is%3Aissue+author%3ACassieFox23), 24 of them bugs. [6 PRs merged](https://github.com/morluto/rea/pulls?q=is%3Apr+author%3ACassieFox23+is%3Amerged), like [website dark mode](https://github.com/morluto/rea/pull/1894) and [an Electron launch fix](https://github.com/morluto/rea/pull/2705). Counts as of Nov 2026 |
| [rsleigh](https://github.com/ShaneBreazeale/rsleigh) (Apache-2.0) | A decompiler workbench in Rust | [Same output every run](https://github.com/ShaneBreazeale/rsleigh/pull/8), [two `ls` jump tables](https://github.com/ShaneBreazeale/rsleigh/pull/14). [2 bug reports](https://github.com/ShaneBreazeale/rsleigh/issues?q=is%3Aissue+author%3ACassieFox23) |
| [kuna](https://github.com/Noelo-Lab/kuna) (Apache-2.0) | A decompiler built for agents, in Rust | Speed and memory runs on big binaries, [2 bug reports](https://github.com/Noelo-Lab/kuna/issues?q=is%3Aissue+author%3ACassieFox23) |
| [audio.cpp](https://github.com/0xShug0/audio.cpp) (Apache-2.0) | Speech and audio models in pure C++, on ggml | Forked to test it on Linux. Nothing up yet |

### How I test

I read the diff first. Then it gets a real run on my box: the build, the tests, and the thing the PR says it fixes. The result goes on the PR as a comment or a review: what I ran, with exit codes, what I did not run, and the box it ran on. Every post ends with a footer saying what the AI did and that I OK'd it.

As of Oct 2026: [82 PRs I tested or wrote](https://github.com/morluto/rea/discussions/1435#discussioncomment-18855005) have merged.

### Write-ups

- [REA on Fedora-based Linux](https://github.com/morluto/rea/discussions/1435): Setup notes, gotchas and my test queue.
- [Benchmarks](https://github.com/morluto/rea/discussions/1998): REA's startup on Node 22, 24 and 26, plus five local models.
- [My local model setup](https://github.com/morluto/rea/discussions/2006): Free local models reading REA's output on one 12 GB GPU.
- [A 32K local model drove REA over MCP](https://github.com/morluto/rea/discussions/3098): 3 of 3 with 10 tools.
- [kuna, rsleigh and Ghidra on the same three files](https://github.com/morluto/rea/discussions/3858): First speed results, side by side.

My test bench: Nobara Linux 44 (Fedora-based), Ryzen 9 5900X, 32 GB RAM, Radeon RX 6700 XT 12 GB. Node 22, 24 and 26, Ghidra 12.1.4 (Apache-2.0), and local models in llama.cpp (MIT).

<sub>I work with [Claude Code](https://github.com/anthropics/claude-code). It runs the tests and drafts the write-ups. I pick what gets tested, and I read every result before it goes up. 🦊</sub>
