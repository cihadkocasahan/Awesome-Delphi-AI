# Awesome Delphi AI [![Awesome](https://awesome.re/badge.svg)](https://awesome.re) [![Community Curation](https://img.shields.io/badge/Curated_by-Community-8A2BE2?style=flat-square)](https://github.com/cihadkocasahan/Awesome-Delphi-AI)

[🇬🇧 English](README.md) · [🇹🇷 Türkçe](README.tr.md)

> A curated list of awesome tools, libraries, MCP servers, LSP implementations, and AI-driven workflows for modern Delphi and Object Pascal development.
>
> 🔍 **Community-Curated:** Periodically scanned and updated to include the latest open-source Delphi AI projects.

This list focuses on modernizing the **development experience (DevEx) and engineering workflows** of Delphi developers. All resources are organized by category in the contents below.

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
- [Testing & GUI Automation](#testing--gui-automation)
- [Curated Lists & Community Directories](#curated-lists--community-directories)
- [Community & Resources](#community--resources)
- [Contributing](#contributing)
- [Security & Disclaimer](#security--disclaimer)

---

## Agent Tooling & MCP (Model Context Protocol)

*MCP servers allow autonomous AI coding agents (Claude Code, Cursor, Codex) to interact directly with Delphi compilers, debuggers, running processes, and project structures.*

🔍 **Live GitHub Searches:** [`delphi mcp`](https://github.com/search?q=delphi+mcp&type=repositories&s=updated&o=desc) · [`pascal mcp`](https://github.com/search?q=pascal+mcp&type=repositories&s=updated&o=desc) · [`delphi model context protocol`](https://github.com/search?q=delphi+model+context+protocol&type=repositories&s=updated&o=desc)

| Project | Stars & Health | Description | Tags |
| :--- | :---: | :--- | :--- |
| **[MARS](https://github.com/andrea-magni/MARS)** | [![Stars](https://img.shields.io/github/stars/andrea-magni/MARS?style=flat-square)](https://github.com/andrea-magni/MARS/stargazers)<br>[![Last Commit](https://img.shields.io/github/last-commit/andrea-magni/MARS?style=flat-square)](https://github.com/andrea-magni/MARS/commits) | High-performance Delphi REST framework with native Model Context Protocol (MCP) server support. Exposes Delphi business logic, database queries, and custom functions directly as tools for AI agents with Server-Sent Events (SSE). | `MCP` `SSE` `Delphi 12` `OpenAPI` `Linux` |
| **[MCPConnect](https://github.com/delphi-blocks/MCPConnect)** | [![Stars](https://img.shields.io/github/stars/delphi-blocks/MCPConnect?style=flat-square)](https://github.com/delphi-blocks/MCPConnect/stargazers)<br>[![Last Commit](https://img.shields.io/github/last-commit/delphi-blocks/MCPConnect?style=flat-square)](https://github.com/delphi-blocks/MCPConnect/commits) | Native Object Pascal implementation of the Model Context Protocol. Simplifies creating custom MCP tools and resource providers directly inside Delphi desktop and server applications. | `MCP` `Agent Tooling` `Delphi` |
| **[DPT — Delphi Processing Tools](https://github.com/WladiD/WDDelphiTools/tree/master/Projects/DPT)** | [![Stars](https://img.shields.io/github/stars/WladiD/WDDelphiTools?style=flat-square)](https://github.com/WladiD/WDDelphiTools/stargazers)<br>[![Last Commit](https://img.shields.io/github/last-commit/WladiD/WDDelphiTools?style=flat-square)](https://github.com/WladiD/WDDelphiTools/commits) | CLI Swiss Army knife for Delphi featuring a dedicated MCP debugger server. Enables Claude Code and other agents to start/stop debug sessions, set hardware breakpoints, inspect call stacks, read registers/memory, and run automated linting without opening the IDE. | `MCP` `CLI` `Debugger` `CI/CD` |
| **[delphi-visual-studio-code-debugger](https://github.com/csm101/delphi-visual-studio-code-debugger)** | [![Stars](https://img.shields.io/github/stars/csm101/delphi-visual-studio-code-debugger?style=flat-square)](https://github.com/csm101/delphi-visual-studio-code-debugger/stargazers)<br>[![Last Commit](https://img.shields.io/github/last-commit/csm101/delphi-visual-studio-code-debugger?style=flat-square)](https://github.com/csm101/delphi-visual-studio-code-debugger/commits) | Delphi debugger integration with an embedded MCP server, giving AI assistants the ability to autonomously launch, inspect, and debug compiled Delphi binaries inside modern editors. | `MCP` `VSCode` `DAP` |
| **[Delphi-MCP-Server](https://github.com/GDKsoftware/Delphi-MCP-Server)** | [![Stars](https://img.shields.io/github/stars/GDKsoftware/Delphi-MCP-Server?style=flat-square)](https://github.com/GDKsoftware/Delphi-MCP-Server/stargazers)<br>[![Last Commit](https://img.shields.io/github/last-commit/GDKsoftware/Delphi-MCP-Server?style=flat-square)](https://github.com/GDKsoftware/Delphi-MCP-Server/commits) | Pure Delphi MCP server listening on localhost:3000/mcp. Integrates with Claude Desktop, Cursor, and Claude Code to provide Delphi project context. | `MCP` `Claude Code` `Claude Desktop` |
| **[mxLore](https://github.com/MicrotronX/mxLore)** | [![Stars](https://img.shields.io/github/stars/MicrotronX/mxLore?style=flat-square)](https://github.com/MicrotronX/mxLore/stargazers)<br>[![Last Commit](https://img.shields.io/github/last-commit/MicrotronX/mxLore?style=flat-square)](https://github.com/MicrotronX/mxLore/commits) | Native Pascal Model Context Protocol server providing persistent memory, session tracking, and tool execution for AI coding agents across Delphi and FreePascal/Lazarus. | `MCP` `Claude Code` `FreePascal` `Lazarus` |
| **[Delphi-LSP-MCP-Server](https://github.com/SkybuckFlying/Delphi-LSP-MCP-Server)** | [![Stars](https://img.shields.io/github/stars/SkybuckFlying/Delphi-LSP-MCP-Server?style=flat-square)](https://github.com/SkybuckFlying/Delphi-LSP-MCP-Server/stargazers)<br>[![Last Commit](https://img.shields.io/github/last-commit/SkybuckFlying/Delphi-LSP-MCP-Server?style=flat-square)](https://github.com/SkybuckFlying/Delphi-LSP-MCP-Server/commits) | Routes Model Context Protocol requests directly to Embarcadero's official DelphiLSP.exe for compiler-backed code intelligence: symbol lookups, definitions, and references. | `MCP` `DelphiLSP` |
| **[daofy](https://github.com/chinawsb/daofy)** | [![Stars](https://img.shields.io/github/stars/chinawsb/daofy?style=flat-square)](https://github.com/chinawsb/daofy/stargazers)<br>[![Last Commit](https://img.shields.io/github/last-commit/chinawsb/daofy?style=flat-square)](https://github.com/chinawsb/daofy/commits) | Model Context Protocol server enabling AI assistants to compile Delphi projects and query domain-specific knowledge bases. Facilitates automated build validation and contextual code assistance in Object Pascal workflows. | `MCP` `Delphi` `Tooling` `RAG` `Compiler` |
| **[delphi-dev](https://github.com/adrianosantostreina/delphi-dev)** | [![Stars](https://img.shields.io/github/stars/adrianosantostreina/delphi-dev?style=flat-square)](https://github.com/adrianosantostreina/delphi-dev/stargazers)<br>[![Last Commit](https://img.shields.io/github/last-commit/adrianosantostreina/delphi-dev?style=flat-square)](https://github.com/adrianosantostreina/delphi-dev/commits) | Plugin for Claude Code that enforces Delphi Style Guide, Clean Code, and SOLID principles during LLM agent interactions. It provides structured architectural guidance directly inside Delphi development workflows. | `Claude Code` `Agent Tooling` `Prompt Optimization` `Clean Code` `Object Pascal` |
| **[delphi-compiler](https://github.com/JavierusTk/delphi-compiler)** | [![Stars](https://img.shields.io/github/stars/JavierusTk/delphi-compiler?style=flat-square)](https://github.com/JavierusTk/delphi-compiler/stargazers)<br>[![Last Commit](https://img.shields.io/github/last-commit/JavierusTk/delphi-compiler?style=flat-square)](https://github.com/JavierusTk/delphi-compiler/commits) | Wraps Delphi compiler execution into structured tool interfaces optimized for autonomous AI coding agents like Claude Code. It automates error feedback loops to allow LLMs to iteratively fix Object Pascal build errors. | `Agent Tooling` `Claude Code` `Compiler` `CLI` `Object Pascal` |
| **[HTML-To-Delphi-FMX](https://github.com/dondonondon/HTML-To-Delphi-FMX)** | [![Stars](https://img.shields.io/github/stars/dondonondon/HTML-To-Delphi-FMX?style=flat-square)](https://github.com/dondonondon/HTML-To-Delphi-FMX/stargazers)<br>[![Last Commit](https://img.shields.io/github/last-commit/dondonondon/HTML-To-Delphi-FMX?style=flat-square)](https://github.com/dondonondon/HTML-To-Delphi-FMX/commits) | Provides agent skills and prompts enabling AI coding assistants to translate HTML/CSS design specs directly into native Delphi FMX code. Automates UI layout generation to accelerate cross-platform frontend development in Object Pascal. | `Agent Skills` `FMX` `Delphi` `UI Conversion` `Codex` |
| **[mcp-server-delphi](https://github.com/danieleteti/mcp-server-delphi)** | [![Stars](https://img.shields.io/github/stars/danieleteti/mcp-server-delphi?style=flat-square)](https://github.com/danieleteti/mcp-server-delphi/stargazers)<br>[![Last Commit](https://img.shields.io/github/last-commit/danieleteti/mcp-server-delphi?style=flat-square)](https://github.com/danieleteti/mcp-server-delphi/commits) | Delphi implementation of the Model Context Protocol built on DMVCFramework. Uses RTTI and attributes to expose tools, resources, and prompts over stdio or HTTP streaming transports. | `MCP` `DMVCFramework` `Tools` `Delphi 12` `RTTI` |
| **[ShellDelphi](https://github.com/AnaLauraCorrea/ShellDelphi)** | [![Stars](https://img.shields.io/github/stars/AnaLauraCorrea/ShellDelphi?style=flat-square)](https://github.com/AnaLauraCorrea/ShellDelphi/stargazers)<br>[![Last Commit](https://img.shields.io/github/last-commit/AnaLauraCorrea/ShellDelphi?style=flat-square)](https://github.com/AnaLauraCorrea/ShellDelphi/commits) | Embeds a ConPTY-based PowerShell terminal directly into RAD Studio IDE to run interactive AI developer tooling like Claude Code. Enables agentic CLI workflows and terminal-based coding assistants inside native Delphi projects. | `Claude Code` `Agent Tooling` `IDE Plugin` `ConPTY` `VCL` |
| **[Claude-Tools-for-Delphi](https://github.com/GabrielOnDelphi/Claude-Tools-for-Delphi)** | [![Stars](https://img.shields.io/github/stars/GabrielOnDelphi/Claude-Tools-for-Delphi?style=flat-square)](https://github.com/GabrielOnDelphi/Claude-Tools-for-Delphi/stargazers)<br>[![Last Commit](https://img.shields.io/github/last-commit/GabrielOnDelphi/Claude-Tools-for-Delphi?style=flat-square)](https://github.com/GabrielOnDelphi/Claude-Tools-for-Delphi/commits) | Provides configured skills, prompts, and agent workflows tailored for Claude Code in Delphi environments. Enables automated Delphi code analysis and project management directly through Anthropic's CLI tooling. | `Claude Code` `Agent Tooling` `Prompt Optimization` `Delphi` |
| **[delphi-ide-remote-mcp](https://github.com/soporte-defontsoft/delphi-ide-remote-mcp)** | [![Stars](https://img.shields.io/github/stars/soporte-defontsoft/delphi-ide-remote-mcp?style=flat-square)](https://github.com/soporte-defontsoft/delphi-ide-remote-mcp/stargazers)<br>[![Last Commit](https://img.shields.io/github/last-commit/soporte-defontsoft/delphi-ide-remote-mcp?style=flat-square)](https://github.com/soporte-defontsoft/delphi-ide-remote-mcp/commits) | Model Context Protocol server exposing RAD Studio toolchains directly to AI coding agents. Enables remote MSBuild execution, PAServer deployment, and DelphiLSP code navigation under per-workspace security boundaries. | `MCP` `LSP` `MSBuild` `PAServer` `RAD Studio` |
| **[mcp-delphi](https://github.com/flydev-fr/mcp-delphi)** | [![Stars](https://img.shields.io/github/stars/flydev-fr/mcp-delphi?style=flat-square)](https://github.com/flydev-fr/mcp-delphi/stargazers)<br>[![Last Commit](https://img.shields.io/github/last-commit/flydev-fr/mcp-delphi?style=flat-square)](https://github.com/flydev-fr/mcp-delphi/commits) | Model Context Protocol server enabling LLM agents to compile, clean, and manage Delphi and Free Pascal/Lazarus projects directly. Bridges external AI tooling with command-line Pascal toolchains. | `MCP` `Delphi` `Lazarus` `FPC` `Agent Tooling` |
| **[mcp-firebird](https://github.com/danieleteti/mcp-firebird)** | [![Stars](https://img.shields.io/github/stars/danieleteti/mcp-firebird?style=flat-square)](https://github.com/danieleteti/mcp-firebird/stargazers)<br>[![Last Commit](https://img.shields.io/github/last-commit/danieleteti/mcp-firebird?style=flat-square)](https://github.com/danieleteti/mcp-firebird/commits) | Delphi-native Model Context Protocol server interfacing with Firebird databases via fbclient. Enables LLMs to inspect schemas, optimize queries, and analyze execution plans safely using read-only defaults. | `MCP` `Firebird` `Database AI` `Agent Tooling` |
| **[LingoFuse-pasAgent-v3](https://github.com/PassByYou888/LingoFuse-pasAgent-v3)** | [![Stars](https://img.shields.io/github/stars/PassByYou888/LingoFuse-pasAgent-v3?style=flat-square)](https://github.com/PassByYou888/LingoFuse-pasAgent-v3/stargazers)<br>[![Last Commit](https://img.shields.io/github/last-commit/PassByYou888/LingoFuse-pasAgent-v3?style=flat-square)](https://github.com/PassByYou888/LingoFuse-pasAgent-v3/commits) | Industrial-grade agent framework v3 bringing multimodal (vision + text) agent capabilities and cross-language MCP-API generation to Pascal. Enables LLMs to invoke Pascal functions and process image inputs with zero client-side changes. | `MCP` `Multimodal` `Agents` `Delphi` `FreePascal` |
| **[pascal-mcp](https://github.com/tina4stack/pascal-mcp)** | [![Stars](https://img.shields.io/github/stars/tina4stack/pascal-mcp?style=flat-square)](https://github.com/tina4stack/pascal-mcp/stargazers)<br>[![Last Commit](https://img.shields.io/github/last-commit/tina4stack/pascal-mcp?style=flat-square)](https://github.com/tina4stack/pascal-mcp/commits) | Model Context Protocol server enabling Claude and AI agents to interface with Free Pascal and Delphi RAD Studio environments. Provides tooling for codebase navigation, project building, and Pascal code manipulation. | `MCP` `Claude Code` `Free Pascal` `RAD Studio` `Delphi` |

---

## Code Intelligence & LSP (Language Server Protocol)

*Language Server Protocol (LSP) engines and symbol indexers that feed deep semantic understanding, definitions, and call hierarchies of large Pascal workspaces to AI coding assistants.*

🔍 **Live GitHub Searches:** [`delphi lsp`](https://github.com/search?q=delphi+lsp&type=repositories&s=updated&o=desc) · [`pascal lsp`](https://github.com/search?q=pascal+lsp&type=repositories&s=updated&o=desc) · [`language server protocol pascal`](https://github.com/search?q=language+server+protocol+pascal&type=repositories&s=updated&o=desc)

| Project | Stars & Health | Description | Tags |
| :--- | :---: | :--- | :--- |
| **[pascal-language-server](https://github.com/genericptr/pascal-language-server)** | [![Stars](https://img.shields.io/github/stars/genericptr/pascal-language-server?style=flat-square)](https://github.com/genericptr/pascal-language-server/stargazers)<br>[![Last Commit](https://img.shields.io/github/last-commit/genericptr/pascal-language-server?style=flat-square)](https://github.com/genericptr/pascal-language-server/commits) | Production-grade Language Server Protocol implementation for Pascal and FreePascal. Provides cross-editor code completion, jump-to-definition, and symbol navigation essential for modern developer tooling and agent context extraction. | `LSP` `Code Intelligence` `FreePascal` `Lazarus` |
| **[delphi-lookup](https://github.com/JavierusTk/delphi-lookup)** | [![Stars](https://img.shields.io/github/stars/JavierusTk/delphi-lookup?style=flat-square)](https://github.com/JavierusTk/delphi-lookup/stargazers)<br>[![Last Commit](https://img.shields.io/github/last-commit/JavierusTk/delphi-lookup?style=flat-square)](https://github.com/JavierusTk/delphi-lookup/commits) | High-speed symbol indexer and Delphi LSP provider designed to feed exact code context and symbol references across complex unit hierarchies directly to AI coding agents. | `LSP` `Code Intelligence` `Symbol Search` `Delphi` |
| **[LSP-Pascal-Library](https://github.com/rickard67/LSP-Pascal-Library)** | [![Stars](https://img.shields.io/github/stars/rickard67/LSP-Pascal-Library?style=flat-square)](https://github.com/rickard67/LSP-Pascal-Library/stargazers)<br>[![Last Commit](https://img.shields.io/github/last-commit/rickard67/LSP-Pascal-Library?style=flat-square)](https://github.com/rickard67/LSP-Pascal-Library/commits) | Object Pascal client library implementing the LSP protocol. Enables building custom CLI tools, CI verification bots, and agent integrations that query language servers. | `LSP` `Delphi` `Library` |
| **[PaskalCPP](https://github.com/tinyBigGAMES/PaskalCPP)** | [![Stars](https://img.shields.io/github/stars/tinyBigGAMES/PaskalCPP?style=flat-square)](https://github.com/tinyBigGAMES/PaskalCPP/stargazers)<br>[![Last Commit](https://img.shields.io/github/last-commit/tinyBigGAMES/PaskalCPP?style=flat-square)](https://github.com/tinyBigGAMES/PaskalCPP/commits) | PaskalCPP includes a native Delphi-built compiler and Language Server Protocol implementation for code diagnostics and editor integration. It provides an architecture reference for implementing custom LSP servers and AST parsing in Object Pascal. | `LSP` `Delphi` `Static Analysis` `Compiler` |
| **[pascal-lsp](https://github.com/andrei-markeev/pascal-lsp)** | [![Stars](https://img.shields.io/github/stars/andrei-markeev/pascal-lsp?style=flat-square)](https://github.com/andrei-markeev/pascal-lsp/stargazers)<br>[![Last Commit](https://img.shields.io/github/last-commit/andrei-markeev/pascal-lsp?style=flat-square)](https://github.com/andrei-markeev/pascal-lsp/commits) | Implements a high-performance Language Server Protocol backend for Pascal from scratch. Provides semantic analysis and code intelligence essential for AI coding assistants and modern IDE integrations. | `LSP` `Object Pascal` `FreePascal` `Static Analysis` `Code Intelligence` |

---

## AST, DFM & Codebase Analysis

*AST parsers, form extractors, and static analyzers that translate Object Pascal source files and binary DFMs into structured tokens for LLMs and automated refactoring.*

🔍 **Live GitHub Searches:** [`delphi ast`](https://github.com/search?q=delphi+ast&type=repositories&s=updated&o=desc) · [`pascal ast`](https://github.com/search?q=pascal+ast&type=repositories&s=updated&o=desc) · [`delphi static analysis`](https://github.com/search?q=delphi+static+analysis&type=repositories&s=updated&o=desc)

| Project | Stars & Health | Description | Tags |
| :--- | :---: | :--- | :--- |
| **[DelphiAST](https://github.com/RomanYankovsky/DelphiAST)** | [![Stars](https://img.shields.io/github/stars/RomanYankovsky/DelphiAST?style=flat-square)](https://github.com/RomanYankovsky/DelphiAST/stargazers)<br>[![Last Commit](https://img.shields.io/github/last-commit/RomanYankovsky/DelphiAST?style=flat-square)](https://github.com/RomanYankovsky/DelphiAST/commits) | Full-featured Abstract Syntax Tree (AST) generator for Delphi source code. The standard building block for building custom code refactorings, semantic analyzers, and LLM context extractors. | `AST` `Parsing` `Static Analysis` `Delphi` |
| **[StaticCodeAnalyser](https://github.com/nrodear/StaticCodeAnalyser)** | [![Stars](https://img.shields.io/github/stars/nrodear/StaticCodeAnalyser?style=flat-square)](https://github.com/nrodear/StaticCodeAnalyser/stargazers)<br>[![Last Commit](https://img.shields.io/github/last-commit/nrodear/StaticCodeAnalyser?style=flat-square)](https://github.com/nrodear/StaticCodeAnalyser/commits) | Static analysis engine for Delphi and Free Pascal with 200+ AST and DFM checks. Emits SARIF reports for automated agent-driven review and CI/CD quality gates. | `AST` `SARIF` `Delphi 12` `Lazarus` `Static Analysis` |
| **[Markdown4D](https://github.com/GDKsoftware/Markdown4D)** | [![Stars](https://img.shields.io/github/stars/GDKsoftware/Markdown4D?style=flat-square)](https://github.com/GDKsoftware/Markdown4D/stargazers)<br>[![Last Commit](https://img.shields.io/github/last-commit/GDKsoftware/Markdown4D?style=flat-square)](https://github.com/GDKsoftware/Markdown4D/commits) | High-speed CommonMark/GFM parser featuring a public AST and streaming parsing. Essential for parsing, formatting, and rendering LLM streaming responses in VCL and FMX interfaces. | `AST` `Markdown` `VCL` `FMX` `Streaming` |
| **[Neslib.Clang](https://github.com/neslib/Neslib.Clang)** | [![Stars](https://img.shields.io/github/stars/neslib/Neslib.Clang?style=flat-square)](https://github.com/neslib/Neslib.Clang/stargazers)<br>[![Last Commit](https://img.shields.io/github/last-commit/neslib/Neslib.Clang?style=flat-square)](https://github.com/neslib/Neslib.Clang/commits) | Delphi bindings for libclang. Enables AST parsing, semantic analysis, and tokenization of C/C++ headers to automate Delphi wrapper and binding generation. | `AST` `libclang` `Delphi 12` |

---

## Legacy Workflows & Encoding Bridges

*Tools solving character set encoding, line endings, and workspace friction when AI agents refactor legacy Delphi projects.*

🔍 **Live GitHub Searches:** [`delphi legacy utf8`](https://github.com/search?q=delphi+legacy+utf8&type=repositories&s=updated&o=desc) · [`delphi encoding bom`](https://github.com/search?q=delphi+encoding+bom&type=repositories&s=updated&o=desc)

| Project | Stars & Health | Description | Tags |
| :--- | :---: | :--- | :--- |
| **[mcp-file-tools](https://github.com/dimitar-grigorov/mcp-file-tools)** | [![Stars](https://img.shields.io/github/stars/dimitar-grigorov/mcp-file-tools?style=flat-square)](https://github.com/dimitar-grigorov/mcp-file-tools/stargazers)<br>[![Last Commit](https://img.shields.io/github/last-commit/dimitar-grigorov/mcp-file-tools?style=flat-square)](https://github.com/dimitar-grigorov/mcp-file-tools/commits) | Transparently prevents character set corruption when AI assistants edit legacy Delphi 7 through 2007 projects by safely handling ANSI, Windows-1252, and UTF-8 with BOM while preserving CRLF line endings. | `Legacy Migration` `Delphi 7` `Delphi 2007` `UTF-8 BOM` `MCP` |
| **[EncodingFixTool](https://github.com/MaxLogic/EncodingFixTool)** | [![Stars](https://img.shields.io/github/stars/MaxLogic/EncodingFixTool?style=flat-square)](https://github.com/MaxLogic/EncodingFixTool/stargazers)<br>[![Last Commit](https://img.shields.io/github/last-commit/MaxLogic/EncodingFixTool?style=flat-square)](https://github.com/MaxLogic/EncodingFixTool/commits) | Fast, parallel CLI utility tailored for Delphi projects to fix mixed legacy ANSI/UTF-8 encodings, enforce UTF-8 with BOM, and normalize CRLF line endings. Includes dedicated AI agent skills for Claude Code and Codex. | `UTF-8 BOM` `Encoding` `CRLF` `CLI` `Agent Skill` |
| **[chsdet](https://github.com/alexeydott/chsdet)** | [![Stars](https://img.shields.io/github/stars/alexeydott/chsdet?style=flat-square)](https://github.com/alexeydott/chsdet/stargazers)<br>[![Last Commit](https://img.shields.io/github/last-commit/alexeydott/chsdet?style=flat-square)](https://github.com/alexeydott/chsdet/commits) | Pure Delphi port of Mozilla's universal charset detector supporting Delphi 12 (Win32/Win64). Accurately identifies encodings, Windows code pages, and BOMs from raw streams or files without external DLLs. | `Charset Detector` `BOM` `Mozilla` `Delphi 12` `Encoding` |
| **[charset-enigma](https://github.com/rareMaxim/charset-enigma)** | [![Stars](https://img.shields.io/github/stars/rareMaxim/charset-enigma?style=flat-square)](https://github.com/rareMaxim/charset-enigma/stargazers)<br>[![Last Commit](https://img.shields.io/github/last-commit/rareMaxim/charset-enigma?style=flat-square)](https://github.com/rareMaxim/charset-enigma/commits) | Cross-platform Delphi charset and BOM detector (XE3 to 10.3+) supporting over 50 encodings (UTF-8, UTF-16, Cyrillic, Asian, European code pages) for legacy migration pipelines. | `Charset` `BOM` `Cross-Platform` `Delphi` |

---

## IDE Plugins & In-Editor Assistants

*AI-assisted chat, code generation, and inline refactoring embedded directly into RAD Studio via the ToolsAPI.*

🔍 **Live GitHub Searches:** [`delphi copilot`](https://github.com/search?q=delphi+copilot&type=repositories&s=updated&o=desc) · [`delphi ide plugin ai`](https://github.com/search?q=delphi+ide+plugin+ai&type=repositories&s=updated&o=desc) · [`rad studio ai`](https://github.com/search?q=rad+studio+ai&type=repositories&s=updated&o=desc)

| Project | Stars & Health | Description | Tags |
| :--- | :---: | :--- | :--- |
| **[FusionAI](https://github.com/AliDehbansiahkarbon/FusionAI)** | [![Stars](https://img.shields.io/github/stars/AliDehbansiahkarbon/FusionAI?style=flat-square)](https://github.com/AliDehbansiahkarbon/FusionAI/stargazers)<br>[![Last Commit](https://img.shields.io/github/last-commit/AliDehbansiahkarbon/FusionAI?style=flat-square)](https://github.com/AliDehbansiahkarbon/FusionAI/commits) | Comprehensive RAD Studio IDE plugin supporting OpenAI, Anthropic Claude, Google Gemini, and local Ollama instances for in-editor chat, inline code generation, and refactoring across Delphi XE5 to 12. | `RAD Studio` `ToolsAPI` `Multi-Provider` `Delphi 12` |
| **[Delphi AI Developer](https://github.com/Code4Delphi/Delphi-AI-Developer)** | [![Stars](https://img.shields.io/github/stars/Code4Delphi/Delphi-AI-Developer?style=flat-square)](https://github.com/Code4Delphi/Delphi-AI-Developer/stargazers)<br>[![Last Commit](https://img.shields.io/github/last-commit/Code4Delphi/Delphi-AI-Developer?style=flat-square)](https://github.com/Code4Delphi/Delphi-AI-Developer/commits) | Open-source RAD Studio plugin providing multi-provider AI chat, code completion, and refactoring directly inside the IDE. | `IDE Plugin` `ToolsAPI` `Multi-Provider` |
| **[RadIA-Plugin](https://github.com/regyssilveira/RadIA-Plugin)** | [![Stars](https://img.shields.io/github/stars/regyssilveira/RadIA-Plugin?style=flat-square)](https://github.com/regyssilveira/RadIA-Plugin/stargazers)<br>[![Last Commit](https://img.shields.io/github/last-commit/regyssilveira/RadIA-Plugin?style=flat-square)](https://github.com/regyssilveira/RadIA-Plugin/commits) | RAD Studio plugin leveraging Open Tools API and WebView2 with Server-Sent Events (SSE) for conversational AI assistance and contextual code editing. | `OTA` `WebView2` `Delphi IDE` `SSE` |
| **[RAD Studio Smart CodeInsight — Claude Patch](https://blogs.embarcadero.com/rad-studio-13-smart-codeinsight-claude-patch-released/)** | `Official` | Official Embarcadero patch adding Claude-powered code completion directly to Smart CodeInsight. | `RAD Studio 13` `GetIt` `Official` |
| **[ChatGPT](https://github.com/HemulGM/ChatGPT)** | [![Stars](https://img.shields.io/github/stars/HemulGM/ChatGPT?style=flat-square)](https://github.com/HemulGM/ChatGPT/stargazers)<br>[![Last Commit](https://img.shields.io/github/last-commit/HemulGM/ChatGPT?style=flat-square)](https://github.com/HemulGM/ChatGPT/commits) | Cross-platform FireMonkey desktop and mobile client interfacing directly with the OpenAI API. Provides production-grade patterns for streaming chat completions, token handling, and multi-OS deployment in Delphi. | `FMX` `Delphi 12` `OpenAI API` `Cross-Platform` `LLM Client` |

---

## AI Frameworks & Multi-Agent Orchestration

*Delphi-native architectures for building agentic workflows, RAG pipelines, and LLM applications.*

🔍 **Live GitHub Searches:** [`delphi agent`](https://github.com/search?q=delphi+agent&type=repositories&s=updated&o=desc) · [`pascal rag`](https://github.com/search?q=pascal+rag&type=repositories&s=updated&o=desc) · [`delphi vector`](https://github.com/search?q=delphi+vector&type=repositories&s=updated&o=desc)

| Project | Stars & Health | Description | Tags |
| :--- | :---: | :--- | :--- |
| **[MakerAI](https://github.com/gustavoeenriquez/MakerAi)** | [![Stars](https://img.shields.io/github/stars/gustavoeenriquez/MakerAi?style=flat-square)](https://github.com/gustavoeenriquez/MakerAi/stargazers)<br>[![Last Commit](https://img.shields.io/github/last-commit/gustavoeenriquez/MakerAi?style=flat-square)](https://github.com/gustavoeenriquez/MakerAi/commits) | Embedded framework for building AI-powered Delphi applications. Provides Vector RAG (HNSW + BM25), Graph RAG, autonomous multi-node agent thread pools, runtime-swappable LLM connectors, and MCP support. | `RAG` `Agents` `Vector DB` `FPC` |
| **[PasClaw](https://github.com/FMXExpress/PasClaw)** | [![Stars](https://img.shields.io/github/stars/FMXExpress/PasClaw?style=flat-square)](https://github.com/FMXExpress/PasClaw/stargazers)<br>[![Last Commit](https://img.shields.io/github/last-commit/FMXExpress/PasClaw?style=flat-square)](https://github.com/FMXExpress/PasClaw/commits) | Lightweight autonomous AI agent framework in Object Pascal featuring tool calling and task orchestration for Delphi and FreePascal. | `Agents` `Tool Calling` `FMX` `VCL` `Lazarus` |
| **[SmartCore AI Components Pack](https://blogs.embarcadero.com/introducing-the-smartcore-ai-components-pack/)** | `Official` | Official Embarcadero AI component suite with engine-agnostic connection components (OpenAI, Claude, Gemini, Ollama), structured JSON request handling, and direct UI data binding. | `RAD Studio 13` `GetIt` `Official` |

---

## Local / On-Device Inference (Delphi-Native)

*Run local LLMs, SLMs, and neural networks on-device without cloud dependencies, API keys, or external Python runtimes.*

🔍 **Live GitHub Searches:** [`delphi llama`](https://github.com/search?q=delphi+llama&type=repositories&s=updated&o=desc) · [`pascal onnx`](https://github.com/search?q=pascal+onnx&type=repositories&s=updated&o=desc) · [`delphi gguf`](https://github.com/search?q=delphi+gguf&type=repositories&s=updated&o=desc)

| Project | Stars & Health | Description | Tags |
| :--- | :---: | :--- | :--- |
| **[VindexLLM](https://github.com/tinyBigGAMES/VindexLLM)** | [![Stars](https://img.shields.io/github/stars/tinyBigGAMES/VindexLLM?style=flat-square)](https://github.com/tinyBigGAMES/VindexLLM/stargazers)<br>[![Last Commit](https://img.shields.io/github/last-commit/tinyBigGAMES/VindexLLM?style=flat-square)](https://github.com/tinyBigGAMES/VindexLLM/commits) | Native Delphi GPU inference engine executing GGUF transformer models via Vulkan compute shaders. Zero external runtime dependencies (no Python, no CUDA)—requires only vulkan-1.dll. | `Local Inference` `GGUF` `Vulkan GPU` `Zero-Dependency` |
| **[LlamaKit](https://github.com/gustavoeenriquez/LlamaKit)** | [![Stars](https://img.shields.io/github/stars/gustavoeenriquez/LlamaKit?style=flat-square)](https://github.com/gustavoeenriquez/LlamaKit/stargazers)<br>[![Last Commit](https://img.shields.io/github/last-commit/gustavoeenriquez/LlamaKit?style=flat-square)](https://github.com/gustavoeenriquez/LlamaKit/commits) | Local LLM inference using llama.cpp GGUF models with compiled Windows DLLs and native Delphi wrapper components. | `llama.cpp` `GGUF` `Local` |
| **[llama-cpp-delphi](https://github.com/Embarcadero/llama-cpp-delphi)** | [![Stars](https://img.shields.io/github/stars/Embarcadero/llama-cpp-delphi?style=flat-square)](https://github.com/Embarcadero/llama-cpp-delphi/stargazers)<br>[![Last Commit](https://img.shields.io/github/last-commit/Embarcadero/llama-cpp-delphi?style=flat-square)](https://github.com/Embarcadero/llama-cpp-delphi/commits) | Official Embarcadero wrapper around llama.cpp for local GGUF model execution. | `llama.cpp` `Embarcadero` `Official` |
| **[Dllama](https://github.com/tinyBigGAMES/Dllama)** | [![Stars](https://img.shields.io/github/stars/tinyBigGAMES/Dllama?style=flat-square)](https://github.com/tinyBigGAMES/Dllama/stargazers)<br>[![Last Commit](https://img.shields.io/github/last-commit/tinyBigGAMES/Dllama?style=flat-square)](https://github.com/tinyBigGAMES/Dllama/commits) | Lightweight Delphi binding for llama.cpp, supporting Ollama-compatible GGUF models (Llama, Mistral, Gemma). | `llama.cpp` `GGUF` |
| **[TONNXRuntime](https://github.com/hshatti/TONNXRuntime)** | [![Stars](https://img.shields.io/github/stars/hshatti/TONNXRuntime?style=flat-square)](https://github.com/hshatti/TONNXRuntime/stargazers)<br>[![Last Commit](https://img.shields.io/github/last-commit/hshatti/TONNXRuntime?style=flat-square)](https://github.com/hshatti/TONNXRuntime/commits) | Microsoft ONNX Runtime bindings for FreePascal and Delphi for running pre-trained neural networks on desktop and edge devices. | `ONNX` `Lazarus` `Delphi` |
| **[Ollama-Delphi-GUI](https://github.com/HuichanKIM/Ollama-Delphi-GUI)** | [![Stars](https://img.shields.io/github/stars/HuichanKIM/Ollama-Delphi-GUI?style=flat-square)](https://github.com/HuichanKIM/Ollama-Delphi-GUI/stargazers)<br>[![Last Commit](https://img.shields.io/github/last-commit/HuichanKIM/Ollama-Delphi-GUI?style=flat-square)](https://github.com/HuichanKIM/Ollama-Delphi-GUI/commits) | Delphi desktop client demonstrating real-time local model streaming and chat interface patterns over Ollama's REST API. | `Ollama` `VCL` `Desktop UI` |

---

## Cloud LLM API Clients

*Robust, actively maintained Delphi SDKs for calling major AI provider APIs directly from Object Pascal.*

🔍 **Live GitHub Searches:** [`delphi openai`](https://github.com/search?q=delphi+openai&type=repositories&s=updated&o=desc) · [`delphi anthropic`](https://github.com/search?q=delphi+anthropic&type=repositories&s=updated&o=desc) · [`delphi gemini`](https://github.com/search?q=delphi+gemini&type=repositories&s=updated&o=desc) · [`delphi deepseek`](https://github.com/search?q=delphi+deepseek&type=repositories&s=updated&o=desc)

| Project | Stars & Health | Description | Tags |
| :--- | :---: | :--- | :--- |
| **[DelphiAnthropic](https://github.com/MaxiDonkey/DelphiAnthropic)** | [![Stars](https://img.shields.io/github/stars/MaxiDonkey/DelphiAnthropic?style=flat-square)](https://github.com/MaxiDonkey/DelphiAnthropic/stargazers)<br>[![Last Commit](https://img.shields.io/github/last-commit/MaxiDonkey/DelphiAnthropic?style=flat-square)](https://github.com/MaxiDonkey/DelphiAnthropic/commits) | Full Anthropic SDK covering Claude 3.5 & 3.7, vision, prompt caching, tool use, batch processing, and streaming. | `Anthropic` `Claude 3.7` `Prompt Caching` |
| **[DelphiOpenAI](https://github.com/HemulGM/DelphiOpenAI)** | [![Stars](https://img.shields.io/github/stars/HemulGM/DelphiOpenAI?style=flat-square)](https://github.com/HemulGM/DelphiOpenAI/stargazers)<br>[![Last Commit](https://img.shields.io/github/last-commit/HemulGM/DelphiOpenAI?style=flat-square)](https://github.com/HemulGM/DelphiOpenAI/commits) | Feature-complete OpenAI client (ChatGPT, Whisper, DALL-E, embeddings, function calling). Also connects to Azure, DeepSeek, and Ollama. | `OpenAI` `GPT-4o` `Function Calling` |
| **[DelphiGenAI](https://github.com/MaxiDonkey/DelphiGenAI)** | [![Stars](https://img.shields.io/github/stars/MaxiDonkey/DelphiGenAI?style=flat-square)](https://github.com/MaxiDonkey/DelphiGenAI/stargazers)<br>[![Last Commit](https://img.shields.io/github/last-commit/MaxiDonkey/DelphiGenAI?style=flat-square)](https://github.com/MaxiDonkey/DelphiGenAI/commits) | OpenAI client supporting GPT-4o, vision, audio, embeddings, and agentic workflows. | `OpenAI` `Multimodal` `Embeddings` |
| **[openai-delphi](https://github.com/landgraf-dev/openai-delphi)** | [![Stars](https://img.shields.io/github/stars/landgraf-dev/openai-delphi?style=flat-square)](https://github.com/landgraf-dev/openai-delphi/stargazers)<br>[![Last Commit](https://img.shields.io/github/last-commit/landgraf-dev/openai-delphi?style=flat-square)](https://github.com/landgraf-dev/openai-delphi/commits) | Lightweight, clean OpenAI client with full FreePascal and Lazarus compatibility. | `OpenAI` `Lazarus` `FPC` |
| **[DelphiGemini](https://github.com/MaxiDonkey/DelphiGemini)** | [![Stars](https://img.shields.io/github/stars/MaxiDonkey/DelphiGemini?style=flat-square)](https://github.com/MaxiDonkey/DelphiGemini/stargazers)<br>[![Last Commit](https://img.shields.io/github/last-commit/MaxiDonkey/DelphiGemini?style=flat-square)](https://github.com/MaxiDonkey/DelphiGemini/commits) | Google Gemini SDK supporting multimodal prompts, code generation, caching, and fine-tuning. | `Google Gemini` `Multimodal` `Caching` |
| **[Gemini4Delphi](https://github.com/delmardelima/Gemini4Delphi)** | [![Stars](https://img.shields.io/github/stars/delmardelima/Gemini4Delphi?style=flat-square)](https://github.com/delmardelima/Gemini4Delphi/stargazers)<br>[![Last Commit](https://img.shields.io/github/last-commit/delmardelima/Gemini4Delphi?style=flat-square)](https://github.com/delmardelima/Gemini4Delphi/commits) | Lightweight Google Gemini bridge for Delphi. | `Google Gemini` `Delphi` |
| **[DelphiDeepseek](https://github.com/MaxiDonkey/DelphiDeepseek)** | [![Stars](https://img.shields.io/github/stars/MaxiDonkey/DelphiDeepseek?style=flat-square)](https://github.com/MaxiDonkey/DelphiDeepseek/stargazers)<br>[![Last Commit](https://img.shields.io/github/last-commit/MaxiDonkey/DelphiDeepseek?style=flat-square)](https://github.com/MaxiDonkey/DelphiDeepseek/commits) | DeepSeek reasoning model wrapper with local LM Studio compatibility. | `DeepSeek` `Reasoning` `LM Studio` |
| **[DelphiGroqCloud](https://github.com/MaxiDonkey/DelphiGroqCloud)** | [![Stars](https://img.shields.io/github/stars/MaxiDonkey/DelphiGroqCloud?style=flat-square)](https://github.com/MaxiDonkey/DelphiGroqCloud/stargazers)<br>[![Last Commit](https://img.shields.io/github/last-commit/MaxiDonkey/DelphiGroqCloud?style=flat-square)](https://github.com/MaxiDonkey/DelphiGroqCloud/commits) | Groq LPU cloud API wrapper for ultra-low latency model inference. | `Groq` `Fast Inference` `LPU` |
| **[DelphiMistralAI](https://github.com/MaxiDonkey/DelphiMistralAI)** | [![Stars](https://img.shields.io/github/stars/MaxiDonkey/DelphiMistralAI?style=flat-square)](https://github.com/MaxiDonkey/DelphiMistralAI/stargazers)<br>[![Last Commit](https://img.shields.io/github/last-commit/MaxiDonkey/DelphiMistralAI?style=flat-square)](https://github.com/MaxiDonkey/DelphiMistralAI/commits) | Mistral SDK covering Codestral, vision, embeddings, and agentic conversations. | `Mistral` `Codestral` `Embeddings` |
| **[RDOpenAI](https://github.com/baumwollschaf/RDOpenAI)** | [![Stars](https://img.shields.io/github/stars/baumwollschaf/RDOpenAI?style=flat-square)](https://github.com/baumwollschaf/RDOpenAI/stargazers)<br>[![Last Commit](https://img.shields.io/github/last-commit/baumwollschaf/RDOpenAI?style=flat-square)](https://github.com/baumwollschaf/RDOpenAI/commits) | Event-driven Delphi component wrapper for interacting with the OpenAI ChatGPT API. Simplifies asynchronous streaming and response handling in VCL/FMX desktop applications. | `OpenAI` `ChatGPT` `Cloud LLM` `VCL` `FMX` |
| **[delphi-ai-skills](https://github.com/danieleteti/delphi-ai-skills)** | [![Stars](https://img.shields.io/github/stars/danieleteti/delphi-ai-skills?style=flat-square)](https://github.com/danieleteti/delphi-ai-skills/stargazers)<br>[![Last Commit](https://img.shields.io/github/last-commit/danieleteti/delphi-ai-skills?style=flat-square)](https://github.com/danieleteti/delphi-ai-skills/commits) | Collection of domain-specific instructions and skills enabling LLMs like Claude, Gemini, and Cursor to generate idiomatic Delphi, DMVCFramework, and JSON-RPC code. It standardizes Delphi coding conventions and anti-pattern detection across AI programming assistants. | `Claude Code` `Cursor` `DMVCFramework` `Prompt Engineering` `Code Smell` |
| **[file2knowledge](https://github.com/MaxiDonkey/file2knowledge)** | [![Stars](https://img.shields.io/github/stars/MaxiDonkey/file2knowledge?style=flat-square)](https://github.com/MaxiDonkey/file2knowledge/stargazers)<br>[![Last Commit](https://img.shields.io/github/last-commit/MaxiDonkey/file2knowledge?style=flat-square)](https://github.com/MaxiDonkey/file2knowledge/commits) | Delphi reference implementation demonstrating OpenAI API integration, vector store search, and session-based RAG workflows. It serves as a practical blueprint for deep research and generative AI interactions in Object Pascal. | `Delphi` `OpenAI` `RAG` `Vector Search` `LLM` |
| **[Toon4D](https://github.com/GDKsoftware/Toon4D)** | [![Stars](https://img.shields.io/github/stars/GDKsoftware/Toon4D?style=flat-square)](https://github.com/GDKsoftware/Toon4D/stargazers)<br>[![Last Commit](https://img.shields.io/github/last-commit/GDKsoftware/Toon4D?style=flat-square)](https://github.com/GDKsoftware/Toon4D/commits) | Delphi library encoding JSON data into TOON format to cut token usage in LLM prompts by 30-60%. Optimizes context window consumption and API billing for data-heavy AI workflows. | `Delphi` `LLM` `Prompt Optimization` `JSON` |

---

## Testing & GUI Automation

*AI-driven and automated testing tools for validating Delphi application behavior.*

🔍 **Live GitHub Searches:** [`delphi test automation`](https://github.com/search?q=delphi+test+automation&type=repositories&s=updated&o=desc) · [`claude code delphi`](https://github.com/search?q=claude+code+delphi&type=repositories&s=updated&o=desc)

| Project | Stars & Health | Description | Tags |
| :--- | :---: | :--- | :--- |
| **[Autopilot for Delphi](https://github.com/GabrielOnDelphi/Autopilot-for-Delphi)** | [![Stars](https://img.shields.io/github/stars/GabrielOnDelphi/Autopilot-for-Delphi?style=flat-square)](https://github.com/GabrielOnDelphi/Autopilot-for-Delphi/stargazers)<br>[![Last Commit](https://img.shields.io/github/last-commit/GabrielOnDelphi/Autopilot-for-Delphi?style=flat-square)](https://github.com/GabrielOnDelphi/Autopilot-for-Delphi/commits) | Drives running VCL/FMX forms via MCP or DUnitX: clicks controls, verifies labels, dismisses dialogs, and validates screens without moving the physical mouse. | `VCL` `FMX` `GUI Automation` `DUnitX` |
| **[ClaudeCode TokenVampire](https://github.com/GabrielOnDelphi/ClaudeCode_TokenVampire)** | [![Stars](https://img.shields.io/github/stars/GabrielOnDelphi/ClaudeCode_TokenVampire?style=flat-square)](https://github.com/GabrielOnDelphi/ClaudeCode_TokenVampire/stargazers)<br>[![Last Commit](https://img.shields.io/github/last-commit/GabrielOnDelphi/ClaudeCode_TokenVampire?style=flat-square)](https://github.com/GabrielOnDelphi/ClaudeCode_TokenVampire/commits) | Real-time token usage monitor for Claude Code sessions. Displays rolling window quotas, cache hit rates, and cost estimates via offline log analysis. | `Claude Code` `DevEx` `Token Optimization` |

---

## Curated Lists & Community Directories

*Other curated directories and meta-catalogs in the Delphi ecosystem.*

🔍 **Live GitHub Searches:** [`awesome delphi`](https://github.com/search?q=awesome+delphi&type=repositories&s=updated&o=desc) · [`awesome pascal`](https://github.com/search?q=awesome+pascal&type=repositories&s=updated&o=desc)

| Project | Stars & Health | Description | Tags |
| :--- | :---: | :--- | :--- |
| **[Awesome-AI-For-Delphi](https://github.com/GabrielOnDelphi/Awesome-AI-For-Delphi)** | [![Stars](https://img.shields.io/github/stars/GabrielOnDelphi/Awesome-AI-For-Delphi?style=flat-square)](https://github.com/GabrielOnDelphi/Awesome-AI-For-Delphi/stargazers)<br>[![Last Commit](https://img.shields.io/github/last-commit/GabrielOnDelphi/Awesome-AI-For-Delphi?style=flat-square)](https://github.com/GabrielOnDelphi/Awesome-AI-For-Delphi/commits) | Gabriel Moraru's curated repository collection that served as an early inspiration for structuring and expanding this modernized, MCP/LSP-focused, and automated discovery edition. | `Curated List` `Delphi AI` `Inspiration` |
| **[Awesome Delphi](https://github.com/PassKit/Awesome-Delphi)** | [![Stars](https://img.shields.io/github/stars/PassKit/Awesome-Delphi?style=flat-square)](https://github.com/PassKit/Awesome-Delphi/stargazers)<br>[![Last Commit](https://img.shields.io/github/last-commit/PassKit/Awesome-Delphi?style=flat-square)](https://github.com/PassKit/Awesome-Delphi/commits) | The classic comprehensive directory of open-source Delphi libraries, frameworks, components, and tools. | `Awesome List` `Delphi` `General Catalog` |

---

## Community & Resources

### Global Communities
* **[Delphi-PRAXiS (English)](https://en.delphipraxis.net/)** & **[German Edition](https://www.delphipraxis.net/)**  
  The largest independent global Delphi forum, featuring dedicated discussions on [AI-Assisted Coding](https://en.delphipraxis.net/forum/43-ai-assisted-coding/), LLM integration, and modern Pascal practices.
* **[Embarcadero Community & Developer Blogs](https://blogs.embarcadero.com/)**  
  Official developer blogs, product updates, SmartCore AI news, and technical deep-dives from Embarcadero architects.
* **[Reddit r/delphi](https://www.reddit.com/r/delphi/)**  
  Active community subreddit for Delphi and Object Pascal news, tooling, and open-source project showcases.
* **[Claude Code Training for Delphi Developers](https://training.gdksoftware.com/)**  
  Specialized hands-on training by GDK Software covering CLAUDE.md architecture, MCP setups, and Delphi agent workflows. `[Commercial]`

### Turkish Communities (Türkiye)
* **[DelphiCan](https://www.delphican.com/)**  
  Türkiye'nin en aktif ve kapsamlı Delphi & Object Pascal geliştirici topluluğu; VCL, FMX, modern mimariler, API ve yapay zekâ tartışmaları.
* **[Delphi Türkiye Forum](https://www.delphiturkiye.com/forum/)**  
  1998'den beri Türkiye Delphi ekosisteminin en köklü bilgi bankası ve teknik tartışma forumu (`delphiturkiye.com`).

---

## Contributing

Contributions and recommendations are warmly welcome!
1. **Focus:** Must enhance Delphi or Object Pascal development with AI, MCP, LSP, AST analysis, or modern developer workflows.
2. **Quality & Distribution:** Open-source and actively maintained repositories are prioritized. Commercial or closed-source distribution tools must be uniquely valuable and clearly tagged `[Commercial]`.
3. **Format:** Submit a Pull Request following the established categorization and tag conventions.

---

## Security & Disclaimer

> ⚠️ **Important Notice & Due Diligence**
>
> 1. **Index & Catalog Only:** This repository is an automated, community-curated index. Inclusion of any project does **not** constitute an endorsement, code audit, or verification of its security posture.
> 2. **Untested Third-Party Code:** The maintainers have **not** compiled, audited, executed, or tested every third-party repository, binary, script, or library referenced in this list.
> 3. **Developer Responsibility:** Before integrating third-party code, pre-compiled binaries (`.dll`, `.so`, `.bpl`), MCP servers, or dependencies into your local development environments, corporate workstations, or production systems, you are solely responsible for inspecting source code, validating build scripts, and conducting thorough security audits.
> 4. **No Warranty:** All resources and links are provided strictly *"as is"*, without warranty of any kind, express or implied. In no event shall the maintainers be held liable for any damages, vulnerabilities, data loss, or system compromises resulting from the use of linked software.
