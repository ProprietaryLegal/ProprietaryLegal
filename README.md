# PLI Labs — Proprietary Legal Intelligence

Your proprietary work product is your proprietary intelligence.

[Website](https://proprietarylegal.ai) · [PLI Labs](https://proprietarylegal.ai/labs.html) · [Research](https://proprietarylegal.ai/research/index.html) · [Hugging Face](https://huggingface.co/ProprietaryLegal) · [Contact](https://proprietarylegal.ai/contact.html)

PLI Labs is the open research arm of Proprietary Legal Intelligence. We publish methods, code, and measured results so you can inspect the work before hiring us. PLI builds AI around a legal organization's own work product, with retrieval, staged workflows, validation, and attorney review.

## What we publish

- **Legal model prunes (REAPs):** [MiniMax-M2.7](https://huggingface.co/ProprietaryLegal/minimax-m2.7-legal-reap-0.35), [Qwen3.5](https://huggingface.co/ProprietaryLegal/Qwen3.5-104b-a10b-LegalReap), and [MiniMax-M3](https://huggingface.co/ProprietaryLegal/minimax-m3-legal-reap-0.22). Read each card's evaluation status and license; these releases include research candidates and unhealed previews.
- **Owned-hardware serving:** [V100 research](https://github.com/ProprietaryLegal/pli-labs/tree/main/research/v100), [Swift 1.5 on V100](https://github.com/ProprietaryLegal/swift-1.5-v100), [DeepSeek-V4-Flash on V100](https://github.com/ProprietaryLegal/deepseek-v4-flash-v100), and the [DeepSeek-V4.1-Flash V100 port](https://huggingface.co/ProprietaryLegal/deepseek-v4.1-flash-sm70).
- **Tools and findings:** source packages, serving recipes, benchmarks, correctness checks, and negative results. Each release states its tested conditions and limits.

## DeepSeek-V4.1-Flash: two DGX Spark (GB10) nodes + x86 offload

An x86 offload host with RTX 3090s supplies host-memory Engram tables and remote drafting. Status reflects the published cards on 2026-10-23; the new acceptance-ceiling entry extends the published findings.

| Repository | What it provides | Status |
| --- | --- | --- |
| [DeepSeek-V4.1-Flash-2xDGX-Spark-x86-offload](https://github.com/ProprietaryLegal/DeepSeek-V4.1-Flash-2xDGX-Spark-x86-offload) | Architecture, configuration, and combined results | Production: one-card async drafter |
| [dsv41-async-hostflag-handoff](https://github.com/ProprietaryLegal/dsv41-async-hostflag-handoff) | CUDA-free handoff and process proxy for GB10 | Production: one-card worker |
| [dsv41-remote-dspark-drafter-3090](https://github.com/ProprietaryLegal/dsv41-remote-dspark-drafter-3090) | Remote drafting; freed Spark memory becomes KV cache | Production |
| [dsv41-dspark-drafter-tp2-nvlink](https://github.com/ProprietaryLegal/dsv41-dspark-drafter-tp2-nvlink) | DSpark worker split across an NVLinked RTX 3090 pair | Opt-in: measured; promotion pending |
| [dsv41-remote-engram-rdma](https://github.com/ProprietaryLegal/dsv41-remote-engram-rdma) | Engram tables served from host RAM over RDMA | Production |
| [ofl-rdma-transport](https://github.com/ProprietaryLegal/ofl-rdma-transport) | RDMA and TCP request/response transport | Production |
| [dsv41-native-1017-drafter-sm86](https://github.com/ProprietaryLegal/dsv41-native-1017-drafter-sm86) | Native-format drafter kernels on RTX 3090 | Opt-in research: strict fidelity gate failing, fix in progress |
| [dsv41-kv-page-packing-1m](https://github.com/ProprietaryLegal/dsv41-kv-page-packing-1m) | KV page packing and a 1M-token context limit (overlay on the upstream image) | KV page packing validated on GB10 at 327,680 (production promotion pending); 524,288 serves correctly but is held for a prefill regression under investigation. 1M untested on GB10. |
| [dsv41-longctx-bench-tools](https://github.com/ProprietaryLegal/dsv41-longctx-bench-tools) | Long-context timing, interference, and failure tools | Research: proven measurement tools |
| [dsv41-exact-acceptance-ceiling](https://github.com/ProprietaryLegal/dsv41-exact-acceptance-ceiling) | Exact replay method for speculative-acceptance headroom | Research |
| [dsv41-spark-offload-findings](https://github.com/ProprietaryLegal/dsv41-spark-offload-findings) | Findings, failure analysis, and limits | Research |

[HF stack overview](https://huggingface.co/ProprietaryLegal/DeepSeek-V4.1-Flash-2xDGX-Spark-x86-offload) · [HF collection](https://huggingface.co/collections/ProprietaryLegal/deepseek-v41-flash-on-2x-dgx-spark-x86-offload-6adab604a517b426ded3916e) · [Research hub](https://github.com/ProprietaryLegal/pli-labs/tree/main/research/dgx-spark-offload)

## Sources and collaboration

The [pli-labs hub](https://github.com/ProprietaryLegal/pli-labs) connects our releases and research. Our Spark forks build on [HeNryous's serving image and patches](https://github.com/ProprietaryLegal/deepseek-v41-1017-dgx-spark) and [sudoingX's recipe](https://github.com/ProprietaryLegal/dgx-spark-deepseek-v41). Their work retains its upstream credit and licenses.

For AI systems using approved frontier APIs, private cloud, or hardware you own, [reach us through the contact page](https://proprietarylegal.ai/contact.html).

Proprietary Legal Intelligence LLC is a technology consultancy, not a law firm, and does not provide legal services or legal advice.
