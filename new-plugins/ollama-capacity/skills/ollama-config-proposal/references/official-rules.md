# Official Ollama capacity knowledge

Verified live and read 2026-10-11. Scope: public rolling documentation for local Ollama, not a guarantee about an older installed version. The pages provide no single release version or publication date for all rules; the date here is the actual access date.

| Official URL | Deciding knowledge and section | Use |
|---|---|---|
| https://docs.ollama.com/faq | Concurrent requests: model residency and per-model parallelism differ; parallelism multiplies context. Queue rejection returns 503; queue default 512. Loaded-model default 3 times GPUs or 3 on CPU; parallel default 1. | Interpret allocation and overload; prefer observed effective limits. |
| https://docs.ollama.com/faq | Flash Attention and KV: supported backends/devices enable attention automatically; force with 1 or disable with 0. Cache type is global; f16 default, q8_0 about half and q4_0 about quarter cache memory; quality sensitivity varies. | Cache-only estimates, conditional quality trials. |
| https://docs.ollama.com/faq | Residency: five-minute default; request keep_alive overrides server setting; negative pins, zero unloads. Server configuration: systemd override/reload/restart, macOS launchctl/restart, Windows inherited environment/relaunch. | Avoid wrong-process settings and unintended persistent residency. |
| https://docs.ollama.com/context-length | Context defaults by VRAM: below 24 GiB 4k, 24–48 GiB 32k, at least 48 GiB 256k. Larger context increases memory. Cloud context defaults to model maximum. CONTEXT and PROCESSOR in ps expose allocation and offload. | Runtime context takes precedence over a guessed default. At exactly 48 GiB the printed ranges overlap: use effective evidence. |
| https://docs.ollama.com/api/ps | GET /api/ps lists currently loaded models; sample response has size, size_vram, details.quantization_level, expires_at and context_length. | Accept pasted API exports; expiry is residency metadata, not a capacity promise. Preserve missing fields. |
| https://docs.ollama.com/troubleshooting | NVIDIA discovery errors: 3 not initialized, 46 device unavailable, 100 no device, 999 unknown. Logs on macOS, Windows, systemd and containers differ. | Separate discovery failure from allocation failure; request the serving process's timestamped log. |
| https://docs.ollama.com/gpu | Hardware support: NVIDIA compute capability at least 5.0, driver at least 550; capability 5.0–6.2 needs driver at least 570. Supported AMD devices vary by OS. NVIDIA suspend/resume can cause GPU discovery trouble and CPU fallback. | Do not call a detection failure OOM. Use actual driver/device/OS evidence before hardware-specific advice. |

## Conflicts and narrow scope

FAQ context-window section still states a fixed 4096-token default, unlike the context page's VRAM tiers. Do not silently choose either for an unidentified installation. FAQ also retains a Windows Radeon note tied to ROCm 5.7/6.2; do not generalize that historical default to a supplied current runtime. Record version, effective settings and placement.

Multi-GPU placement (FAQ section): fit on one device first, otherwise spread across available GPUs. Device capacity, currently available memory and observed placement must stay separate; a combined total is insufficient.

## Authored analysis conventions

These are analysis methods, not vendor limits: per-pool ledgers; same-time reconciliation; inclusive-total double-count prevention; context-times-parallel as a relative allocation measure; proportional scaling only of measured KV; conditional unchanged-buffer estimates; staged changes; preserving the user's minimum context; q8_0 trial before q4_0; acceptance against supplied workload criteria. No universal headroom percentage or throughput estimate is prescribed.

GB and GiB conversions are unit definitions, not an Ollama allocation model. PROCESSOR percentages do not establish byte placement. On shared-memory hardware, inventory capacity must be reconciled as one pool rather than summed.

## Backend diagnosis — read 2026-10-11

- [Hardware support: GPU Selection, Linux Support, Vulkan GPU Support](https://docs.ollama.com/gpu): selectors are CUDA_VISIBLE_DEVICES (NVIDIA), ROCR_VISIBLE_DEVICES (ROCm), GGML_VK_VISIBLE_DEVICES (Vulkan). Invalid IDs exclude GPUs; NVIDIA UUIDs avoid numeric reordering. ROCm on Linux needs its v7 driver. Vulkan is default when installed; available-VRAM reporting on Linux needs capability/permissions, otherwise scheduling uses approximate model sizes. Use the actual backend; do not apply ROCm requirements to Vulkan.
- [Troubleshooting: AMD Driver Version Mismatch](https://docs.ollama.com/troubleshooting): bundled Linux ROCm 7 needs a compatible ROCm 7 kernel driver. Older ROCm 6.x drivers can hang initialization until discovery timeout and CPU fallback. Match the failure-during-discovery, timeout and 30-second bootstrap log pattern to supplied driver/backend/version evidence.
- [Troubleshooting: AMD GPU Discovery](https://docs.ollama.com/troubleshooting): Linux ROCm device access requires video/render groups; ROCm containers need the numeric groups owning /dev/kfd and /dev/dri. Host device visibility alone does not establish serving-process access.

These are rolling vendor rules, checked on the access date above. The proposed diagnostic ordering and one-control trials are authored analysis methods.
