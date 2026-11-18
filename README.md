# PLI Labs — Proprietary Legal Intelligence

Your proprietary work product is your proprietary intelligence.

[Website](https://proprietarylegal.ai) · [Claude workflows](https://proprietarylegal.ai/frontier.html) · [Local models](https://proprietarylegal.ai/local.html) · [PLI Labs](https://proprietarylegal.ai/labs.html) · [Research](https://proprietarylegal.ai/research/index.html) · [Hugging Face](https://huggingface.co/ProprietaryLegal) · [Contact](https://proprietarylegal.ai/contact.html)

**In the press:** Tom's Hardware, November 9, 2026, by Shane Downing, on the eight-V100 build: [Lawyer builds private AI server with eight used Nvidia V100 GPUs — up to 215 tokens per second to keep legal files offline, costing about $2,400 per four-GPU board](https://www.tomshardware.com/tech-industry/artificial-intelligence/lawyer-builds-private-ai-server-with-eight-used-nvidia-v100-gpus-up-to-215-tokens-per-second-to-keep-legal-files-offline-costing-about-usd2-400-per-four-gpu-board).

## The builds

Every build serves DeepSeek-V4.1-Flash-1017 on hardware you can own. Figures are MEASURED on the build's own bench,
one request at a time unless a row says otherwise; each repository gives the method, the conditions and the losses
beside the wins.

### [Volta Max uPLIft](https://github.com/ProprietaryLegal/Volta-Max-uPLIft-FP4-DeepSeek-V4.1-Flash-1017-NVFP4-8xV100-SXM2-PP2xTP4)

As much of the routed work at NVIDIA's NVFP4 precision as fits on eight cards, every expert on the cards.

| | |
| --- | --- |
| Hardware | 8x V100-SXM2-32GB (2018), two NVLink boards, two pipeline stages of four cards |
| Speed | 143 to 180 tok/s on code, 94.7 to 97.3 on legal-style text |
| Context | First token after 1.0 s at 1K, 54 s at 128K, 108 s at 256K; a follow-up at 100K resumes in 0.69 s |
| Concurrency | Three requests together: 176 to 192 tok/s in all (1.48x to 1.62x one stream), same tokens as alone |
| Accuracy | Same next token as the NVFP4 reference on 95.1 % of tokens (KL 0.079 nats); MMLU 83.6 % of 513 |

### [Volta sPLIt](https://github.com/ProprietaryLegal/Volta-sPLIt-DeepSeek-V4.1-Flash-1017-8xV100-SXM2-PP2xTP4)

The whole 249 GB model resident on eight 2018 cards: the fastest of the eight-card builds.

| | |
| --- | --- |
| Hardware | 8x V100-SXM2-32GB, two NVLink boards, two pipeline stages of four cards, 150 W per card |
| Speed | About 200 tok/s on code and JSON, 105 to 118 on legal text, 85 to 110 on prose and chat |
| Context | Prompt reading up to 2,200 tok/s; first token after 59 s at 128K and 119 s at 256K |
| Concurrency | One request at a time on this build (several together: see Volta Max uPLIft) |
| Accuracy | LegalBench 0.716 balanced accuracy (22 tasks); MMLU-Pro 79.9 %; HumanEval+ 89.6 %; the original model's top next token 89.0 % of the time |

### [Volta Full NVFP4](https://github.com/ProprietaryLegal/Volta-Full-NVFP4-DeepSeek-V4.1-Flash-8xV100)

Every routed expert at exactly NVFP4 precision on the same eight cards, the less-used ones from host RAM: the
reference the other builds are measured against.

| | |
| --- | --- |
| Hardware | 8x V100-SXM2-32GB plus host RAM over PCIe |
| Speed | 28 to 30 tok/s on legal-style text, 19 to 20 on general text |
| Context | A 498,099-token prompt read in 326.6 s |
| Concurrency | One request at a time |
| Accuracy | 44.7 billion expert values checked bit-equal to the NVFP4 formula; MMLU 83.8 % of 513 |

### [DGX sPLIce](https://github.com/ProprietaryLegal/DGX-sPLIce-DeepSeek-V4.1-Flash-2xDGX-Spark-2xRTX3090-drafter-x86-offload)

Two DGX Sparks serve the model; an x86 machine holds the Engram tables in RAM over RDMA and runs the drafter on two
RTX 3090s.

| | |
| --- | --- |
| Hardware | 2x NVIDIA DGX Spark (GB10), 2x RTX 3090, one x86 host |
| Speed | 138 tok/s on structured output for one stream |
| Context | Prompt reading 2,606 to 2,827 tok/s from 4K to 256K; a KV pool of 1,934,490 tokens |
| Concurrency | Four streams: 322 tok/s on structured output, 192 on code |
| Accuracy | Top-1 agreement with the original model 95.9 % (KLD 0.018) |

## More

[All repositories](https://github.com/ProprietaryLegal?tab=repositories) (components, earlier builds, mirrors of
upstream work with their credit) · [pli-labs](https://github.com/ProprietaryLegal/pli-labs) (legal model prunes,
evaluation methods, research) · [Hugging Face](https://huggingface.co/ProprietaryLegal)

PLI Labs is the open research arm of Proprietary Legal Intelligence. We publish methods, code and measured results
so you can inspect the work before hiring us. For AI systems on approved frontier APIs, private cloud or hardware
you own, [reach us through the contact page](https://proprietarylegal.ai/contact.html).

Proprietary Legal Intelligence LLC is a technology consultancy, not a law firm, and does not provide legal services or legal advice.
