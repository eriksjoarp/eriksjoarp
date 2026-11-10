# Erik Westring

I work on LLM inference performance on a single workstation GPU: serving 27B-class models with
vLLM on an RTX 5090 (Blackwell, SM120), and the kernels, quantization and settings around it.

**Focus**

- vLLM serving: speculative decoding (DFlash, MTP drafters), KV-cache dtypes (FP8, NVFP4),
  CUDA graphs, step-time attribution
- FlashInfer attention backends (FMHA v2, cuDNN, TRT-LLM) on consumer Blackwell
- Weight and KV quantization: FP8, NVFP4, W4A16
- Profiling with Nsight Systems / Nsight Compute: kernel and step milliseconds first, full A/B runs
  only when nothing smaller decides

**Upstream contributions**

- [flashinfer-ai/flashinfer#9324](https://github.com/flashinfer-ai/flashinfer/pull/9324):
  pass `kv_data_type` to the cuDNN paged prefill plan in the attention benchmark

Most of my work lives in private repos; fixes that matter beyond my setup go upstream as PRs.
