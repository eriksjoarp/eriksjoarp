# Hi, I'm Erik 👋

Research engineer, 15 years in research institutes, the last 3 in AI. I make models run fast on
desk-sized GPUs.

Same tiny transformer, same training loop, one RTX 4090 (seed-steps/s):

```
stock eager PyTorch                          █                                 47
+ no host syncs, on-GPU metrics, CUDA graph  ████████                         279
+ seeds batched in one graph                 ████████████████████████████     962
+ async checkpoints and metric flush         ██████████████████████████████  1042   ~22×
```

The GPU was mostly waiting for Python.

**Now:** a 27B model on one RTX 5090 with vLLM and FlashInfer: speculative decoding, FP8/NVFP4 KV.
**Upstream:** [flashinfer#9324](https://github.com/flashinfer-ai/flashinfer/pull/9324)
**Off the keyboard:** skiing sunny slopes · snowy mountains · 42 countries
