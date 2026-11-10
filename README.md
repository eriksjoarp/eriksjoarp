# Hi, I'm Erik 👋

Research engineer, 15 years in research institutes, the last 3 in AI. I like making models run
fast on hardware you can put under a desk, and then skiing it off on a sunny, sparkling slope.

### ⚡ Favourite speedup: same GPU, same model, ~20× faster training

A tiny transformer (228K params) learning modular arithmetic, on one RTX 4090:

```
eager PyTorch            ██                                47 seed-steps/s
+ CUDA graph, no syncs   ███████████▊                     279
+ seeds vectorized       ████████████████████████████████████████  962
```

No new hardware, no new math: just remove every host sync, capture the whole step in one CUDA
graph, and train several seeds in one batched graph. A bigger GPU wouldn't have helped: the GPU
was mostly waiting for Python.

### 🔧 Currently

- Serving a 27B model on one RTX 5090 with **vLLM**: speculative decoding, FP8 / NVFP4 KV cache,
  CUDA graphs, and chasing milliseconds per decode step
- Reading **FlashInfer** attention kernels and sending the bugs I find upstream
- Rule of thumb: profile first (Nsight Systems / Compute), then attack the biggest slice

### 🚀 Upstream

- [flashinfer-ai/flashinfer#9324](https://github.com/flashinfer-ai/flashinfer/pull/9324): cuDNN
  paged prefill benchmark used the wrong KV dtype for FP8

### 🏔️ Off the keyboard

Skiing · low snowy mountains · 42 countries so far

---

🛠️ Python · CUDA · PyTorch · Triton · vLLM · FlashInfer · Linux
