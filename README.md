# Hi, I'm Erik 👋

Research engineer, 15 years in research institutes, the last 3 in AI. I make models run fast on
desk-sized GPUs.

```
stock PyTorch          ██                                        47 seed-steps/s
tuned, same GPU        ████████████████████████████████████████ 962  (RTX 4090, ~20×)
```

Same tiny transformer, same training loop. No host syncs, metrics computed on the GPU, the whole
step in one CUDA graph, seeds batched. The GPU was mostly waiting for Python.

**Now:** a 27B model on one RTX 5090 with vLLM and FlashInfer: speculative decoding, FP8/NVFP4 KV.
**Upstream:** [flashinfer#9324](https://github.com/flashinfer-ai/flashinfer/pull/9324)
**Off the keyboard:** skiing sunny slopes · snowy mountains · 42 countries
