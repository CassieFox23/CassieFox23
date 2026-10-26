## 🦊 Digging through binaries, one burrow at a time

Hobbyist fox, one Linux box, a few too many reverse-engineering tools. I run the test, show the work, and write it up in plain words.

Every repo on this page is a fork. I'm a tester, so I fork projects to poke at them, not to start my own.

### What I poke at

| Project | What it is | My part |
|---|---|---|
| [REA](https://github.com/morluto/rea) | Reverse engineering with AI agents | Linux tests and code reviews on PRs. [34 issues](https://github.com/morluto/rea/issues?q=is%3Aissue+author%3ACassieFox23) by Oct 2026, 24 of them bugs. Merged: [website dark mode](https://github.com/morluto/rea/pull/1894), [an Electron launch fix](https://github.com/morluto/rea/pull/2705) |
| [rsleigh](https://github.com/ShaneBreazeale/rsleigh) | A decompiler workbench in Rust | [Same output every run](https://github.com/ShaneBreazeale/rsleigh/pull/8), [two `ls` jump tables](https://github.com/ShaneBreazeale/rsleigh/pull/14), [2 bug reports](https://github.com/ShaneBreazeale/rsleigh/issues?q=is%3Aissue+author%3ACassieFox23) |
| [kuna](https://github.com/Noelo-Lab/kuna) | A decompiler built for agents, in Rust | Speed and memory runs on big binaries, [2 bug reports](https://github.com/Noelo-Lab/kuna/issues?q=is%3Aissue+author%3ACassieFox23) |
| [audio.cpp](https://github.com/0xShug0/audio.cpp) | Speech and audio models in pure C++, on ggml | Forked to test it on Linux. Nothing up yet |

### How I test

I read the diff first. Then it gets a real run on my box: the build, the tests, and the thing the PR says it fixes. The result goes on the PR as a comment or a review: what I ran, with exit codes, what I did not run, and the box it ran on. Every post ends with a footer saying what the AI did and that I OK'd it.

As of Oct 2026: [75 PRs I tested or wrote](https://github.com/morluto/rea/discussions/1435#discussioncomment-18855005) have merged. The stats card below counts only the PRs I opened.

### Write-ups

- [REA on Fedora-based Linux](https://github.com/morluto/rea/discussions/1435): Setup notes, gotchas and my test queue.
- [Benchmarks](https://github.com/morluto/rea/discussions/1998): REA's startup on Node 22, 24 and 26, plus five local models.
- [My local model setup](https://github.com/morluto/rea/discussions/2006): Free local models reading REA's output on one 12 GB GPU.
- [kuna, rsleigh and Ghidra on the same three files](https://github.com/morluto/rea/discussions/3858): First speed results, side by side.

My test bench: Nobara Linux 44 (Fedora-based), Ryzen 9 5900X, 32 GB RAM, Radeon RX 6700 XT 12 GB. Node 22, 24 and 26, Ghidra 12.1.4, and local models in llama.cpp.

![Stats card, rebuilt weekly by lowlighter/metrics (MIT)](github-metrics.svg)

<sub>I work with [Claude Code](https://github.com/anthropics/claude-code). It runs the tests and drafts the write-ups. I pick what gets tested, and I read every result before it goes up. 🦊</sub>
