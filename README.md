# PLI Labs — Proprietary Legal Intelligence

Your proprietary work product is your proprietary intelligence.

**Nick Mermiges, Esq.** is a trial lawyer in Columbia, South Carolina, with more than eleven years of civil litigation, trials and appeals, and the founder of Proprietary Legal Intelligence. He runs his own litigation practice on AI every day and helps small and mid-sized civil litigation firms find where their work backs up and fix it. PLI Labs publishes the open research from that work: everything here was built first inside a working trial practice, on hardware he owns.

[Website](https://proprietarylegal.ai) · [Claude workflows](https://proprietarylegal.ai/frontier.html) · [Local models](https://proprietarylegal.ai/local.html) · [PLI Labs](https://proprietarylegal.ai/labs.html) · [Research](https://proprietarylegal.ai/research/index.html) · [Hugging Face](https://huggingface.co/ProprietaryLegal) · [Contact](https://proprietarylegal.ai/contact.html)

**In the press:** Tom's Hardware, November 9, 2026, by Shane Downing, on the eight-V100 build: [Lawyer builds private AI server with eight used Nvidia V100 GPUs — up to 215 tokens per second to keep legal files offline, costing about $2,400 per four-GPU board](https://www.tomshardware.com/tech-industry/artificial-intelligence/lawyer-builds-private-ai-server-with-eight-used-nvidia-v100-gpus-up-to-215-tokens-per-second-to-keep-legal-files-offline-costing-about-usd2-400-per-four-gpu-board).

## The builds

Every build serves DeepSeek-V4.1-Flash-1017 on hardware you can own. Each card shows figures MEASURED on that
build's own bench; its repository gives the method, the conditions and the losses beside the wins.

### [Volta 12X AmPLIfy](https://github.com/ProprietaryLegal/Volta-12X-AmPLIfy-DeepSeek-V4.1-Flash-1017-NVFP4-12xV100-SXM2-PP3xTP4)

Every routed expert at NVIDIA's NVFP4 precision on twelve cards, three pipeline stages of four.

[![Volta 12X AmPLIfy: 12x V100-SXM2-32GB; all 15,360 routed experts at NVFP4 precision on the cards; 130 tok/s for one request on fresh text, 179 when copying text, at 200 W; prompt reading 3,850 tok/s at 61K, a 426K prompt's first token after 173 s; four requests together 312 tok/s in sum](assets/volta-12x-amplify.svg)](https://github.com/ProprietaryLegal/Volta-12X-AmPLIfy-DeepSeek-V4.1-Flash-1017-NVFP4-12xV100-SXM2-PP3xTP4)

### [Volta Max uPLIft](https://github.com/ProprietaryLegal/Volta-Max-uPLIft-FP4-DeepSeek-V4.1-Flash-1017-NVFP4-8xV100-SXM2-PP2xTP4)

As much of the routed work at NVIDIA's NVFP4 precision as fits on eight cards, every expert on the cards.

[![Volta Max uPLIft: 8x V100-SXM2-32GB; same next token as NVIDIA's NVFP4 pack on 95.1 % of tokens; 143 to 180 tok/s on code and 95 to 97 on legal-style text, one request; 176 to 192 tok/s for three requests together, same tokens as alone; first token after 108 s at 256K, 0.69 s to resume at 100K](assets/volta-max-uplift.svg)](https://github.com/ProprietaryLegal/Volta-Max-uPLIft-FP4-DeepSeek-V4.1-Flash-1017-NVFP4-8xV100-SXM2-PP2xTP4)

### [Volta sPLIt](https://github.com/ProprietaryLegal/Volta-sPLIt-DeepSeek-V4.1-Flash-1017-8xV100-SXM2-PP2xTP4)

The whole 249 GB model resident on eight 2018 cards.

[![Volta sPLIt: 8x V100-SXM2-32GB; about 200 tok/s on code and JSON; 105 to 118 on legal text; prompt reading 2,200 tok/s, first token 59 s at 128K; LegalBench 0.716 balanced accuracy over 22 tasks, MMLU-Pro 79.9 %](assets/volta-split.svg)](https://github.com/ProprietaryLegal/Volta-sPLIt-DeepSeek-V4.1-Flash-1017-8xV100-SXM2-PP2xTP4)

### [Volta Full NVFP4](https://github.com/ProprietaryLegal/Volta-Full-NVFP4-DeepSeek-V4.1-Flash-8xV100)

Every routed expert at exactly NVFP4 precision on eight cards, the less-used ones served from host RAM.

[![Volta Full NVFP4: 8x V100-SXM2-32GB plus host RAM; all 15,360 routed experts at exactly NVFP4 precision; 28 to 30 tok/s on legal-style text, 19 to 20 on general text; a 498,099-token prompt read in 326.6 s; MMLU 83.8 % of 513 questions](assets/volta-full-nvfp4.svg)](https://github.com/ProprietaryLegal/Volta-Full-NVFP4-DeepSeek-V4.1-Flash-8xV100)

### [DGX sPLIce](https://github.com/ProprietaryLegal/DGX-sPLIce-DeepSeek-V4.1-Flash-2xDGX-Spark-2xRTX3090-drafter-x86-offload)

Two DGX Sparks serve the model; an x86 machine holds the Engram tables in RAM over RDMA and runs the drafter on two RTX 3090s.

[![DGX sPLIce: 2x DGX Spark, 2x RTX 3090 and one x86 host; 322 tok/s on JSON output with four streams, 138 on one; prompt reading 2,606 to 2,827 tok/s from 4K to 256K; a KV pool of 1,934,490 tokens; top-1 agreement with the original model 95.9 %](assets/dgx-splice.svg)](https://github.com/ProprietaryLegal/DGX-sPLIce-DeepSeek-V4.1-Flash-2xDGX-Spark-2xRTX3090-drafter-x86-offload)
## More

Components, earlier builds and mirrors of upstream work are under
[all repositories](https://github.com/ProprietaryLegal?tab=repositories).

PLI Labs is the open research arm of Proprietary Legal Intelligence. We publish methods, code and measured results
so you can inspect the work before hiring us. For AI systems on approved frontier APIs, private cloud or hardware
you own, [reach us through the contact page](https://proprietarylegal.ai/contact.html).

Proprietary Legal Intelligence LLC is a technology consultancy, not a law firm, and does not provide legal services or legal advice.
