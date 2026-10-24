# Quantization Compatibility

Check whether my quantized model will load in vLLM on my GPU.
For model deployment engineers. Needs pasted checkpoint metadata, quantization settings, hardware identity and backend version; logs and tensor metadata help resolve load failures. No account, key or installation is required.

- `check-quantization-compatibility`: a combination table with supported, unsupported or unresolved verdicts and required evidence.
- `explain-quantization-error`: a field-linked explanation of a quantization load failure and the smallest supported correction.

Paste `config.json`, quantization configuration, GPU/compute capability, exact backend version or commit, selected kernels, activation dtype, cache dtype and tensor-parallel settings. Remove secrets and private locations first. Existing exports are enough; metadata-only cases receive unresolved rows for missing deciding evidence.

The bundled official knowledge focuses on vLLM. Other backends need their own release-specific official evidence; vLLM findings do not transfer automatically. Supported means compatible under the stated constraints. Documented support and an observed successful load are recorded separately.

Network: when refreshing evidence, the agent reads official documentation on docs.vllm.ai, rocm.docs.amd.com and developer.nvidia.com, and vLLM source/release pages on github.com or raw.githubusercontent.com, including official redirects. It can read an official source URL you supply. Requests contain public page paths, not pasted checkpoint data. With no network, it uses bundled references or supplied official exports and leaves version gaps unresolved. No telemetry, accounts, paid APIs or connectors.

[Source register](skills/check-quantization-compatibility/references/official-knowledge.md) · [Privacy](PRIVACY.md)
