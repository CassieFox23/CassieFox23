## 🦊 Digging through binaries, one burrow at a time

Hobbyist fox, one Linux box, a few too many reverse-engineering tools. I run the test, show the work, and write it up in plain words.

Every repo on this page is a fork. I'm a tester, so I fork projects to poke at them, not to start my own.

### What I poke at

| Project | What it is | My part |
|---|---|---|
| [REA](https://github.com/morluto/rea) | Reverse engineering with AI agents | Linux tests, [24 bug reports](https://github.com/morluto/rea/issues?q=is%3Aissue+author%3ACassieFox23), [website dark mode](https://github.com/morluto/rea/pull/1894) |
| [rsleigh](https://github.com/ShaneBreazeale/rsleigh) | A decompiler workbench in Rust | [Same output every run](https://github.com/ShaneBreazeale/rsleigh/pull/8), [two `ls` jump tables](https://github.com/ShaneBreazeale/rsleigh/pull/14), [1 bug report](https://github.com/ShaneBreazeale/rsleigh/issues?q=is%3Aissue+author%3ACassieFox23) |
| [kuna](https://github.com/Noelo-Lab/kuna) | A decompiler built for agents, in Rust | [1 bug report](https://github.com/Noelo-Lab/kuna/issues?q=is%3Aissue+author%3ACassieFox23) |

### Write-ups

- [REA on Fedora-based Linux](https://github.com/morluto/rea/discussions/1435): Setup notes, gotchas and my test queue.
- [Benchmarks](https://github.com/morluto/rea/discussions/1998): REA's startup on Node 22, 24 and 26, plus five local models.
- [My local model setup](https://github.com/morluto/rea/discussions/2006): Free local models reading REA's output on one 12 GB GPU.

My test bench runs Nobara Linux, which is Fedora-based. It has Node 22, 24 and 26, Ghidra 12.1.4, and local models in llama.cpp.

<sub>I work with [Claude Code](https://github.com/anthropics/claude-code). It runs the tests and drafts the write-ups. I pick what gets tested and what gets posted. 🦊</sub>
