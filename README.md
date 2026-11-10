# Erik Westring

Research engineer. Fifteen years at research institutes, the last three in AI, which is moving
faster than anything I've worked on and I love it. At home I run a desk cluster (three GPUs, one
desk): tuning models, chasing microseconds and staring at Nsight timelines, mostly to find out
what the GPU is waiting for.

Usually it's Python. A tiny transformer learning modular arithmetic, one RTX 4090, same training
loop throughout (seed-steps/s):

```
plain PyTorch                      47   GPU mostly idle, politely waiting
CUDA graph, no host syncs         279
all seeds in one graph            962
async checkpoints                1042   ~22x, same card, same math
```

Currently: a 27B model, one RTX 5090, vLLM, and a strong opinion about every millisecond in the
decode step. Bugs found along the way go upstream, e.g.
[flashinfer#9324](https://github.com/flashinfer-ai/flashinfer/pull/9324).

Off the keyboard: skiing on sunny days, travelling (42 countries, still counting).
