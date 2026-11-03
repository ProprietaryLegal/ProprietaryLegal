# PLI Labs — Proprietary Legal Intelligence

Your proprietary work product is your proprietary intelligence.

[Website](https://proprietarylegal.ai) · [PLI Labs](https://proprietarylegal.ai/labs.html) · [Research](https://proprietarylegal.ai/research/index.html) · [Hugging Face](https://huggingface.co/ProprietaryLegal) · [Contact](https://proprietarylegal.ai/contact.html)

## Featured: [Volta sPLIt](https://github.com/ProprietaryLegal/Volta-sPLIt-DeepSeek-V4.1-Flash-1017-8xV100-SXM2-PP2xTP4): ~118 tok/s on eight 2018 V100s

[![decode: ~118 tok/s](https://img.shields.io/badge/decode-~118%20tok%2Fs-2EA043?style=for-the-badge)](https://github.com/ProprietaryLegal/Volta-sPLIt-DeepSeek-V4.1-Flash-1017-8xV100-SXM2-PP2xTP4) [![thinking on: ~121 tok/s](https://img.shields.io/badge/thinking%20on-~121%20tok%2Fs-1F6FEB?style=for-the-badge)](https://github.com/ProprietaryLegal/Volta-sPLIt-DeepSeek-V4.1-Flash-1017-8xV100-SXM2-PP2xTP4) [![context: 524K](https://img.shields.io/badge/context-524K%20per%20request-555555?style=for-the-badge)](https://github.com/ProprietaryLegal/Volta-sPLIt-DeepSeek-V4.1-Flash-1017-8xV100-SXM2-PP2xTP4)

**~118 tok/s decode, ~121 tok/s with thinking on: DeepSeek-V4.1-Flash-1017 on 8x V100-SXM2-32GB.** The whole 249 GB
model, every expert, resident in the HBM2 of eight sm_70 cards from 2018, split pipeline-parallel 2 x tensor-parallel 4
across two NVLink boards. Our port of 1Cat-vLLM #1277 went from 99 to ~118 tok/s in one day, one A/B-tested switch at a
time, with exact outputs. Every patch, measurement and losing idea is published.

| Decode, thinking off | Thinking on | Thinking high, DGX sPLIce's benchmark | After a 500K-token prompt | vs our previous V100 build |
| --- | --- | --- | --- | --- |
| ~118 tok/s | ~121 tok/s | 84.6-87.3 tok/s | 61.7 tok/s | 2.6x per verify round |

<sub>One request at a time, 2026-11-03, 150 W per card, DSpark 5 drafts per round. ~118 / ~121 are ESTIMATED (the measured ~114 / ~117 stack minus a measured −0.871 ms/round kernel change); the other figures are MEASURED. Method, every lever and the test queue are in the <a href="https://github.com/ProprietaryLegal/Volta-sPLIt-DeepSeek-V4.1-Flash-1017-8xV100-SXM2-PP2xTP4">repository</a>.</sub>

[Repository](https://github.com/ProprietaryLegal/Volta-sPLIt-DeepSeek-V4.1-Flash-1017-8xV100-SXM2-PP2xTP4) · [Measurements](https://github.com/ProprietaryLegal/Volta-sPLIt-DeepSeek-V4.1-Flash-1017-8xV100-SXM2-PP2xTP4/blob/main/docs/measurements.md) · [Every lever, won and lost](https://github.com/ProprietaryLegal/Volta-sPLIt-DeepSeek-V4.1-Flash-1017-8xV100-SXM2-PP2xTP4/blob/main/docs/levers.md) · [Test queue](https://github.com/ProprietaryLegal/Volta-sPLIt-DeepSeek-V4.1-Flash-1017-8xV100-SXM2-PP2xTP4/blob/main/docs/roadmap.md) · [Hugging Face card](https://huggingface.co/ProprietaryLegal/Volta-sPLIt-DeepSeek-V4.1-Flash-1017-8xV100-GGUF)

## Also featured: [DGX sPLIce](https://github.com/ProprietaryLegal/DGX-sPLIce-DeepSeek-V4.1-Flash-2xDGX-Spark-2xRTX3090-drafter-x86-offload)

**DGX sPLIce: DeepSeek-V4.1-Flash on 2x DGX Spark + 2x RTX 3090 drafter, x86 offload.** Two NVIDIA DGX Spark (GB10)
nodes serve the model in tensor parallel; an ordinary x86 machine holds the Engram tables in RAM and serves them over
RDMA, and runs the DSpark speculative drafter on a pair of RTX 3090s. The memory this frees on the Sparks goes to KV
cache.

| Prefill, 4K to 256K-token prompts | Structured output, 4 streams | Code, 4 streams | KV pool | Top-1 agreement with the original |
| --- | --- | --- | --- | --- |
| 2,606-2,827 tok/s | 322 tok/s (138 at one) | 192 tok/s | 1,934,490 tokens | 95.9 % (KLD 0.018) |

<sub>sparkDash protocol, production commit <code>ebc29ed8</code>, 2026-10-31, both Sparks at a 2,300 MHz clock cap, 3 repeats, median; agreement: sudoingX's <code>p4_kld.py</code> panel, agentic domain, 2026-10-21. Every number, the losses beside the wins, the raw JSON and the full install guide are in the <a href="https://github.com/ProprietaryLegal/DGX-sPLIce-DeepSeek-V4.1-Flash-2xDGX-Spark-2xRTX3090-drafter-x86-offload">repository</a>.</sub>

[Repository](https://github.com/ProprietaryLegal/DGX-sPLIce-DeepSeek-V4.1-Flash-2xDGX-Spark-2xRTX3090-drafter-x86-offload) · [Benchmarks and comparisons](https://github.com/ProprietaryLegal/DGX-sPLIce-DeepSeek-V4.1-Flash-2xDGX-Spark-2xRTX3090-drafter-x86-offload/blob/main/docs/comparison.md) · [Install guide](https://github.com/ProprietaryLegal/DGX-sPLIce-DeepSeek-V4.1-Flash-2xDGX-Spark-2xRTX3090-drafter-x86-offload/blob/main/docs/install.md) · [Changelog](https://github.com/ProprietaryLegal/DGX-sPLIce-DeepSeek-V4.1-Flash-2xDGX-Spark-2xRTX3090-drafter-x86-offload/blob/main/CHANGELOG.md) · [Hugging Face card](https://huggingface.co/ProprietaryLegal/DeepSeek-V4.1-Flash-2xDGX-Spark-x86-offload)

PLI Labs is the open research arm of Proprietary Legal Intelligence. We publish methods, code, and measured results so you can inspect the work before hiring us. PLI builds AI around a legal organization's own work product, with retrieval, staged workflows, validation, and attorney review.

## DGX sPLIce components

Earlier standalone releases of DGX sPLIce's parts and research, each with its own write-up and measurements. The DGX sPLIce repository carries the production source as it serves today.

| Repository | What it is |
| --- | --- |
| [dsv41-remote-engram-rdma](https://github.com/ProprietaryLegal/dsv41-remote-engram-rdma) | Engram tables served from x86 RAM over RDMA, with exact local fallback |
| [ofl-rdma-transport](https://github.com/ProprietaryLegal/ofl-rdma-transport) | RDMA RC and TCP request/response transport for the Engram and drafter offloads |
| [dsv41-remote-dspark-drafter-3090](https://github.com/ProprietaryLegal/dsv41-remote-dspark-drafter-3090) | Remote DSpark drafter on an x86 RTX 3090 over RDMA; freed Spark memory becomes KV cache |
| [dsv41-dspark-drafter-tp2-nvlink](https://github.com/ProprietaryLegal/dsv41-dspark-drafter-tp2-nvlink) | The DSpark drafter split across two NVLinked RTX 3090s |
| [dsv41-async-hostflag-handoff](https://github.com/ProprietaryLegal/dsv41-async-hostflag-handoff) | Async remote drafting rounds: CUDA-free host flags and a process proxy |
| [dsv41-kv-page-packing-1m](https://github.com/ProprietaryLegal/dsv41-kv-page-packing-1m) | KV page packing, head-memory switches and long-context experiments |
| [dsv41-native-1017-drafter-sm86](https://github.com/ProprietaryLegal/dsv41-native-1017-drafter-sm86) | Native MXFP4/FP8 drafter kernels for RTX 3090 (research, not serving) |
| [dsv41-exact-acceptance-ceiling](https://github.com/ProprietaryLegal/dsv41-exact-acceptance-ceiling) | Exact speculative-acceptance headroom: replay method and aggregates (research) |
| [dsv41-sampled-drafting](https://github.com/ProprietaryLegal/dsv41-sampled-drafting) | Sampled DSpark drafts with exact target-side acceptance (research) |
| [dsv41-longctx-bench-tools](https://github.com/ProprietaryLegal/dsv41-longctx-bench-tools) | Long-context, needle, prefix-identity and RDMA interference tools |
| [dsv41-window-harness](https://github.com/ProprietaryLegal/dsv41-window-harness) | Fenced, paired measurement windows on a production server |
| [dsv41-spark-offload-findings](https://github.com/ProprietaryLegal/dsv41-spark-offload-findings) | Findings: round costs, async deadlocks, NVLink safety, exactness and acceptance |
| [dsv41-offload](https://github.com/ProprietaryLegal/dsv41-offload) | Research archive: every experiment branch up to 2026-10-27 |
| [deepseek-v41-flash-2x-dgx-spark-progress](https://github.com/ProprietaryLegal/deepseek-v41-flash-2x-dgx-spark-progress) | The October 2026 progress report (historical; DGX sPLIce is the current state) |

## V100 serving work

| Repository | What it is |
| --- | --- |
| [Volta-sPLIt-DeepSeek-V4.1-Flash-1017-8xV100-SXM2-PP2xTP4](https://github.com/ProprietaryLegal/Volta-sPLIt-DeepSeek-V4.1-Flash-1017-8xV100-SXM2-PP2xTP4) | **~118 tok/s**: DeepSeek-V4.1-Flash-1017 on 8x V100, PP2 x TP4, every expert resident; full patch series, measurements and test queue (2026-11-03) |
| [deepseek-v4-flash-v100](https://github.com/ProprietaryLegal/deepseek-v4-flash-v100) | DeepSeek-V4-Flash and V4.1-Flash on NVIDIA V100: llama.cpp recipe and quantized-KV fixes (V4); 1Cat-vLLM results so far and patches (V4.1, 2026-11-01) |
| [swift-1.5-v100](https://github.com/ProprietaryLegal/swift-1.5-v100) | Swift 1.5 on four V100s: 1Cat-vLLM serving recipe and a measured comparison with Qwen3.8-27B |
| [V100 research notes](https://github.com/ProprietaryLegal/pli-labs/tree/main/research/v100) | Volta serving research in the pli-labs hub |
| [DeepSeek-V4.1-Flash V100 port](https://huggingface.co/ProprietaryLegal/deepseek-v4.1-flash-sm70) | SM70 port (Hugging Face) |

## Legal-model work

- **Legal model prunes (REAPs):** [MiniMax-M2.7](https://huggingface.co/ProprietaryLegal/minimax-m2.7-legal-reap-0.35), [Qwen3.5](https://huggingface.co/ProprietaryLegal/Qwen3.5-104b-a10b-LegalReap), and [MiniMax-M3](https://huggingface.co/ProprietaryLegal/minimax-m3-legal-reap-0.22). Read each card's evaluation status and license; these releases include research candidates and unhealed previews.
- **[pli-labs](https://github.com/ProprietaryLegal/pli-labs):** the hub that connects our releases, evaluation methods and research.

## Mirrors and forks

Upstream work keeps its credit and licence; follow each link to the original.

| Repository | What it is |
| --- | --- |
| [deepseek-v41-1017-dgx-spark](https://github.com/ProprietaryLegal/deepseek-v41-1017-dgx-spark) | Fork of HeNryous's vLLM serving image and patches for DeepSeek-V4.1-Flash-1017 EXL3 on 2x DGX Spark |
| [dgx-spark-deepseek-v41](https://github.com/ProprietaryLegal/dgx-spark-deepseek-v41) | Fork of sudoingX's DGX Spark launcher with our two optional offload hooks |
| [1Cat-vLLM](https://github.com/ProprietaryLegal/1Cat-vLLM) | Mirror of the V100 / SM70-focused vLLM fork |
| [v100-skinny](https://github.com/ProprietaryLegal/v100-skinny) | Mirror of hand-written NVFP4 W4A16 CUDA kernels for Volta |

## Collaboration

For AI systems using approved frontier APIs, private cloud, or hardware you own, [reach us through the contact page](https://proprietarylegal.ai/contact.html).

Proprietary Legal Intelligence LLC is a technology consultancy, not a law firm, and does not provide legal services or legal advice.
