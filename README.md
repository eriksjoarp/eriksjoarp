# Hi, I'm Erik 👋

I make large language models run fast on hardware you can put under a desk. Right now that means
squeezing a 27B model, speculative decoding and a quantized KV cache onto one RTX 5090, and
chasing every millisecond per decode step.

### 🔧 Currently

- Tuning **vLLM** serving on Blackwell (SM120): speculative decoding with DFlash and MTP drafters,
  FP8 / NVFP4 KV cache, CUDA graphs
- Digging into **FlashInfer** attention kernels (FMHA v2, cuDNN, TRT-LLM) and sending fixes upstream
- Profiling with Nsight Systems and Nsight Compute: find the critical path, then attack the biggest
  share

### 💡 Interests

- **LLM inference**: kernels, quantization (FP8, NVFP4, W4A16), speculative decoding, KV-cache tricks
- **Local LLMs and AI agents**: running models at home, coding agents, multi-model debate and review
- **Measurement**: honest benchmarks, paired A/B runs, numbers over impressions
- Earlier: computer vision (Swin, EuroSAT satellite imagery), NLP finetuning, RAG pipelines and
  ML-based network intrusion detection

### 🚀 Upstream contributions

- [flashinfer-ai/flashinfer#9324](https://github.com/flashinfer-ai/flashinfer/pull/9324): pass
  `kv_data_type` to the cuDNN paged prefill plan in the attention benchmark

---

🛠️ Python · CUDA · PyTorch · Triton · vLLM · FlashInfer · Linux
