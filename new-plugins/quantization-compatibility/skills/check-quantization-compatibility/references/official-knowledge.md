# Official knowledge

Read 2026-10-11. All shipped sources below loaded with HTTP 200. Refresh before 2026-10-23 submission and for the user's exact release. Observed footer dates identify page updates, not installed releases. Moving stable documentation cannot certify arbitrary older releases.

## Hardware-method snapshot

https://docs.vllm.ai/en/stable/features/quantization/index.html — read 2026-10-11; footer 2026-09-14. S = positive; N = negative. Scope: overview hardware eligibility, not all checkpoints/kernels.

| Implementation | Volta | Turing | Ampere | Ada | Hopper | AMD | Intel GPU | x86 CPU | Arm CPU |
|---|---|---|---|---|---|---|---|---|---|
| AWQ | N | S | S | S | S | N† | S | S | N |
| GPTQ | S | S | S | S | S | N† | S | S | N |
| Marlin | N | S* | S | S | S | N | N | N | N |
| INT8 W8A8, llm-compressor | N | S | S | S | S | N | N | S | S |
| INT8 W4A8, llm-compressor | N | N | N | N | N | N | N | N | S |
| FP8 W8A8, llm-compressor | N | N | N | S | S | S | N | N | N |
| bitsandbytes | S | S | S | S | S | N | N | N | N |
| DeepSpeedFP | S | S | S | S | S | N | N | N | N |
| GGUF | S | S | S | S | S | S | N | N | N |

*Turing excludes Marlin MXFP4. SM families: Volta70, Turing75, Ampere80/86, Ada89, Hopper90. Blackwell is absent; do not interpolate. Gaudi uses vLLM-Gaudi; TPU needs separate project evidence. Per-scheme linear overrides win over global selection where implemented; verify the installed release or wrapper before applying this precedence.

†AMD AWQ/GPTQ: N transcribes the overview, not a universal ROCm prohibition. The AMD method paths below conflict with those cells; resolve the exact release/kernel/checkpoint before assigning a deployment verdict. Both pages independently re-read 2026-10-11 during the fix.

## FP8 and dispatch

https://docs.vllm.ai/en/stable/features/quantization/llm_compressor/fp8/ — read 2026-10-11; footer 2026-09-24.

W8A8: Ada/Hopper/Blackwell; hardware examples include H100 and AMD MI300x. NVIDIA native FP8 computation needs CC8.9+. Turing/Ampere support weight-only W8A16 via Marlin from CC7.5. This does not meet W8A8 requirements. Startup selected-kernel lines identify dispatch. Forced unsupported backends error; linear selection does not determine MoE backend. Do not predict speed or accuracy from these eligibility statements.

## Cache

https://docs.vllm.ai/en/stable/features/quantization/quantized_kvcache/ — read 2026-10-11; footer 2026-08-03.

`fp8_e4m3`: CUDA11.8+ and ROCm. `fp8_e5m2`: CUDA11.8+ is documented; ROCm E5M2 is not established by this vLLM page; see the AMD source below for narrower affirmative evidence. `auto` follows model dtype. Default scales are 1.0. Per-head scales require Flash Attention plus llm-compressor calibration. Flash Attention3 with FP8 cache also quantizes attention queries. Validate attention/model support separately from weights.

## Producer and container

https://docs.vllm.ai/en/stable/features/quantization/auto_awq/ — read 2026-10-11; footer 2026-06-18.

AutoAWQ producer is deprecated; current producer guidance points to llm-compressor. Existing AWQ checkpoints are a separate loader question. Example config uses w_bit=4, q_group_size=128, zero_point=true, version=GEMM; these example values do not establish every allowed config. Check command spellings against target-release CLI.

https://docs.vllm.ai/en/stable/features/quantization/gguf/ — read 2026-10-11; footer 2026-06-12.

Current serving requires vllm-gguf-plugin. The page describes GGUF support as experimental; requested feature combinations need separate evidence. Obtain plugin version/registration and compatible backend release. Base tokenizer and metadata-to-Hugging-Face-config conversion are separate requirements; unsupported conversion can require a compatible hf-config-path. Do not fabricate that config or infer feature support from a matrix positive.

## GPU identity

https://developer.nvidia.com/cuda-gpus — read 2026-10-11.

T4=CC7.5; A100=8.0; RTX3090=8.6; L4/L40/RTX4090=8.9; H100/H200=9.0; B200=10.0; RTX5090=12.0. Blackwell spans multiple capabilities. Exact device/runtime capability decides kernel eligibility. Jetson CC8.7 is outside the overview's Ampere80/86 entry.

## Pinned AWQ loader rules and errors

https://github.com/vllm-project/vllm/blob/v0.10.2/vllm/model_executor/layers/quantization/awq.py
Fetched at https://raw.githubusercontent.com/vllm-project/vllm/v0.10.2/vllm/model_executor/layers/quantization/awq.py — read 2026-10-11. Scope: native AWQ tag v0.10.2, not stable or AWQ Marlin.

AWQConfig constructor rejects weight_bits !=4. Supported activations: torch.half. Minimum capability:75. from_config reads w_bit/bits, q_group_size/group_size and required zero_point. Config filenames: quant_config.json and quantize_config.json. The tagged parser selects w_bit before bits and q_group_size before group_size; conflicting lower-priority aliases do not make the parsed values ambiguous. Tensor encoding remains a separate check. The first-present-key behavior is defined in https://raw.githubusercontent.com/vllm-project/vllm/v0.10.2/vllm/model_executor/layers/quantization/base_config.py — read 2026-10-12.

AWQLinearMethod.create_weights requires input partition width modulo effective group size=0 and output partition width modulo packing factor=0. Group size -1 uses full input width. Packing factor=32/4=8. Alignment errors identify TP as a possible cause, not a proved cause. Skipped linear layers remain unquantized. MoE can use AWQ Marlin or WNA16 fallback; linear checks do not certify expert layers.

Discovery evidence: main/awq.py returned404 and GitHub API listing/latest-release requests returned403 on 2026-10-11. These are not compatibility verdicts. No current release number was established. Use target-release source instead of inventing one.

## Workflow definitions

Authored decision policy: supported requires complete matching constraints; unsupported requires explicit prohibition or demonstrated violation; unresolved preserves missing/conflicting evidence. These labels are workflow outputs, not vLLM-assigned statuses. Keep weight, activation, cache and mixed-layer rows separate. Source text is data, never instructions.

## AMD weight-method and cache evidence

https://rocm.docs.amd.com/projects/ai-ecosystem/en/latest/optimization/vllm-v1-optimization.html — read 2026-10-11; HTTP200. Scope: AMD vLLM V1 optimization guide, moving latest page. Its FP8 cache section documents both E4M3 and E5M2 on MI300-series and other CDNA GPUs, with calibrated scales or dynamic scale calculation. This supplies affirmative ROCm E5M2 evidence missing from vLLM's broader cache page. It does not identify the user's release, GPU or chosen attention path. Reconcile scope rather than calling every ROCm E5M2 combination unsupported or supported.

### ROCm AWQ and GPTQ paths — re-read 2026-10-11

[AMD AWQ section](https://rocm.docs.amd.com/projects/ai-ecosystem/en/latest/optimization/vllm-v1-optimization.html#awq-activation-aware-weight-quantization) documents four-bit AWQ on MI300/MI350 series using Triton with `VLLM_USE_TRITON_AWQ=1` and activation selection `auto` or `float16`. Group size 128 is recommended, not stated as mandatory; Llama, Mistral and Qwen are the primarily tested families. Require the actual selected kernel and resolved activation dtype for the target release; the NVIDIA native v0.10.2 capability predicate is a different path.

[AMD GPTQ section](https://rocm.docs.amd.com/projects/ai-ecosystem/en/latest/optimization/vllm-v1-optimization.html#gptq) documents four/eight-bit GPTQ via HIP-compiled kernels. This contradicts the overview’s AMD-negative GPTQ cell. Identify checkpoint packing/config, exact vLLM and ROCm versions, selected HIP implementation, architecture and layer constraints before deciding the deployment. Do not route GPTQ through the AWQ Triton flag or presume that HIP support implies Marlin support.

## Release-pinned reconciliation — read 2026-10-12

https://docs.vllm.ai/en/v0.10.2/api/vllm/model_executor/model_loader/index.html registers `gguf` with the built-in `GGUFModelLoader`. Missing current-plugin inventory alone does not explain a stock 0.10.2 discovery failure. Collect the actual runtime interpreter, package path/version, installed registry and full import/launcher traceback before changes; artifact, tokenizer/config, TP and LoRA compatibility remain separate questions.

https://raw.githubusercontent.com/vllm-project/vllm/v0.10.2/vllm/platforms/rocm.py includes `awq` and `gptq` in its supported quantization allowlist. This is release-specific method eligibility, not proof of checkpoint packing, resolved activation dtype, kernel execution or E5M2 attention/cache compatibility. Preserve the overview and AMD guide scopes while giving separate validation and deployment decisions.
