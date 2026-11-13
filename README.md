# PLI Labs — Proprietary Legal Intelligence

Your proprietary work product is your proprietary intelligence.

[Website](https://proprietarylegal.ai) · [Claude workflows](https://proprietarylegal.ai/frontier.html) · [Local models](https://proprietarylegal.ai/local.html) · [PLI Labs](https://proprietarylegal.ai/labs.html) · [Research](https://proprietarylegal.ai/research/index.html) · [Hugging Face](https://huggingface.co/ProprietaryLegal) · [Contact](https://proprietarylegal.ai/contact.html)

**In the press:** Tom's Hardware, November 9, 2026, by Shane Downing, on the eight-V100 build: [Lawyer builds private AI server with eight used Nvidia V100 GPUs — up to 215 tokens per second to keep legal files offline, costing about $2,400 per four-GPU board](https://www.tomshardware.com/tech-industry/artificial-intelligence/lawyer-builds-private-ai-server-with-eight-used-nvidia-v100-gpus-up-to-215-tokens-per-second-to-keep-legal-files-offline-costing-about-usd2-400-per-four-gpu-board). The article reports the builder's own measurements. The same measurements, with the method, are in the [Volta sPLIt repository](https://github.com/ProprietaryLegal/Volta-sPLIt-DeepSeek-V4.1-Flash-1017-8xV100-SXM2-PP2xTP4).

## Featured: [Volta Max uPLIft](https://github.com/ProprietaryLegal/Volta-Max-uPLIft-FP4-DeepSeek-V4.1-Flash-1017-NVFP4-8xV100-SXM2-PP2xTP4): as much of the routed work at NVFP4 precision as fits, every expert on the cards

[![share of decode work at NVFP4 precision: 79-85 %](https://img.shields.io/badge/share%20of%20decode%20work%20at%20NVFP4%20precision-79--85%20%25-76B900?style=for-the-badge)](https://github.com/ProprietaryLegal/Volta-Max-uPLIft-FP4-DeepSeek-V4.1-Flash-1017-NVFP4-8xV100-SXM2-PP2xTP4) [![same next token as NVIDIA's NVFP4 pack: 95.1 %, Volta sPLIt 92.2 %](https://img.shields.io/badge/same%20next%20token%20as%20NVFP4-95.1%20%25%20(Volta%20sPLIt%2092.2%20%25)-76B900?style=for-the-badge)](https://github.com/ProprietaryLegal/Volta-Max-uPLIft-FP4-DeepSeek-V4.1-Flash-1017-NVFP4-8xV100-SXM2-PP2xTP4#how-close-to-nvfp4) [![experts at NVFP4 precision: 6,087 of 15,360](https://img.shields.io/badge/experts%20at%20NVFP4%20precision-6%2C087%20of%2015%2C360-76B900?style=for-the-badge)](https://github.com/ProprietaryLegal/Volta-Max-uPLIft-FP4-DeepSeek-V4.1-Flash-1017-NVFP4-8xV100-SXM2-PP2xTP4) [![code and JSON, one request at a time: 150-188 tok/s](https://img.shields.io/badge/code%20and%20JSON%2C%20one%20at%20a%20time-150--188%20tok%2Fs-2EA043?style=for-the-badge)](https://github.com/ProprietaryLegal/Volta-Max-uPLIft-FP4-DeepSeek-V4.1-Flash-1017-NVFP4-8xV100-SXM2-PP2xTP4#speed-bench-2026-11-12-final-build) [![legal, one request at a time: 86-106 tok/s](https://img.shields.io/badge/legal%2C%20one%20at%20a%20time-86--106%20tok%2Fs-1F6FEB?style=for-the-badge)](https://github.com/ProprietaryLegal/Volta-Max-uPLIft-FP4-DeepSeek-V4.1-Flash-1017-NVFP4-8xV100-SXM2-PP2xTP4#speed-bench-2026-11-12-final-build) [![prose and chat, one request at a time: 71-89 tok/s](https://img.shields.io/badge/prose%20and%20chat%2C%20one%20at%20a%20time-71--89%20tok%2Fs-8250DF?style=for-the-badge)](https://github.com/ProprietaryLegal/Volta-Max-uPLIft-FP4-DeepSeek-V4.1-Flash-1017-NVFP4-8xV100-SXM2-PP2xTP4#speed-bench-2026-11-12-final-build) [![prompt reading at 128K: 2,295-2,448 tok/s](https://img.shields.io/badge/prompt%20reading%20at%20128K-2%2C295--2%2C448%20tok%2Fs-D29922?style=for-the-badge)](https://github.com/ProprietaryLegal/Volta-Max-uPLIft-FP4-DeepSeek-V4.1-Flash-1017-NVFP4-8xV100-SXM2-PP2xTP4#speed-bench-2026-11-12-final-build) [![experts on the cards in decode: all 15,360](https://img.shields.io/badge/experts%20on%20the%20cards%20in%20decode-all%2015%2C360-555555?style=for-the-badge)](https://github.com/ProprietaryLegal/Volta-Max-uPLIft-FP4-DeepSeek-V4.1-Flash-1017-NVFP4-8xV100-SXM2-PP2xTP4) [![three requests together: 176.2 tok/s, 1.48x one stream](https://img.shields.io/badge/3%20requests%20together-176.2%20tok%2Fs%20(1.48x)-1F6FEB?style=for-the-badge)](https://github.com/ProprietaryLegal/Volta-Max-uPLIft-FP4-DeepSeek-V4.1-Flash-1017-NVFP4-8xV100-SXM2-PP2xTP4#speed-bench-2026-11-13-close-out)
[![legal-style short set, one request at a time on the two-slot default: 94.7 tok/s](https://img.shields.io/badge/legal--style%20short%20set%2C%20one%20at%20a%20time-94.7%20tok%2Fs-1F6FEB?style=for-the-badge)](https://github.com/ProprietaryLegal/Volta-Max-uPLIft-FP4-DeepSeek-V4.1-Flash-1017-NVFP4-8xV100-SXM2-PP2xTP4#speed-bench-2026-11-13-close-out) [![general short set, one request at a time on the two-slot default: 117.7 tok/s](https://img.shields.io/badge/general%20short%20set%2C%20one%20at%20a%20time-117.7%20tok%2Fs-8250DF?style=for-the-badge)](https://github.com/ProprietaryLegal/Volta-Max-uPLIft-FP4-DeepSeek-V4.1-Flash-1017-NVFP4-8xV100-SXM2-PP2xTP4#speed-bench-2026-11-13-close-out)

**DeepSeek-V4.1-Flash-1017 on 8x V100-SXM2-32GB, MEASURED 2026-11-10 at a 1,425 MHz clock ceiling.** Volta Max uPLIft
puts as much of the routed work at NVIDIA's NVFP4 precision as fits on the eight cards, with all routed experts on the
cards (VRAM) in decode. Experts are promoted to exactly NVFP4 precision in order of use per byte until the next does not
fit, and the rest run from compressed IQ2-class records. This maximizes use (the mixed tally's routed counts, in-sample),
not the number of NVFP4 experts. 6,087 of the 15,360 routed experts are at NVFP4, and they carried 79 to 85 % of
decode routes in the measured sets (in-sample). Decode runs at 104 to 127 tok/s on code and 62 to 72 on legal text from
1K to 256K prompts, slower than Volta sPLIt.

**2026-11-13: the close-out.** A follow-up whose previous reply came back changed now resumes from the cache
instead of reading the whole chat again: first token 0.69 s against 31.0 s at 100K tokens, the same output as an
ordinary cache hit at the same position. The two-slot default holds 5,936 experts at NVFP4 (32 MiB more reserve on
stage 1). On the close-out build, one request at a time on the two-slot default, the short sets ran at
117.7 tok/s general and 94.7 legal-style and code decoded at 143 to 175 tok/s from
1K to 256K prompts. Three requests together on a three-slot profile gave 176.2 tok/s (1.48x
one stream), and every request with others running gave the same token ids as the same prompt alone on the same boot (MEASURED 2026-11-13, cards at the default 300 W power limit and 1,530 MHz maximum clock, the power cap was not in force during this bench,
[close-out bench](https://github.com/ProprietaryLegal/Volta-Max-uPLIft-FP4-DeepSeek-V4.1-Flash-1017-NVFP4-8xV100-SXM2-PP2xTP4#speed-bench-2026-11-13-close-out)).

**2026-11-12: several requests at once.** Volta Max uPLIft now serves two prompt slots by default, with one and three
as options (a four-slot profile was measured on 2026-11-12, before the prompt-reading kernels). With three requests running together on the three-slot option it delivers **192.3 tok/s in
all, 1.62x one stream** (118.9 tok/s), and two requests on the two-slot default give 159.0 tok/s (1.34x), with the
same token ids as each prompt alone (MEASURED 2026-11-12, 175 W and 1,522 MHz per card,
[table and limits](https://github.com/ProprietaryLegal/Volta-Max-uPLIft-FP4-DeepSeek-V4.1-Flash-1017-NVFP4-8xV100-SXM2-PP2xTP4#serving-several-requests-at-once-window-18)). Each slot costs NVFP4 experts: 5,949 of 15,360 with two slots, so the share of
decode routes at NVFP4 precision is predicted at about 78 to 85 % (not measured). Prompts are now read the fast way,
86 to 119 s for a first read near 200K tokens against 155 to 165 s. Quality not established for the slot options or
the fast reading: every closeness figure below was measured on the first release, with one slot and native reading.
The repository's launcher also exports two request-path switches taken over from Volta sPLIt (window 16): a system
message sent in the middle of a chat no longer makes the server read the chat again (a 30,779-token chat: 30,752
tokens reused and 0.45 s, against 14.84 s), token for token the same output, decode speed no measurable change.
Since window 17 prompts are read with two bit-equal kernels: same output bits, second reads of a
215,847-token prompt 4.43 s faster.
On the final build, one request at a time on the two-slot default, the short sets ran at 123.2 tok/s general and
97.3 legal-style (101.1 and 81.1 on the previous public bench, the kernel build of 2026-11-11 with one slot and
native reading: build against build, not one change), code decoded at 150 to 180 tok/s from 1K to 256K prompts,
and a 256K prompt got its first token after 108.4 s instead of 207.9 s (MEASURED 2026-11-12, [speed bench](https://github.com/ProprietaryLegal/Volta-Max-uPLIft-FP4-DeepSeek-V4.1-Flash-1017-NVFP4-8xV100-SXM2-PP2xTP4#speed-bench-2026-11-12-final-build)).
On that bench boot the cards of stage 1 went 2 MiB over the build's memory line, with no out-of-memory line.
The speed table and chart below are the final build's. The closeness figures are those of the first release.

**How close to NVIDIA's NVFP4 pack, MEASURED 2026-11-11 at a 1,475 MHz ceiling** (320 contexts and 513 MMLU questions,
greedy, thinking off, rules fixed and published before any capture). Volta Max uPLIft picks the same next token as the
NVFP4 reference (Volta Full NVFP4) on 95.1 % of compared tokens, Volta sPLIt on 92.2 %. Its KL divergence from the
reference is 0.079 nats against Volta sPLIt's 0.196, and on the tokens both builds still share with the reference it
removes 63 % of Volta sPLIt's KL divergence. It changes 1.6 % of the multiple-choice answers, Volta sPLIt 15.4 %.

| How much runs at NVFP4 precision | Volta sPLIt | Volta Max uPLIft | Volta Full NVFP4 |
| --- | --- | --- | --- |
| Share of decode work (routes) at NVFP4 precision | 0 % | **79 to 85 %** (measured sets, in-sample) | 100 % |
| Routed experts at exactly NVFP4 precision | 0 of 15,360 | **6,087 of 15,360** | 15,360 of 15,360 |
| Routed experts on the cards in decode | all | **all** | the most-used, the rest from host RAM |

| How close to the NVFP4 reference | Volta sPLIt | Volta Max uPLIft | Volta Full NVFP4 (the reference) |
| --- | --- | --- | --- |
| Same next token as the reference | 92.2 % | **95.1 %** | repeat: 100 % |
| Mean KL divergence from the reference (nats, top 20, lower bound) | 0.196 | **0.079** | repeat: 0 |
| Multiple-choice answers that differ from the reference | 15.4 % | **1.6 %** | repeat: 0 % |
| Multiple-choice accuracy, 513 MMLU questions | 84.4 % | 83.6 % | 83.8 % |

<sub>Volta sPLIt as captured on 2026-11-10. The reference repeat is the same boot run again on 50 contexts and 50 questions. Both accuracies are not distinguishable from the reference's at this sample size. 37 of Volta sPLIt's 79 changed answers are on the 38 questions the reference left unanswered: on the 475 it answered, the changed shares are 1.7 % and 8.8 % (counted after scoring, outside the preregistered rules). Intervals, verdicts, receipts and the scoring script are in the <a href="https://github.com/ProprietaryLegal/Volta-Max-uPLIft-FP4-DeepSeek-V4.1-Flash-1017-NVFP4-8xV100-SXM2-PP2xTP4#how-close-to-nvfp4">repository</a>.</sub>

[![Greedy continuations that stay identical to the NVFP4 reference: Volta Max uPLIft, Volta sPLIt and the reference's own repeat](https://raw.githubusercontent.com/ProprietaryLegal/Volta-Max-uPLIft-FP4-DeepSeek-V4.1-Flash-1017-NVFP4-8xV100-SXM2-PP2xTP4/main/quality/closeness-test/charts/survival.svg)](https://github.com/ProprietaryLegal/Volta-Max-uPLIft-FP4-DeepSeek-V4.1-Flash-1017-NVFP4-8xV100-SXM2-PP2xTP4#how-close-to-nvfp4)

| Prompt | First token | Code | Structured (JSON) | Legal | Prose | Chat |
| --- | --- | --- | --- | --- | --- | --- |
| 1K | 1.0 s | 150 tok/s | 169 tok/s | 106 tok/s | 81 tok/s | 88 tok/s |
| 32K | 16 s | 165 | 165 | 93 | 78 | 81 |
| 128K | 54 s | 151 | 153 | 87 | 78 | 76 |
| 256K | 108 s | 155 | 150 | 94 | 81 | 71 |

<sub>Final build, MEASURED 2026-11-12: one request at a time on the two-slot default, 175 W and 1,522 MHz per card (the clock ceiling of Volta sPLIt's table of 2026-11-05), thinking off, greedy, 1,024 tokens out, the same prompts and method as the Volta sPLIt table above, mean of 2 runs, greedy outputs byte-identical across runs. Every length from 1K to 256K, the thinking-on rows, the first release's table and the method are in the <a href="https://github.com/ProprietaryLegal/Volta-Max-uPLIft-FP4-DeepSeek-V4.1-Flash-1017-NVFP4-8xV100-SXM2-PP2xTP4#speed-bench-2026-11-12-final-build">repository</a>.</sub>

![Decode speed by prompt length on the final build, one request at a time on the two-slot default, against Volta sPLIt's published bench](https://raw.githubusercontent.com/ProprietaryLegal/Volta-Max-uPLIft-FP4-DeepSeek-V4.1-Flash-1017-NVFP4-8xV100-SXM2-PP2xTP4/main/docs/charts/decode-by-length-final-light.png#gh-light-mode-only)
![Decode speed by prompt length on the final build, one request at a time on the two-slot default, against Volta sPLIt's published bench](https://raw.githubusercontent.com/ProprietaryLegal/Volta-Max-uPLIft-FP4-DeepSeek-V4.1-Flash-1017-NVFP4-8xV100-SXM2-PP2xTP4/main/docs/charts/decode-by-length-final-dark.png#gh-dark-mode-only)

[Repository](https://github.com/ProprietaryLegal/Volta-Max-uPLIft-FP4-DeepSeek-V4.1-Flash-1017-NVFP4-8xV100-SXM2-PP2xTP4) · [Measurements](https://github.com/ProprietaryLegal/Volta-Max-uPLIft-FP4-DeepSeek-V4.1-Flash-1017-NVFP4-8xV100-SXM2-PP2xTP4/blob/main/docs/measurements.md) · [Speed bench](https://github.com/ProprietaryLegal/Volta-Max-uPLIft-FP4-DeepSeek-V4.1-Flash-1017-NVFP4-8xV100-SXM2-PP2xTP4#tokens-per-second) · [How close to NVFP4](https://github.com/ProprietaryLegal/Volta-Max-uPLIft-FP4-DeepSeek-V4.1-Flash-1017-NVFP4-8xV100-SXM2-PP2xTP4#how-close-to-nvfp4) · [Closeness receipts and score](https://github.com/ProprietaryLegal/Volta-Max-uPLIft-FP4-DeepSeek-V4.1-Flash-1017-NVFP4-8xV100-SXM2-PP2xTP4/tree/main/quality/closeness-test) · [Hugging Face package](https://huggingface.co/ProprietaryLegal/Volta-Max-uPLIft-FP4-DeepSeek-V4.1-Flash-1017-hot_iq-8xV100-SXM2-PP2xTP4)

## Also featured: [Volta sPLIt](https://github.com/ProprietaryLegal/Volta-sPLIt-DeepSeek-V4.1-Flash-1017-8xV100-SXM2-PP2xTP4): ~200 tok/s on code, ~110 on legal text, on eight 2018 V100s

[![code and JSON: ~200 tok/s](https://img.shields.io/badge/code%20and%20JSON-~200%20tok%2Fs-2EA043?style=for-the-badge)](https://github.com/ProprietaryLegal/Volta-sPLIt-DeepSeek-V4.1-Flash-1017-8xV100-SXM2-PP2xTP4) [![legal: ~110 tok/s](https://img.shields.io/badge/legal-~110%20tok%2Fs-1F6FEB?style=for-the-badge)](https://github.com/ProprietaryLegal/Volta-sPLIt-DeepSeek-V4.1-Flash-1017-8xV100-SXM2-PP2xTP4) [![prose and chat: ~85-110 tok/s](https://img.shields.io/badge/prose%20and%20chat-~85--110%20tok%2Fs-8250DF?style=for-the-badge)](https://github.com/ProprietaryLegal/Volta-sPLIt-DeepSeek-V4.1-Flash-1017-8xV100-SXM2-PP2xTP4) [![prompt reading at 128K: 2,200 tok/s](https://img.shields.io/badge/prompt%20reading%20at%20128K-2%2C200%20tok%2Fs-D29922?style=for-the-badge)](https://github.com/ProprietaryLegal/Volta-sPLIt-DeepSeek-V4.1-Flash-1017-8xV100-SXM2-PP2xTP4) [![context: 524K per request](https://img.shields.io/badge/context-524K%20per%20request-555555?style=for-the-badge)](https://github.com/ProprietaryLegal/Volta-sPLIt-DeepSeek-V4.1-Flash-1017-8xV100-SXM2-PP2xTP4)

**DeepSeek-V4.1-Flash-1017 on the same 8x V100-SXM2-32GB, MEASURED 2026-11-05 on our checkpoint build.** The whole 249 GB model,
every expert, resident in the HBM2 of eight sm_70 cards from 2018, split pipeline-parallel 2 x tensor-parallel 4 across
two NVLink boards. Decode depends on what the model writes: about 200 tok/s for code and JSON, 105-118 for legal text,
85-110 for prose and chat, from a 1K prompt to 128K, a little slower at 256K. Prompt reading reaches 2,200 tok/s from
128K up (first token 59 s at 128K). Our port of 1Cat-vLLM #1277, one A/B-tested switch at a time, with exact outputs.
Quality, thinking off: LegalBench 0.716 balanced accuracy over 22 tasks; MMLU-Pro 79.9 % (700-item subset); HumanEval+ 89.6 % pass@1; it picks the original model's top next token 89.0 % of the time (92.5 % on legal text). Every patch, measurement and losing idea is published.

| Prompt | First token | Code | Structured (JSON) | Legal | Prose | Chat |
| --- | --- | --- | --- | --- | --- | --- |
| 1K | 1.2 s | 215 tok/s | 203 tok/s | 118 tok/s | 89 tok/s | 95 tok/s |
| 32K | 17 s | 200 | 207 | 117 | 90 | 107 |
| 128K | 59 s | 183 | 197 | 111 | 91 | 96 |
| 256K | 119 s | 160 | 180 | 103 | 84 | 81 |

<sub>One request at a time, 150 W per card, DSpark 5 drafts per round, thinking off, greedy, 1,024 tokens out; each prompt a real document of its kind; mean of 2 runs, greedy outputs byte-identical across runs. Thinking-on rows, every length from 1K to 256K, method and the test queue are in the <a href="https://github.com/ProprietaryLegal/Volta-sPLIt-DeepSeek-V4.1-Flash-1017-8xV100-SXM2-PP2xTP4">repository</a>.</sub>

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

## Also featured: [Volta Full NVFP4](https://github.com/ProprietaryLegal/Volta-Full-NVFP4-DeepSeek-V4.1-Flash-8xV100): every expert at NVFP4 precision, using host RAM

Volta Full NVFP4 runs every routed expert at exactly NVIDIA's NVFP4 precision on the same eight V100s, the most-used on the cards and the rest served from host RAM over PCIe. Slower, with no expert below NVFP4 precision at any time: 28 to 30 tok/s on legal-style text and 19 to 20 on general text, a 498,099-token prompt read in 326.6 s, and 44,696,862,720 folded expert values checked bit-equal to the NVFP4 formula (MEASURED 2026-11-09). As the reference of Volta Max uPLIft's closeness test it answered 83.8 % of 513 MMLU questions correctly (95 % interval 80.7 % to 86.7 %, greedy, thinking off), and a repeat in the same boot was identical on all 50 contexts and 50 questions (MEASURED 2026-11-11, 1,475 MHz).

[Repository](https://github.com/ProprietaryLegal/Volta-Full-NVFP4-DeepSeek-V4.1-Flash-8xV100) · [Measurements](https://github.com/ProprietaryLegal/Volta-Full-NVFP4-DeepSeek-V4.1-Flash-8xV100/blob/main/docs/measurements.md) · [The closeness test](https://github.com/ProprietaryLegal/Volta-Max-uPLIft-FP4-DeepSeek-V4.1-Flash-1017-NVFP4-8xV100-SXM2-PP2xTP4#how-close-to-nvfp4)

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
| [Volta-sPLIt-DeepSeek-V4.1-Flash-1017-8xV100-SXM2-PP2xTP4](https://github.com/ProprietaryLegal/Volta-sPLIt-DeepSeek-V4.1-Flash-1017-8xV100-SXM2-PP2xTP4) | **~200 tok/s code, ~110 legal**: DeepSeek-V4.1-Flash-1017 on 8x V100, PP2 x TP4, every expert resident; full patch series, measurements and test queue (2026-11-05 checkpoint) |
| [Volta-Max-uPLIft-FP4-DeepSeek-V4.1-Flash-1017-NVFP4-8xV100-SXM2-PP2xTP4](https://github.com/ProprietaryLegal/Volta-Max-uPLIft-FP4-DeepSeek-V4.1-Flash-1017-NVFP4-8xV100-SXM2-PP2xTP4) | Volta Max uPLIft: as much of the routed work at NVIDIA's NVFP4 precision as fits on the same 8x V100, every routed expert on the cards, the rest from compressed records. Every measurement published, and the build as one [Hugging Face package](https://huggingface.co/ProprietaryLegal/Volta-Max-uPLIft-FP4-DeepSeek-V4.1-Flash-1017-hot_iq-8xV100-SXM2-PP2xTP4) |
| [Volta-Full-NVFP4-DeepSeek-V4.1-Flash-8xV100](https://github.com/ProprietaryLegal/Volta-Full-NVFP4-DeepSeek-V4.1-Flash-8xV100) | Volta Full NVFP4: every routed expert at exactly NVIDIA's NVFP4 precision on the same 8x V100, the less-used ones from host RAM. Recipe, bit-equality proof and measurements |
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
| [deepseek-v4.1-v100](https://github.com/ProprietaryLegal/deepseek-v4.1-v100) | Fork of philbert440's 1Cat-vLLM engine snapshot and prebuilt SM70 wheel for DeepSeek-V4.1-Flash-1017 EXL3 at 1M context on 8x V100 |
| [1Cat-vLLM](https://github.com/ProprietaryLegal/1Cat-vLLM) | Mirror of the V100 / SM70-focused vLLM fork |
| [v100-skinny](https://github.com/ProprietaryLegal/v100-skinny) | Mirror of hand-written NVFP4 W4A16 CUDA kernels for Volta |

## Collaboration

For AI systems using approved frontier APIs, private cloud, or hardware you own, [reach us through the contact page](https://proprietarylegal.ai/contact.html).

Proprietary Legal Intelligence LLC is a technology consultancy, not a law firm, and does not provide legal services or legal advice.
