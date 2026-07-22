# Awesome NVIDIA NIM

[![Awesome](https://awesome.re/badge.svg)](https://awesome.re)
[![GitHub stars](https://img.shields.io/github/stars/DanielDeshmukh/awesome-nvidia-nim?style=social)](https://github.com/DanielDeshmukh/awesome-nvidia-nim)
[![GitHub forks](https://img.shields.io/github/forks/DanielDeshmukh/awesome-nvidia-nim?style=social)](https://github.com/DanielDeshmukh/awesome-nvidia-nim/network/members)
[![GitHub issues](https://img.shields.io/github/issues/DanielDeshmukh/awesome-nvidia-nim)](https://github.com/DanielDeshmukh/awesome-nvidia-nim/issues)
[![GitHub last commit](https://img.shields.io/github/last-commit/DanielDeshmukh/awesome-nvidia-nim)](https://github.com/DanielDeshmukh/awesome-nvidia-nim/commits)
[![License: CC0-1.0](https://img.shields.io/badge/License-CC0_1.0-lightgrey.svg)](https://creativecommons.org/publicdomain/zero/1.0/)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](https://github.com/DanielDeshmukh/awesome-nvidia-nim/pulls)
[![Maintenance](https://img.shields.io/badge/Maintained%3F-yes-green.svg)](https://github.com/DanielDeshmukh/awesome-nvidia-nim)

*If this list helped you, please consider giving it a ⭐ star — it helps other developers find it.*

---

> A curated list of resources, tools, projects, and workflows for building with [NVIDIA NIM](https://developer.nvidia.com/nim) — inference microservices for deploying AI models at production scale.

NVIDIA NIM provides optimized, containerized AI model inference via a simple REST API. This list covers everything from getting started to advanced agentic workflows.

**Inclusion criteria:** NVIDIA NIM must be central to the project — the primary inference/embedding backend, not one of many interchangeable LLM providers. See [Contributing](#contributing) for the full quality bar.

**[Submit a PR](https://github.com/DanielDeshmukh/awesome-nvidia-nim/pulls) to add your project!**

---

## Contents

- [Official Resources](#official-resources)
- [Getting Started](#getting-started)
- [Models Available on NIM](#models-available-on-nim)
- [Agentic Workflows & Multi-Agent Systems](#agentic-workflows--multi-agent-systems)
- [RAG Pipelines](#rag-pipelines)
- [Speech, Voice & Healthcare](#speech-voice--healthcare)
- [CLI Tools & SDKs](#cli-tools--sdks)
- [Integrations](#integrations)
- [Example Projects](#example-projects)
- [Tutorials & Blog Posts](#tutorials--blog-posts)
- [Community & Discussion](#community--discussion)
- [Contributing](#contributing)

---

## Official Resources

- [NVIDIA NIM Overview](https://developer.nvidia.com/nim) — Official landing page and API key signup.
- [NIM API Catalog](https://build.nvidia.com/explore/discover) — Browse all hosted models (LLMs, VLMs, embeddings, speech, code).
- [NVIDIA Generative AI Examples](https://github.com/NVIDIA/GenerativeAIExamples) — Official RAG and agentic workflow examples, including a [Community Showcase](https://github.com/NVIDIA/GenerativeAIExamples/blob/main/community/README.md) of external NIM projects.
- [NVIDIA AI Blueprints](https://github.com/NVIDIA-AI-Blueprints) — Production-ready, enterprise reference architectures using NIM.
- [NIM Documentation](https://docs.nvidia.com/nim/) — Full API reference and deployment guides.
- [Metropolis NIM Workflows](https://github.com/NVIDIA/metropolis-nim-workflows) — Visual AI agent workflows using NIM microservices.
- [NVIDIA NIM Deploy](https://github.com/NVIDIA/nim-deploy) — Official YAML/Helm/Operator reference implementations for deploying NIM in Kubernetes and production.
- [NVIDIA K8s NIM Operator](https://github.com/NVIDIA/k8s-nim-operator) — Operator for deploying and maintaining NIMs and NeMo microservices on Kubernetes.
- [NVIDIA NIM Anywhere](https://github.com/NVIDIA/nim-anywhere) — Reference project to accelerate Gen AI development with NIM + AI Workbench, with or without local GPUs.

## Getting Started

- [NIM Quickstart Guide](https://docs.nvidia.com/nim/large-language-models/latest/getting-started.html) — Get your first API call working in under 5 minutes.
- [NIM Free Credits](https://build.nvidia.com) — Free credits for new accounts; no GPU required.
- [OpenAI-Compatible API](https://docs.nvidia.com/nim/large-language-models/latest/openai-api.html) — NIM endpoints are OpenAI-spec compatible; drop-in for any OpenAI SDK client.
- [Deploy Your Own LLM with NIM](https://github.com/NVIDIA-AI-Blueprints/bring-llms-to-nim) — Containerized deployment blueprint for custom models.

## Models Available on NIM

NIM hosts a large and growing catalog of models. Key categories:

**LLMs**
- `meta/llama-3.3-70b-instruct` — Meta's flagship instruction-tuned model.
- `nvidia/nemotron-4-340b-instruct` — NVIDIA's frontier reasoning model.
- `mistralai/mistral-7b-instruct-v0.3` — Efficient 7B instruction model.
- `microsoft/phi-3-mini-128k-instruct` — Long-context small model.
- `deepseek-ai/deepseek-r1` — Reasoning-focused model.

**Code**
- `qwen/qwen2.5-coder-32b-instruct` — Top-tier code model.
- `ibm/granite-34b-code-instruct` — Enterprise code model.

**Embeddings**
- `nvidia/nv-embedqa-e5-v5` — High-quality retrieval embeddings.
- `baai/bge-m3` — Multilingual embedding model.

**Vision / Multimodal**
- `microsoft/phi-3-vision-128k-instruct` — Vision + language understanding.
- `nvidia/neva-22b` — NVIDIA's VLM.

> Full catalog: [build.nvidia.com/explore/discover](https://build.nvidia.com/explore/discover) (model availability changes frequently — always check the live catalog).

## Agentic Workflows & Multi-Agent Systems

- [autobots](https://github.com/DanielDeshmukh/autobots) ⭐ — PyPI-published CLI for spinning up NVIDIA NIM-powered multi-agent swarms. Live model catalog discovery, skill injection, extensive test suite. `pip install autobot-swarm`
- [NVIDIA NeMo Agent Toolkit](https://github.com/NVIDIA/NeMo-Agent-Toolkit) — Official open-source toolkit for connecting and optimizing agent teams, with MCP/A2A protocol support and NIM as a core backend.
- [LangGraph + NIM Agents](https://github.com/NVIDIA/GenerativeAIExamples/tree/main/AgentFrameworks) — LangGraph-based multi-agent examples with NIM backends.
- [cybersentry](https://github.com/prutxvi/cybersentry) — Autonomous AI-powered ethical hacking agent powered by Llama 3.1 70B on NVIDIA NIM.
- [Blacknode](https://github.com/temiroff/Blacknode) — MCP-native visual workflow framework for AI agents with a node editor and Python export; NIM-supported.
- [proteus](https://github.com/DanielDeshmukh/proteus) `*new*` — Five-agent JD-aware resume analyzer with NIM pipeline: parse, calibrate, map, rewrite, draft.
- [CodeSage](https://github.com/DanielDeshmukh/CodeSage) `*new*` — AI codebase examiner for interview prep using 5 specialized NIM models for question generation and scoring.

## RAG Pipelines

- [NVIDIA RAG Blueprint](https://github.com/NVIDIA-AI-Blueprints/rag) — Official enterprise reference RAG pipeline using NIM microservices, NeMo Retriever, and guardrailing.
- [RAG with NIM + LangChain](https://github.com/NVIDIA/GenerativeAIExamples/tree/main/RAG) — Production RAG using NIM embeddings + LLM inference.
- [Hybrid RAG Workbench Example](https://github.com/NVIDIA/workbench-example-hybrid-rag) — RAG project that works interchangeably with build.nvidia.com endpoints, local NIM containers, or HF TGI.
- [NVIDIA ChatRTX](https://github.com/NVIDIA/ChatRTX) — Personalize a local LLM with your own docs using RAG + TensorRT-LLM + NIM, runs on RTX PCs.
- [NIM + Qdrant RAG](https://qdrant.tech/documentation/integrations/nvidia-nim/) — Qdrant vector DB integrated with NIM for semantic search.
- [Chat-RAG](https://github.com/JakeFurtaw/Chat-RAG) — Gradio-based coding assistant streaming responses, pulling context from GitHub repos and local files, with NIM inference.
- [nvidia-NIM-RAG](https://github.com/mickymultani/nvidia-NIM-RAG) — Community project demonstrating a NIM-powered RAG pipeline end to end.
- [NVIDIA_NIM-demo](https://github.com/anirxudh/NVIDIA_NIM-demo) — Streamlit RAG chatbot using NIM embeddings, FAISS, and document loaders.
- [ella](https://github.com/DanielDeshmukh/ella) `*new*` — Medical triage RAG engine with 90K+ clinical chunks, NIM embeddings + Pinecone. `pip install ella-sdk`

## Speech, Voice & Healthcare

- [Nemotron Voice Agent Blueprint](https://build.nvidia.com/nvidia/nemotron-voice-agent) — Official NVIDIA blueprint for real-time, interruptible voice agents combining Nemotron ASR, LLM, and TTS in a streaming pipeline.
- [nemotron-speech-demos](https://github.com/fciannella/nemotron-speech-demos) — Vertical voice-agent examples (wire transfer with Twilio, ambient healthcare agents + guardrails) built on Nemotron NIM.
- [NVIDIA Digital Biology Examples](https://github.com/NVIDIA/bionemo-examples) — Official BioNeMo + NIM examples for drug discovery: protein structure prediction, molecular generation, and genomics inference.
- [Speech & Translation NIM Microservices Guide](https://developer.nvidia.com/blog/quickly-voice-your-apps-with-nvidia-nim-microservices-for-speech-and-translation) — Official walkthrough integrating ASR/NMT/TTS NIMs into a voice-driven RAG pipeline.

## CLI Tools & SDKs

- [autobot-swarm](https://pypi.org/project/autobot-swarm/) — CLI tool for NIM multi-agent orchestration. Live model discovery, skill injection, swarm configuration. `pip install autobot-swarm`
- [pi-nvidia-nim](https://github.com/xRyul/pi-nvidia-nim) — NVIDIA NIM provider extension for the `pi` coding agent; access 100+ models from build.nvidia.com with reasoning-level support.
- [openai Python SDK](https://github.com/openai/openai-python) — Works out-of-the-box with NIM (set `base_url="https://integrate.api.nvidia.com/v1"`).
- [ella-sdk](https://pypi.org/project/ella-sdk/) `*new*` — Python SDK for medical triage RAG using NIM embeddings + Pinecone. `pip install ella-sdk`

## Integrations

**Frameworks**
- [LangChain NIM Integration](https://python.langchain.com/docs/integrations/chat/nvidia_ai_endpoints/) — `ChatNVIDIA` class; drop-in for any LangChain chain or agent.
- [LlamaIndex NIM](https://docs.llamaindex.ai/en/stable/examples/llm/nvidia/) — Use NIM as LLM or embedding provider in LlamaIndex pipelines.
- [Haystack NIM](https://haystack.deepset.ai/integrations/nvidia) — NVIDIA NIM components for Haystack pipelines.
- [DSPy + NIM](https://dspy.ai) — Use NIM as the LM backend for DSPy programs.
- [elizaOS plugin-nvidia-nim](https://github.com/elizaos-plugins/plugin-nvidia-nim) — ElizaOS plugin integrating NIM foundation models for content analysis, image detection, and safety checks.

**Vector Stores**
- [Qdrant](https://qdrant.tech/documentation/integrations/nvidia-nim/) — Native NIM embedding integration.
- [Milvus](https://milvus.io/docs/integrate_with_nvidia.md) — NVIDIA NIM + Milvus for large-scale vector search.
- [Weaviate](https://weaviate.io/developers/weaviate/model-providers/nvidia) — NIM embedding and generative modules.

**Infrastructure**
- [NIM on Docker](https://docs.nvidia.com/nim/large-language-models/latest/getting-started.html#deploy-nim) — Self-hosted NIM containers with Docker.
- [NIM on Kubernetes](https://docs.nvidia.com/nim/large-language-models/latest/k8s-operator.html) — Helm charts and K8s operator for NIM deployments.

## Example Projects

- [autobots](https://github.com/DanielDeshmukh/autobots) — Multi-agent CLI swarm using NIM with live model catalog discovery. PyPI-published.
- [nextjs-nvidia-chatbot](https://github.com/lakshaybhushan/nextjs-nvidia-chatbot) — Open-source AI chatbot template built with Next.js, the Vercel AI SDK, and NIM inference.
- [H.E.I.M.D.A.L.L](https://github.com/KarthikSriramGit/H.E.I.M.D.A.L.L) — Fleet telemetry natural-language insights using GPU data loading (cuDF), local LLM inference, and production NIM on GKE.
- [Satark-AI](https://github.com/theunstopabble/Satark-AI) — Multi-model deepfake detection and speaker verification platform using NIM (Llama 3.2-90B Vision) for image detection.
- [Comfy-Cozy](https://github.com/JosephOIbrahim/Comfy-Cozy) — AI co-pilot for ComfyUI with 129 MCP tools; supports NIM alongside other LLM providers.
- [AETHER](https://github.com/DanielDeshmukh/aether) — Autonomous pentest platform built on LangGraph + NIM + Playwright.
- [ella](https://github.com/DanielDeshmukh/ella) `*new*` — Medical triage RAG engine with 90K+ clinical chunks, NIM embeddings + Pinecone + Groq for zero-hallucination patient triage.
- [proteus](https://github.com/DanielDeshmukh/proteus) `*new*` — Five-agent JD-aware resume analyzer: semantic match scoring, gap analysis, bullet rewrites, and cover letters via NIM pipeline.
- [CodeSage](https://github.com/DanielDeshmukh/CodeSage) `*new*` — AI codebase examiner for viva/interview prep using 5 specialized NIM models (embed, rerank, question gen, scoring, safety).

## Tutorials & Blog Posts

- [Getting Started with NVIDIA NIM APIs](https://developer.nvidia.com/blog/getting-started-with-nvidia-nim/) — Official NVIDIA walkthrough.
- [Building Agentic AI with NIM and LangGraph](https://developer.nvidia.com/blog/build-ai-agents-with-nvidia-nim-and-langchain/) — End-to-end agent tutorial.
- [RAG in 5 Minutes with NIM](https://developer.nvidia.com/blog/rag-101-retrieval-augmented-generation-with-llms/) — Fast RAG setup guide.
- [NVIDIA NIM: The Inference Layer for Agentic AI](https://blog.langchain.dev/nvidia-nim-and-langchain/) — LangChain blog on the NIM + LangChain integration.

## Community & Discussion

- [NVIDIA Developer Forums — NIM](https://forums.developer.nvidia.com/c/ai-data-science/nim/535) — Official support and discussion.
- [r/NVIDIA](https://www.reddit.com/r/nvidia/) — Reddit community.

---

## Contributing

Contributions welcome! Read the [contribution guidelines](CONTRIBUTING.md) first.

To add a resource:
1. Fork this repo.
2. Add your link in the relevant section — name, URL, and a one-sentence description.
3. Open a pull request.

**Quality bar:**
- NVIDIA NIM must be the **primary or required** inference/embedding backend — not one of many interchangeable LLM providers a project happens to support.
- Publicly accessible and actively maintained (last commit < 1 year, with rare exceptions for official NVIDIA reference repos).
- Real README, working setup instructions, and some evidence of actual use (stars, forks, or recent commits).
- No duplicates. No self-promotion without a working, documented project.

---

*Maintained by [Daniel Deshmukh](https://github.com/DanielDeshmukh) · Mumbai, India*