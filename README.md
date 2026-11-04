# Awesome Delphi AI [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

> A curated list of awesome tools, libraries, MCP servers, LSP implementations, and AI-driven workflows for modern Delphi and Object Pascal development.

This list focuses on modernizing the **development experience (DevEx) and engineering workflow** of Delphi developers: empowering engineers with autonomous coding agents (Claude Code, Cursor, Copilot), real-time runtime control over MCP, deep code intelligence via LSP, AST/DFM parsing for accurate LLM context, and native on-device AI inference.

---

## Contents

- [Agent Tooling & MCP (Model Context Protocol)](#agent-tooling--mcp-model-context-protocol)
- [Code Intelligence & LSP (Language Server Protocol)](#code-intelligence--lsp-language-server-protocol)
- [AST, DFM & Codebase Analysis](#ast-dfm--codebase-analysis)
- [Legacy Workflows & Encoding Bridges](#legacy-workflows--encoding-bridges)
- [IDE Plugins & In-Editor Assistants](#ide-plugins--in-editor-assistants)
- [AI Frameworks & Multi-Agent Orchestration](#ai-frameworks--multi-agent-orchestration)
- [Local / On-Device Inference (Delphi-Native)](#local--on-device-inference-delphi-native)
- [Cloud LLM API Clients](#cloud-llm-api-clients)
  - [Anthropic / Claude](#anthropic--claude)
  - [OpenAI](#openai)
  - [Google Gemini](#google-gemini)
  - [DeepSeek](#deepseek)
  - [Groq](#groq)
  - [Mistral](#mistral)
- [Testing & GUI Automation](#testing--gui-automation)
- [Community & Resources](#community--resources)
- [Contributing](#contributing)

---

## Agent Tooling & MCP (Model Context Protocol)

*MCP servers allow autonomous AI coding agents (Claude Code, Cursor, Codex) to interact directly with Delphi compilers, debuggers, running processes, and project structures.*

* **[MARS](https://github.com/andrea-magni/MARS)**  
  High-performance Delphi REST framework with native Model Context Protocol (MCP) server support. Exposes Delphi business logic, database queries, and custom functions directly as tools for AI agents with Server-Sent Events (SSE).  
  `[MCP]` `[SSE]` `[Delphi 12]` `[OpenAPI]` `[Linux]`

* **[MCPConnect](https://github.com/delphi-blocks/MCPConnect)**  
  Native Object Pascal implementation of the Model Context Protocol. Simplifies creating custom MCP tools and resource providers directly inside Delphi desktop and server applications.  
  `[MCP]` `[Agent Tooling]` `[Delphi]`

* **[DPT — Delphi Processing Tools](https://github.com/WladiD/WDDelphiTools/tree/master/Projects/DPT)**  
  CLI Swiss Army knife for Delphi featuring a dedicated MCP debugger server. Enables Claude Code and other agents to start/stop debug sessions, set hardware breakpoints, inspect call stacks, read registers/memory, and run automated linting without opening the IDE.  
  `[MCP]` `[CLI]` `[Debugger]` `[CI/CD]`

* **[delphi-visual-studio-code-debugger](https://github.com/csm101/delphi-visual-studio-code-debugger)**  
  Delphi debugger integration with an embedded MCP server, giving AI assistants the ability to autonomously launch, inspect, and debug compiled Delphi binaries inside modern editors.  
  `[MCP]` `[VSCode]` `[DAP]`

* **[Delphi-MCP-Server](https://github.com/GDKsoftware/Delphi-MCP-Server)**  
  Pure Delphi MCP server listening on localhost:3000/mcp. Integrates with Claude Desktop, Cursor, and Claude Code to provide Delphi project context.  
  `[MCP]` `[Claude Code]` `[Claude Desktop]`

* **[mxLore](https://github.com/MicrotronX/mxLore)**  
  Native Pascal Model Context Protocol server providing persistent memory, session tracking, and tool execution for AI coding agents across Delphi and FreePascal/Lazarus.  
  `[MCP]` `[Claude Code]` `[FreePascal]` `[Lazarus]`

* **[Delphi-LSP-MCP-Server](https://github.com/SkybuckFlying/Delphi-LSP-MCP-Server)**  
  Routes Model Context Protocol requests directly to Embarcadero's official `DelphiLSP.exe` for compiler-backed code intelligence: symbol lookups, definitions, and references.  
  `[MCP]` `[DelphiLSP]`

---

## Code Intelligence & LSP (Language Server Protocol)

*Language Server Protocol (LSP) engines and symbol indexers that feed deep semantic understanding, definitions, and call hierarchies of large Pascal workspaces to AI coding assistants.*

* **[pascal-language-server](https://github.com/genericptr/pascal-language-server)**  
  Production-grade Language Server Protocol implementation for Pascal and FreePascal. Provides cross-editor code completion, jump-to-definition, and symbol navigation essential for modern developer tooling and agent context extraction.  
  `[LSP]` `[Code Intelligence]` `[FreePascal]` `[Lazarus]`

* **[delphi-lookup](https://github.com/JavierusTk/delphi-lookup)**  
  High-speed symbol indexer and Delphi LSP provider designed to feed exact code context and symbol references across complex unit hierarchies directly to AI coding agents.  
  `[LSP]` `[Code Intelligence]` `[Symbol Search]` `[Delphi]`

* **[LSP-Pascal-Library](https://github.com/rickard67/LSP-Pascal-Library)**  
  Object Pascal client library implementing the LSP protocol. Enables building custom CLI tools, CI verification bots, and agent integrations that query language servers.  
  `[LSP]` `[Delphi]` `[Library]`

---

## AST, DFM & Codebase Analysis

*AST parsers, form extractors, and static analyzers that translate Object Pascal source files and binary DFMs into structured tokens for LLMs and automated refactoring.*

* **[DelphiAST](https://github.com/RomanYankovsky/DelphiAST)**  
  Full-featured Abstract Syntax Tree (AST) generator for Delphi source code. The standard building block for building custom code refactorings, semantic analyzers, and LLM context extractors.  
  `[AST]` `[Parsing]` `[Static Analysis]` `[Delphi]`

* **[StaticCodeAnalyser](https://github.com/nrodear/StaticCodeAnalyser)**  
  Static analysis engine for Delphi and Free Pascal with 200+ AST and DFM checks. Emits SARIF reports for automated agent-driven review and CI/CD quality gates.  
  `[AST]` `[SARIF]` `[Delphi 12]` `[Lazarus]` `[Static Analysis]`

* **[Markdown4D](https://github.com/GDKsoftware/Markdown4D)**  
  High-speed CommonMark/GFM parser featuring a public AST and streaming parsing. Essential for parsing, formatting, and rendering LLM streaming responses in VCL and FMX interfaces.  
  `[AST]` `[Markdown]` `[VCL]` `[FMX]` `[Streaming]`

* **[Neslib.Clang](https://github.com/neslib/Neslib.Clang)**  
  Delphi bindings for libclang. Enables AST parsing, semantic analysis, and tokenization of C/C++ headers to automate Delphi wrapper and binding generation.  
  `[AST]` `[libclang]` `[Delphi 12]`

---

## Legacy Workflows & Encoding Bridges

*Tools solving character set encoding, line endings, and workspace friction when AI agents refactor legacy Delphi projects.*

* **[mcp-file-tools](https://github.com/dimitar-grigorov/mcp-file-tools)**  
  Transparently prevents character set corruption when AI assistants edit legacy Delphi 7 through 2007 projects by safely handling ANSI, Windows-1252, and UTF-8 with BOM while preserving CRLF line endings.  
  `[Legacy Migration]` `[Delphi 7]` `[Delphi 2007]` `[UTF-8 BOM]` `[MCP]`

---

## IDE Plugins & In-Editor Assistants

*AI-assisted chat, code generation, and inline refactoring embedded directly into RAD Studio via the ToolsAPI.*

* **[FusionAI](https://github.com/AliDehbansiahkarbon/FusionAI)**  
  Comprehensive RAD Studio IDE plugin supporting OpenAI, Anthropic Claude, Google Gemini, and local Ollama instances for in-editor chat, inline code generation, and refactoring across Delphi XE5 to 12.  
  `[RAD Studio]` `[ToolsAPI]` `[Multi-Provider]` `[Delphi 12]`

* **[Delphi AI Developer](https://github.com/Code4Delphi/Delphi-AI-Developer)**  
  Open-source RAD Studio plugin providing multi-provider AI chat, code completion, and refactoring directly inside the IDE.  
  `[IDE Plugin]` `[ToolsAPI]` `[Multi-Provider]`

* **[RadIA-Plugin](https://github.com/regyssilveira/RadIA-Plugin)**  
  RAD Studio plugin leveraging Open Tools API and WebView2 with Server-Sent Events (SSE) for conversational AI assistance and contextual code editing.  
  `[OTA]` `[WebView2]` `[Delphi IDE]` `[SSE]`

* **[RAD Studio 13 Smart CodeInsight — Claude Patch](https://blogs.embarcadero.com/rad-studio-13-smart-codeinsight-claude-patch-released/)**  
  Official Embarcadero patch adding Claude-powered code completion directly to Smart CodeInsight.  
  `[RAD Studio 13]` `[GetIt]`

---

## AI Frameworks & Multi-Agent Orchestration

*Delphi-native architectures for building agentic workflows, RAG pipelines, and LLM applications.*

* **[MakerAI](https://github.com/gustavoeenriquez/MakerAi)**  
  Embedded framework for building AI-powered Delphi applications. Provides Vector RAG (HNSW + BM25), Graph RAG, autonomous multi-node agent thread pools, runtime-swappable LLM connectors, and MCP support.  
  `[RAG]` `[Agents]` `[Vector DB]` `[FPC]`

* **[PasClaw](https://github.com/FMXExpress/PasClaw)**  
  Lightweight autonomous AI agent framework in Object Pascal featuring tool calling and task orchestration for Delphi and FreePascal.  
  `[Agents]` `[Tool Calling]` `[FMX]` `[VCL]` `[Lazarus]`

* **[SmartCore AI Components Pack](https://blogs.embarcadero.com/introducing-the-smartcore-ai-components-pack/)**  
  Official Embarcadero AI component suite with engine-agnostic connection components (OpenAI, Claude, Gemini, Ollama), structured JSON request handling, and direct UI data binding.  
  `[RAD Studio 13]` `[GetIt]`

---

## Local / On-Device Inference (Delphi-Native)

*Run local LLMs, SLMs, and neural networks on-device without cloud dependencies, API keys, or external Python runtimes.*

* **[VindexLLM](https://github.com/tinyBigGAMES/VindexLLM)**  
  Native Delphi GPU inference engine that executes GGUF transformer models via Vulkan compute shaders. Requires zero external runtime dependencies (no Python, no CUDA)—only `vulkan-1.dll`.  
  `[Local Inference]` `[GGUF]` `[Vulkan GPU]` `[Zero-Dependency]`

* **[LlamaKit](https://github.com/gustavoeenriquez/LlamaKit)**  
  Local LLM inference using llama.cpp GGUF models with compiled Windows DLLs and native Delphi wrapper components.  
  `[llama.cpp]` `[GGUF]` `[Local]`

* **[llama-cpp-delphi](https://github.com/Embarcadero/llama-cpp-delphi)**  
  Official Embarcadero wrapper around llama.cpp for local GGUF model execution.  
  `[llama.cpp]` `[Embarcadero]`

* **[Dllama](https://github.com/tinyBigGAMES/Dllama)**  
  Lightweight Delphi binding for llama.cpp, supporting Ollama-compatible GGUF models (Llama, Mistral, Gemma).  
  `[llama.cpp]` `[GGUF]`

* **[TONNXRuntime](https://github.com/hshatti/TONNXRuntime)**  
  Microsoft ONNX Runtime bindings for FreePascal and Delphi for running pre-trained neural networks on desktop and edge devices.  
  `[ONNX]` `[Lazarus]` `[Delphi]`

* **[Ollama-Delphi-GUI](https://github.com/HuichanKIM/Ollama-Delphi-GUI)**  
  Delphi desktop client demonstrating real-time local model streaming and chat interface patterns over Ollama's REST API.  
  `[Ollama]` `[VCL]` `[Desktop UI]`

---

## Cloud LLM API Clients

*Robust, actively maintained Delphi SDKs for calling major AI provider APIs directly from Object Pascal.*

### Anthropic / Claude
* **[DelphiAnthropic](https://github.com/MaxiDonkey/DelphiAnthropic)** — Full Anthropic SDK covering Claude 3.5 and 3.7, vision, prompt caching, tool use, batch processing, and streaming.

### OpenAI
* **[DelphiOpenAI](https://github.com/HemulGM/DelphiOpenAI)** — Feature-complete OpenAI client (ChatGPT, Whisper, DALL-E, embeddings, function calling). Also connects to Azure, DeepSeek, and Ollama.
* **[DelphiGenAI](https://github.com/MaxiDonkey/DelphiGenAI)** — OpenAI client supporting GPT-4o, vision, audio, embeddings, and agentic workflows.
* **[openai-delphi](https://github.com/landgraf-dev/openai-delphi)** — Lightweight, clean client with full FreePascal and Lazarus compatibility.

### Google Gemini
* **[DelphiGemini](https://github.com/MaxiDonkey/DelphiGemini)** — Google Gemini SDK supporting multimodal prompts, code generation, caching, and fine-tuning.
* **[Gemini4Delphi](https://github.com/delmardelima/Gemini4Delphi)** — Lightweight Gemini bridge for Delphi.

### DeepSeek
* **[DelphiDeepseek](https://github.com/MaxiDonkey/DelphiDeepseek)** — DeepSeek reasoning model wrapper with local LM Studio compatibility.

### Groq
* **[DelphiGroqCloud](https://github.com/MaxiDonkey/DelphiGroqCloud)** — Groq LPU cloud API wrapper for ultra-low latency model inference.

### Mistral
* **[DelphiMistralAI](https://github.com/MaxiDonkey/DelphiMistralAI)** — Mistral SDK covering Codestral, vision, embeddings, and agentic conversations.

---

## Testing & GUI Automation

*AI-driven and automated testing tools for validating Delphi application behavior.*

* **[Autopilot for Delphi](https://github.com/GabrielOnDelphi/Autopilot-for-Delphi)**  
  Drives running VCL/FMX forms via MCP or DUnitX: clicks controls, verifies labels, dismisses dialogs, and validates screens without moving the physical mouse.  
  `[VCL]` `[FMX]` `[GUI Automation]` `[DUnitX]`

* **[ClaudeCode TokenVampire](https://github.com/GabrielOnDelphi/ClaudeCode_TokenVampire)**  
  Real-time token usage monitor for Claude Code sessions. Displays rolling window quotas, cache hit rates, and cost estimates via offline log analysis.  
  `[Claude Code]` `[DevEx]` `[Token Optimization]`

---

## Community & Resources

* **[Delphi-PRAXiS — AI & LLM Discussions](https://en.delphipraxis.net/forum/43-ai-assisted-coding/)** — Active community forum on integrating AI and LLMs into Delphi development workflows.
* **[Claude Code Training for Delphi Developers](https://training.gdksoftware.com/)** — Specialized training by GDK Software covering CLAUDE.md architecture, MCP setups, and Delphi agent workflows. `[Commercial]`

---

## Contributing

Contributions and recommendations are warmly welcome!
1. **Focus:** Must enhance Delphi or Object Pascal development with AI, MCP, LSP, AST analysis, or modern developer workflows.
2. **Quality & Distribution:** Open-source and actively maintained repositories are prioritized. Commercial or closed-source distribution tools must be uniquely valuable and clearly tagged `[Commercial]`.
3. **Format:** Submit a Pull Request following the established categorization and tag conventions.
