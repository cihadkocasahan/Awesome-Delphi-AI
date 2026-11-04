# Awesome Delphi AI [![Awesome](https://awesome.re/badge.svg)](https://awesome.re) [![Otonom Kürasyon](https://img.shields.io/badge/K%C3%BCrasyon-Hermes_AI_Agent-8A2BE2?style=flat-square)](https://github.com/cihadkocasahan/Awesome-Delphi-AI)

[🇬🇧 English](README.md) · [🇹🇷 Türkçe](README.tr.md)

> Modern Delphi ve Object Pascal geliştiricileri için yapay zekâ araçları, kütüphaneler, Model Context Protocol (MCP) sunucuları, LSP motorları ve otonom kodlama iş akışlarının özenle seçilmiş açık kaynak kataloğu.
>
> 🤖 **Otonom Keşif ve Güncelleme:** Bu liste, ekosistemi düzenli olarak tarayan, projeleri değerlendiren ve güncelleyen **Hermes Yapay Zekâ Ajanı** tarafından otomatik olarak yönetilmektedir.

Bu kürasyon, Delphi yazılımcılarının **geliştirici deneyimini (DevEx) ve modern yazılım mühendisliği pratiklerini** güçlendirmeye odaklanır: Otonom kodlama ajanları (Claude Code, Cursor, Copilot), MCP protokolü üzerinden canlı derleyici/hata ayıklama denetimi, LSP ile semantik kod zekâsı, LLM bağlamı için AST/DFM ayrıştırma ve yerel (on-device) sinir ağı çıkarımı.

---

## İçindekiler

- [Yapay Zekâ Ajan Araçları ve MCP (Model Context Protocol)](#yapay-zekâ-ajan-araçları-ve-mcp-model-context-protocol)
- [Kod Zekâsı ve LSP (Language Server Protocol)](#kod-zekâsı-ve-lsp-language-server-protocol)
- [AST, DFM ve Kod Tabanı Statik Analizi](#ast-dfm-ve-kod-tabanı-statik-analizi)
- [Eski Kod Tabanları ve Karakter Kodlama Köprüleri](#eski-kod-tabanları-ve-karakter-kodlama-köprüleri)
- [IDE Eklentileri ve Editör İçi Asistanlar](#ide-eklentileri-ve-editör-içi-asistanlar)
- [Yapay Zekâ Çatıları ve Çoklu Ajan Orkestrasyonu](#yapay-zekâ-çatıları-ve-çoklu-ajan-orkestrasyonu)
- [Cihaz Üzerinde Yerel Çıkarım (Delphi-Native Inference)](#cihaz-üzerinde-yerel-çıkarım-delphi-native-inference)
- [Bulut LLM API İstemcileri](#bulut-llm-api-istemcileri)
- [Test ve GUI Otomasyonu](#test-ve-gui-otomasyonu)
- [Derlenmiş Listeler ve Topluluk Dizinleri](#derlenmiş-listeler-ve-topluluk-dizinleri)
- [Topluluk ve Kaynaklar](#topluluk-ve-kaynaklar)
- [Katkıda Bulunma (Contributing)](#katkıda-bulunma-contributing)
- [Güvenlik Uyarısı ve Sorumluluk Reddi (Disclaimer)](#güvenlik-uyarısı-ve-sorumluluk-reddi-disclaimer)

---

## Yapay Zekâ Ajan Araçları ve MCP (Model Context Protocol)

*MCP sunucuları, otonom yapay zekâ kodlama ajanlarının (Claude Code, Cursor, Codex) Delphi derleyicileri, hata ayıklayıcıları, çalışan süreçler ve proje ağacıyla doğrudan iletişim kurmasını sağlar.*

🔍 **Canlı GitHub Aramaları:** [`delphi mcp`](https://github.com/search?q=delphi+mcp&type=repositories&s=updated&o=desc) · [`pascal mcp`](https://github.com/search?q=pascal+mcp&type=repositories&s=updated&o=desc) · [`delphi model context protocol`](https://github.com/search?q=delphi+model+context+protocol&type=repositories&s=updated&o=desc)

| Proje | Yıldız ve Durum | Açıklama | Etiketler |
| :--- | :---: | :--- | :--- |
| **[MARS](https://github.com/andrea-magni/MARS)** | [![Stars](https://img.shields.io/github/stars/andrea-magni/MARS?style=flat-square)](https://github.com/andrea-magni/MARS/stargazers)<br>[![Last Commit](https://img.shields.io/github/last-commit/andrea-magni/MARS?style=flat-square)](https://github.com/andrea-magni/MARS/commits) | Model Context Protocol (MCP) sunucu desteğine sahip yüksek performanslı Delphi REST çatısı. Delphi iş kurallarını, veritabanı sorgularını ve fonksiyonlarını Server-Sent Events (SSE) ile doğrudan yapay zekâ ajanlarına araç olarak açar. | `MCP` `SSE` `Delphi 12` `OpenAPI` `Linux` |
| **[MCPConnect](https://github.com/delphi-blocks/MCPConnect)** | [![Stars](https://img.shields.io/github/stars/delphi-blocks/MCPConnect?style=flat-square)](https://github.com/delphi-blocks/MCPConnect/stargazers)<br>[![Last Commit](https://img.shields.io/github/last-commit/delphi-blocks/MCPConnect?style=flat-square)](https://github.com/delphi-blocks/MCPConnect/commits) | Model Context Protocol protokolünün yerel Object Pascal uygulaması. Delphi masaüstü ve sunucu uygulamaları içinde özel MCP araçları ve kaynak sağlayıcıları oluşturmayı kolaylaştırır. | `MCP` `Agent Tooling` `Delphi` |
| **[DPT — Delphi Processing Tools](https://github.com/WladiD/WDDelphiTools/tree/master/Projects/DPT)** | [![Stars](https://img.shields.io/github/stars/WladiD/WDDelphiTools?style=flat-square)](https://github.com/WladiD/WDDelphiTools/stargazers)<br>[![Last Commit](https://img.shields.io/github/last-commit/WladiD/WDDelphiTools?style=flat-square)](https://github.com/WladiD/WDDelphiTools/commits) | Özel bir MCP debugger sunucusuna sahip Delphi CLI aracı. Claude Code ve benzeri ajanların IDE açmadan hata ayıklama başlatmasına, kesme noktası koymasına, çağrı yığınını (call stack) ve bellek kayıtlarını okumasına olanak tanır. | `MCP` `CLI` `Debugger` `CI/CD` |
| **[delphi-visual-studio-code-debugger](https://github.com/csm101/delphi-visual-studio-code-debugger)** | [![Stars](https://img.shields.io/github/stars/csm101/delphi-visual-studio-code-debugger?style=flat-square)](https://github.com/csm101/delphi-visual-studio-code-debugger/stargazers)<br>[![Last Commit](https://img.shields.io/github/last-commit/csm101/delphi-visual-studio-code-debugger?style=flat-square)](https://github.com/csm101/delphi-visual-studio-code-debugger/commits) | Gömülü MCP sunucusu içeren Delphi hata ayıklayıcısı; yapay zekâ asistanlarına modern editörlerde derlenmiş Delphi ikililerini çalıştırma, denetleme ve hata ayıklama yeteneği kazandırır. | `MCP` `VSCode` `DAP` |
| **[Delphi-MCP-Server](https://github.com/GDKsoftware/Delphi-MCP-Server)** | [![Stars](https://img.shields.io/github/stars/GDKsoftware/Delphi-MCP-Server?style=flat-square)](https://github.com/GDKsoftware/Delphi-MCP-Server/stargazers)<br>[![Last Commit](https://img.shields.io/github/last-commit/GDKsoftware/Delphi-MCP-Server?style=flat-square)](https://github.com/GDKsoftware/Delphi-MCP-Server/commits) | Yerel `localhost:3000/mcp` üzerinde dinleyen saf Delphi MCP sunucusu. Claude Desktop, Cursor ve Claude Code ile entegre olarak Delphi proje bağlamı sağlar. | `MCP` `Claude Code` `Claude Desktop` |
| **[mxLore](https://github.com/MicrotronX/mxLore)** | [![Stars](https://img.shields.io/github/stars/MicrotronX/mxLore?style=flat-square)](https://github.com/MicrotronX/mxLore/stargazers)<br>[![Last Commit](https://img.shields.io/github/last-commit/MicrotronX/mxLore?style=flat-square)](https://github.com/MicrotronX/mxLore/commits) | Delphi ve FreePascal/Lazarus genelinde yapay zekâ kodlama ajanları için kalıcı hafıza, oturum takibi ve araç yürütme sunan yerel Pascal MCP sunucusu. | `MCP` `Claude Code` `FreePascal` `Lazarus` |
| **[Delphi-LSP-MCP-Server](https://github.com/SkybuckFlying/Delphi-LSP-MCP-Server)** | [![Stars](https://img.shields.io/github/stars/SkybuckFlying/Delphi-LSP-MCP-Server?style=flat-square)](https://github.com/SkybuckFlying/Delphi-LSP-MCP-Server/stargazers)<br>[![Last Commit](https://img.shields.io/github/last-commit/SkybuckFlying/Delphi-LSP-MCP-Server?style=flat-square)](https://github.com/SkybuckFlying/Delphi-LSP-MCP-Server/commits) | MCP taleplerini doğrudan Embarcadero nun resmi `DelphiLSP.exe` servisine yönlendirerek sembol arama, tanım ve referansları yapay zekâya bağlar. | `MCP` `DelphiLSP` |

---

## Kod Zekâsı ve LSP (Language Server Protocol)

*Geniş Pascal projelerinin semantik yapısını, tip tanımlarını ve çağrı hiyerarşilerini yapay zekâ kodlama asistanlarına aktaran Language Server Protocol (LSP) motorları ve sembol dizinleyicileri.*

🔍 **Canlı GitHub Aramaları:** [`delphi lsp`](https://github.com/search?q=delphi+lsp&type=repositories&s=updated&o=desc) · [`pascal lsp`](https://github.com/search?q=pascal+lsp&type=repositories&s=updated&o=desc) · [`language server protocol pascal`](https://github.com/search?q=language+server+protocol+pascal&type=repositories&s=updated&o=desc)

| Proje | Yıldız ve Durum | Açıklama | Etiketler |
| :--- | :---: | :--- | :--- |
| **[pascal-language-server](https://github.com/genericptr/pascal-language-server)** | [![Stars](https://img.shields.io/github/stars/genericptr/pascal-language-server?style=flat-square)](https://github.com/genericptr/pascal-language-server/stargazers)<br>[![Last Commit](https://img.shields.io/github/last-commit/genericptr/pascal-language-server?style=flat-square)](https://github.com/genericptr/pascal-language-server/commits) | Pascal ve FreePascal için üretim kalitesinde LSP uygulaması. Editör bağımsız kod tamamlama, tanıma gitme (definition) ve sembol gezinimi sağlar. | `LSP` `Code Intelligence` `FreePascal` `Lazarus` |
| **[delphi-lookup](https://github.com/JavierusTk/delphi-lookup)** | [![Stars](https://img.shields.io/github/stars/JavierusTk/delphi-lookup?style=flat-square)](https://github.com/JavierusTk/delphi-lookup/stargazers)<br>[![Last Commit](https://img.shields.io/github/last-commit/JavierusTk/delphi-lookup?style=flat-square)](https://github.com/JavierusTk/delphi-lookup/commits) | Karmaşık unit hiyerarşilerindeki kod bağlamını ve sembol referanslarını doğrudan yapay zekâ ajanlarına beslemek için tasarlanmış yüksek hızlı sembol dizinleyici ve Delphi LSP sağlayıcısı. | `LSP` `Code Intelligence` `Symbol Search` `Delphi` |
| **[LSP-Pascal-Library](https://github.com/rickard67/LSP-Pascal-Library)** | [![Stars](https://img.shields.io/github/stars/rickard67/LSP-Pascal-Library?style=flat-square)](https://github.com/rickard67/LSP-Pascal-Library/stargazers)<br>[![Last Commit](https://img.shields.io/github/last-commit/rickard67/LSP-Pascal-Library?style=flat-square)](https://github.com/rickard67/LSP-Pascal-Library/commits) | LSP protokolünü uygulayan Object Pascal istemci kütüphanesi. Dil sunucularını sorgulayan CLI araçları ve CI doğrulama botları geliştirmeyi mümkün kılar. | `LSP` `Delphi` `Library` |

---

## AST, DFM ve Kod Tabanı Statik Analizi

*Object Pascal kaynak kodlarını ve ikili DFM form dosyalarını LLM ler ve otomatik refactoring araçları için yapılandırılmış token lara dönüştüren AST ayrıştırıcılar ve statik analiz motorları.*

🔍 **Canlı GitHub Aramaları:** [`delphi ast`](https://github.com/search?q=delphi+ast&type=repositories&s=updated&o=desc) · [`pascal ast`](https://github.com/search?q=pascal+ast&type=repositories&s=updated&o=desc) · [`delphi static analysis`](https://github.com/search?q=delphi+static+analysis&type=repositories&s=updated&o=desc)

| Proje | Yıldız ve Durum | Açıklama | Etiketler |
| :--- | :---: | :--- | :--- |
| **[DelphiAST](https://github.com/RomanYankovsky/DelphiAST)** | [![Stars](https://img.shields.io/github/stars/RomanYankovsky/DelphiAST?style=flat-square)](https://github.com/RomanYankovsky/DelphiAST/stargazers)<br>[![Last Commit](https://img.shields.io/github/last-commit/RomanYankovsky/DelphiAST?style=flat-square)](https://github.com/RomanYankovsky/DelphiAST/commits) | Delphi kaynak kodu için tam donanımlı Soyut Sözdizimi Ağacı (AST) üreticisi. Özel kod refactoring, semantik analiz ve LLM bağlam çıkarımı için temel yapı taşıdır. | `AST` `Parsing` `Static Analysis` `Delphi` |
| **[StaticCodeAnalyser](https://github.com/nrodear/StaticCodeAnalyser)** | [![Stars](https://img.shields.io/github/stars/nrodear/StaticCodeAnalyser?style=flat-square)](https://github.com/nrodear/StaticCodeAnalyser/stargazers)<br>[![Last Commit](https://img.shields.io/github/last-commit/nrodear/StaticCodeAnalyser?style=flat-square)](https://github.com/nrodear/StaticCodeAnalyser/commits) | 200 den fazla AST ve DFM kuralına sahip Delphi ve Free Pascal statik analiz motoru. Otomatik yapay zekâ incelemesi ve CI/CD kalite kapıları için SARIF raporları üretir. | `AST` `SARIF` `Delphi 12` `Lazarus` `Static Analysis` |
| **[Markdown4D](https://github.com/GDKsoftware/Markdown4D)** | [![Stars](https://img.shields.io/github/stars/GDKsoftware/Markdown4D?style=flat-square)](https://github.com/GDKsoftware/Markdown4D/stargazers)<br>[![Last Commit](https://img.shields.io/github/last-commit/GDKsoftware/Markdown4D?style=flat-square)](https://github.com/GDKsoftware/Markdown4D/commits) | Açık AST ve akışlı ayrıştırma mimarisine sahip yüksek hızlı CommonMark/GFM ayrıştırıcı. VCL ve FMX arayüzlerinde LLM akış yanıtlarını görselleştirmek için elzemdir. | `AST` `Markdown` `VCL` `FMX` `Streaming` |
| **[Neslib.Clang](https://github.com/neslib/Neslib.Clang)** | [![Stars](https://img.shields.io/github/stars/neslib/Neslib.Clang?style=flat-square)](https://github.com/neslib/Neslib.Clang/stargazers)<br>[![Last Commit](https://img.shields.io/github/last-commit/neslib/Neslib.Clang?style=flat-square)](https://github.com/neslib/Neslib.Clang/commits) | libclang için Delphi kütüphanesi. C/C++ başlıklarının AST analizini yaparak otomatik Delphi sarmalayıcı (wrapper) ve bağlayıcı kod üretimini sağlar. | `AST` `libclang` `Delphi 12` |

---

## Eski Kod Tabanları ve Karakter Kodlama Köprüleri

*Yapay zekâ ajanları eski (legacy) Delphi projelerini düzenlerken karakter seti bozulmalarını, satır sonu (CRLF) uyumsuzluklarını ve çalışma alanı sürtünmelerini önleyen araçlar.*

🔍 **Canlı GitHub Aramaları:** [`delphi legacy utf8`](https://github.com/search?q=delphi+legacy+utf8&type=repositories&s=updated&o=desc) · [`delphi encoding bom`](https://github.com/search?q=delphi+encoding+bom&type=repositories&s=updated&o=desc)

| Proje | Yıldız ve Durum | Açıklama | Etiketler |
| :--- | :---: | :--- | :--- |
| **[mcp-file-tools](https://github.com/dimitar-grigorov/mcp-file-tools)** | [![Stars](https://img.shields.io/github/stars/dimitar-grigorov/mcp-file-tools?style=flat-square)](https://github.com/dimitar-grigorov/mcp-file-tools/stargazers)<br>[![Last Commit](https://img.shields.io/github/last-commit/dimitar-grigorov/mcp-file-tools?style=flat-square)](https://github.com/dimitar-grigorov/mcp-file-tools/commits) | Delphi 7 den Delphi 2007 ye kadar olan eski projeler düzenlenirken ANSI, Windows-1252 ve UTF-8 BOM kodlamalarını güvenle yönetip CRLF satır sonlarını koruyarak karakter seti bozulmalarını şeffaf biçimde engeller. | `Legacy Migration` `Delphi 7` `Delphi 2007` `UTF-8 BOM` `MCP` |

---

## IDE Eklentileri ve Editör İçi Asistanlar

*RAD Studio içine ToolsAPI aracılığıyla doğrudan entegre edilen yapay zekâ sohbeti, kod tamamlama ve satır içi refactoring eklentileri.*

🔍 **Canlı GitHub Aramaları:** [`delphi copilot`](https://github.com/search?q=delphi+copilot&type=repositories&s=updated&o=desc) · [`delphi ide plugin ai`](https://github.com/search?q=delphi+ide+plugin+ai&type=repositories&s=updated&o=desc) · [`rad studio ai`](https://github.com/search?q=rad+studio+ai&type=repositories&s=updated&o=desc)

| Proje | Yıldız ve Durum | Açıklama | Etiketler |
| :--- | :---: | :--- | :--- |
| **[FusionAI](https://github.com/AliDehbansiahkarbon/FusionAI)** | [![Stars](https://img.shields.io/github/stars/AliDehbansiahkarbon/FusionAI?style=flat-square)](https://github.com/AliDehbansiahkarbon/FusionAI/stargazers)<br>[![Last Commit](https://img.shields.io/github/last-commit/AliDehbansiahkarbon/FusionAI?style=flat-square)](https://github.com/AliDehbansiahkarbon/FusionAI/commits) | OpenAI, Anthropic Claude, Google Gemini ve yerel Ollama modellerini destekleyen kapsamlı RAD Studio eklentisi. Delphi XE5 ile 12 arasında editör içi sohbet ve kod üretimi sunar. | `RAD Studio` `ToolsAPI` `Multi-Provider` `Delphi 12` |
| **[Delphi AI Developer](https://github.com/Code4Delphi/Delphi-AI-Developer)** | [![Stars](https://img.shields.io/github/stars/Code4Delphi/Delphi-AI-Developer?style=flat-square)](https://github.com/Code4Delphi/Delphi-AI-Developer/stargazers)<br>[![Last Commit](https://img.shields.io/github/last-commit/Code4Delphi/Delphi-AI-Developer?style=flat-square)](https://github.com/Code4Delphi/Delphi-AI-Developer/commits) | IDE içinde çoklu sağlayıcı destekli yapay zekâ sohbeti, kod tamamlama ve refactoring imkanı veren açık kaynaklı RAD Studio eklentisi. | `IDE Plugin` `ToolsAPI` `Multi-Provider` |
| **[RadIA-Plugin](https://github.com/regyssilveira/RadIA-Plugin)** | [![Stars](https://img.shields.io/github/stars/regyssilveira/RadIA-Plugin?style=flat-square)](https://github.com/regyssilveira/RadIA-Plugin/stargazers)<br>[![Last Commit](https://img.shields.io/github/last-commit/regyssilveira/RadIA-Plugin?style=flat-square)](https://github.com/regyssilveira/RadIA-Plugin/commits) | Open Tools API ve WebView2 kullanarak Server-Sent Events (SSE) ile bağlamsal kod düzenleme ve yapay zekâ asistanlığı sunan RAD Studio eklentisi. | `OTA` `WebView2` `Delphi IDE` `SSE` |
| **[RAD Studio Smart CodeInsight — Claude Patch](https://blogs.embarcadero.com/rad-studio-13-smart-codeinsight-claude-patch-released/)** | `Resmi` | Smart CodeInsight içerisine doğrudan Claude tabanlı kod tamamlama yeteneği kazandıran resmi Embarcadero yaması. | `RAD Studio 13` `GetIt` `Resmi` |

---

## Yapay Zekâ Çatıları ve Çoklu Ajan Orkestrasyonu

*Otonom ajan iş akışları, RAG boru hatları ve kurumsal LLM uygulamaları geliştirmek için yerel Delphi mimarileri.*

🔍 **Canlı GitHub Aramaları:** [`delphi agent`](https://github.com/search?q=delphi+agent&type=repositories&s=updated&o=desc) · [`pascal rag`](https://github.com/search?q=pascal+rag&type=repositories&s=updated&o=desc) · [`delphi vector`](https://github.com/search?q=delphi+vector&type=repositories&s=updated&o=desc)

| Proje | Yıldız ve Durum | Açıklama | Etiketler |
| :--- | :---: | :--- | :--- |
| **[MakerAI](https://github.com/gustavoeenriquez/MakerAi)** | [![Stars](https://img.shields.io/github/stars/gustavoeenriquez/MakerAi?style=flat-square)](https://github.com/gustavoeenriquez/MakerAi/stargazers)<br>[![Last Commit](https://img.shields.io/github/last-commit/gustavoeenriquez/MakerAi?style=flat-square)](https://github.com/gustavoeenriquez/MakerAi/commits) | Yapay zekâ destekli Delphi uygulamaları geliştirmek için gömülü çatı. Vektör RAG (HNSW + BM25), Graph RAG, çok düğümlü otonom ajan iş parçacığı havuzu ve MCP desteği sunar. | `RAG` `Agents` `Vector DB` `FPC` |
| **[PasClaw](https://github.com/FMXExpress/PasClaw)** | [![Stars](https://img.shields.io/github/stars/FMXExpress/PasClaw?style=flat-square)](https://github.com/FMXExpress/PasClaw/stargazers)<br>[![Last Commit](https://img.shields.io/github/last-commit/FMXExpress/PasClaw?style=flat-square)](https://github.com/FMXExpress/PasClaw/commits) | Araç çağırma (tool calling) ve görev orkestrasyonu özelliklerine sahip, Delphi ve FreePascal uyumlu hafif otonom yapay zekâ ajanı kütüphanesi. | `Agents` `Tool Calling` `FMX` `VCL` `Lazarus` |
| **[SmartCore AI Components Pack](https://blogs.embarcadero.com/introducing-the-smartcore-ai-components-pack/)** | `Resmi` | Sağlayıcı bağımsız bağlantı bileşenleri (OpenAI, Claude, Gemini, Ollama), yapılandırılmış JSON işleme ve doğrudan UI veri bağlama sunan resmi Embarcadero bileşen paketi. | `RAD Studio 13` `GetIt` `Resmi` |

---

## Cihaz Üzerinde Yerel Çıkarım (Delphi-Native Inference)

*Bulut bağımlılığı, harici API anahtarı veya Python ortamı gerektirmeden doğrudan cihaz üzerinde yerel LLM, SLM ve sinir ağı çalıştıran motorlar.*

🔍 **Canlı GitHub Aramaları:** [`delphi llama`](https://github.com/search?q=delphi+llama&type=repositories&s=updated&o=desc) · [`pascal onnx`](https://github.com/search?q=pascal+onnx&type=repositories&s=updated&o=desc) · [`delphi gguf`](https://github.com/search?q=delphi+gguf&type=repositories&s=updated&o=desc)

| Proje | Yıldız ve Durum | Açıklama | Etiketler |
| :--- | :---: | :--- | :--- |
| **[VindexLLM](https://github.com/tinyBigGAMES/VindexLLM)** | [![Stars](https://img.shields.io/github/stars/tinyBigGAMES/VindexLLM?style=flat-square)](https://github.com/tinyBigGAMES/VindexLLM/stargazers)<br>[![Last Commit](https://img.shields.io/github/last-commit/tinyBigGAMES/VindexLLM?style=flat-square)](https://github.com/tinyBigGAMES/VindexLLM/commits) | GGUF transformer modellerini Vulkan hesaplama gölgelendiricileriyle çalıştıran yerel Delphi GPU çıkarım motoru. Sıfır harici bağımlılık (Python veya CUDA yok), yalnızca `vulkan-1.dll` gerektirir. | `Local Inference` `GGUF` `Vulkan GPU` `Zero-Dependency` |
| **[LlamaKit](https://github.com/gustavoeenriquez/LlamaKit)** | [![Stars](https://img.shields.io/github/stars/gustavoeenriquez/LlamaKit?style=flat-square)](https://github.com/gustavoeenriquez/LlamaKit/stargazers)<br>[![Last Commit](https://img.shields.io/github/last-commit/gustavoeenriquez/LlamaKit?style=flat-square)](https://github.com/gustavoeenriquez/LlamaKit/commits) | Derlenmiş Windows DLL leri ve yerel Delphi sarmalayıcı bileşenleriyle llama.cpp GGUF modellerini yerel olarak çalıştıran kütüphane. | `llama.cpp` `GGUF` `Local` |
| **[llama-cpp-delphi](https://github.com/Embarcadero/llama-cpp-delphi)** | [![Stars](https://img.shields.io/github/stars/Embarcadero/llama-cpp-delphi?style=flat-square)](https://github.com/Embarcadero/llama-cpp-delphi/stargazers)<br>[![Last Commit](https://img.shields.io/github/last-commit/Embarcadero/llama-cpp-delphi?style=flat-square)](https://github.com/Embarcadero/llama-cpp-delphi/commits) | Yerel GGUF modellerini çalıştırmak için resmi Embarcadero llama.cpp sarmalayıcısı. | `llama.cpp` `Embarcadero` `Resmi` |
| **[Dllama](https://github.com/tinyBigGAMES/Dllama)** | [![Stars](https://img.shields.io/github/stars/tinyBigGAMES/Dllama?style=flat-square)](https://github.com/tinyBigGAMES/Dllama/stargazers)<br>[![Last Commit](https://img.shields.io/github/last-commit/tinyBigGAMES/Dllama?style=flat-square)](https://github.com/tinyBigGAMES/Dllama/commits) | Ollama uyumlu GGUF modellerini (Llama, Mistral, Gemma) destekleyen hafif Delphi llama.cpp bağlayıcısı. | `llama.cpp` `GGUF` |
| **[TONNXRuntime](https://github.com/hshatti/TONNXRuntime)** | [![Stars](https://img.shields.io/github/stars/hshatti/TONNXRuntime?style=flat-square)](https://github.com/hshatti/TONNXRuntime/stargazers)<br>[![Last Commit](https://img.shields.io/github/last-commit/hshatti/TONNXRuntime?style=flat-square)](https://github.com/hshatti/TONNXRuntime/commits) | Masaüstü ve uç cihazlarda önceden eğitilmiş yapay sinir ağlarını çalıştırmak için FreePascal ve Delphi Microsoft ONNX Runtime bağlayıcısı. | `ONNX` `Lazarus` `Delphi` |
| **[Ollama-Delphi-GUI](https://github.com/HuichanKIM/Ollama-Delphi-GUI)** | [![Stars](https://img.shields.io/github/stars/HuichanKIM/Ollama-Delphi-GUI?style=flat-square)](https://github.com/HuichanKIM/Ollama-Delphi-GUI/stargazers)<br>[![Last Commit](https://img.shields.io/github/last-commit/HuichanKIM/Ollama-Delphi-GUI?style=flat-square)](https://github.com/HuichanKIM/Ollama-Delphi-GUI/commits) | Ollama REST API si üzerinden gerçek zamanlı yerel model akışı ve sohbet arayüzü kalıplarını gösteren Delphi masaüstü istemcisi. | `Ollama` `VCL` `Desktop UI` |

---

## Bulut LLM API İstemcileri

*Büyük yapay zekâ sağlayıcılarının API lerini doğrudan Object Pascal içinden çağırmak için aktif olarak korunan Delphi SDK ları.*

🔍 **Canlı GitHub Aramaları:** [`delphi openai`](https://github.com/search?q=delphi+openai&type=repositories&s=updated&o=desc) · [`delphi anthropic`](https://github.com/search?q=delphi+anthropic&type=repositories&s=updated&o=desc) · [`delphi gemini`](https://github.com/search?q=delphi+gemini&type=repositories&s=updated&o=desc) · [`delphi deepseek`](https://github.com/search?q=delphi+deepseek&type=repositories&s=updated&o=desc)

| Proje | Yıldız ve Durum | Açıklama | Etiketler |
| :--- | :---: | :--- | :--- |
| **[DelphiAnthropic](https://github.com/MaxiDonkey/DelphiAnthropic)** | [![Stars](https://img.shields.io/github/stars/MaxiDonkey/DelphiAnthropic?style=flat-square)](https://github.com/MaxiDonkey/DelphiAnthropic/stargazers)<br>[![Last Commit](https://img.shields.io/github/last-commit/MaxiDonkey/DelphiAnthropic?style=flat-square)](https://github.com/MaxiDonkey/DelphiAnthropic/commits) | Claude 3.5 & 3.7, görüntü işleme, prompt önbellekleme (prompt caching), araç kullanımı ve akış desteği sunan eksiksiz Anthropic SDK sı. | `Anthropic` `Claude 3.7` `Prompt Caching` |
| **[DelphiOpenAI](https://github.com/HemulGM/DelphiOpenAI)** | [![Stars](https://img.shields.io/github/stars/HemulGM/DelphiOpenAI?style=flat-square)](https://github.com/HemulGM/DelphiOpenAI/stargazers)<br>[![Last Commit](https://img.shields.io/github/last-commit/HemulGM/DelphiOpenAI?style=flat-square)](https://github.com/HemulGM/DelphiOpenAI/commits) | Tam donanımlı OpenAI istemcisi (ChatGPT, Whisper, DALL-E, embeddings, function calling). Azure, DeepSeek ve Ollama ya da bağlanabilir. | `OpenAI` `GPT-4o` `Function Calling` |
| **[DelphiGenAI](https://github.com/MaxiDonkey/DelphiGenAI)** | [![Stars](https://img.shields.io/github/stars/MaxiDonkey/DelphiGenAI?style=flat-square)](https://github.com/MaxiDonkey/DelphiGenAI/stargazers)<br>[![Last Commit](https://img.shields.io/github/last-commit/MaxiDonkey/DelphiGenAI?style=flat-square)](https://github.com/MaxiDonkey/DelphiGenAI/commits) | GPT-4o, görüntü, ses, embedding ve ajan iş akışlarını destekleyen OpenAI kütüphanesi. | `OpenAI` `Multimodal` `Embeddings` |
| **[openai-delphi](https://github.com/landgraf-dev/openai-delphi)** | [![Stars](https://img.shields.io/github/stars/landgraf-dev/openai-delphi?style=flat-square)](https://github.com/landgraf-dev/openai-delphi/stargazers)<br>[![Last Commit](https://img.shields.io/github/last-commit/landgraf-dev/openai-delphi?style=flat-square)](https://github.com/landgraf-dev/openai-delphi/commits) | Tam FreePascal ve Lazarus uyumluluğuna sahip temiz ve hafif OpenAI istemcisi. | `OpenAI` `Lazarus` `FPC` |
| **[DelphiGemini](https://github.com/MaxiDonkey/DelphiGemini)** | [![Stars](https://img.shields.io/github/stars/MaxiDonkey/DelphiGemini?style=flat-square)](https://github.com/MaxiDonkey/DelphiGemini/stargazers)<br>[![Last Commit](https://img.shields.io/github/last-commit/MaxiDonkey/DelphiGemini?style=flat-square)](https://github.com/MaxiDonkey/DelphiGemini/commits) | Çok modlu promptlar, kod üretimi, önbellekleme ve ince ayar (fine-tuning) destekleyen Google Gemini SDK sı. | `Google Gemini` `Multimodal` `Caching` |
| **[Gemini4Delphi](https://github.com/delmardelima/Gemini4Delphi)** | [![Stars](https://img.shields.io/github/stars/delmardelima/Gemini4Delphi?style=flat-square)](https://github.com/delmardelima/Gemini4Delphi/stargazers)<br>[![Last Commit](https://img.shields.io/github/last-commit/delmardelima/Gemini4Delphi?style=flat-square)](https://github.com/delmardelima/Gemini4Delphi/commits) | Delphi için hafif Google Gemini köprüsü. | `Google Gemini` `Delphi` |
| **[DelphiDeepseek](https://github.com/MaxiDonkey/DelphiDeepseek)** | [![Stars](https://img.shields.io/github/stars/MaxiDonkey/DelphiDeepseek?style=flat-square)](https://github.com/MaxiDonkey/DelphiDeepseek/stargazers)<br>[![Last Commit](https://img.shields.io/github/last-commit/MaxiDonkey/DelphiDeepseek?style=flat-square)](https://github.com/MaxiDonkey/DelphiDeepseek/commits) | Yerel LM Studio uyumluluğuna sahip DeepSeek akıl yürütme (reasoning) modeli kütüphanesi. | `DeepSeek` `Reasoning` `LM Studio` |
| **[DelphiGroqCloud](https://github.com/MaxiDonkey/DelphiGroqCloud)** | [![Stars](https://img.shields.io/github/stars/MaxiDonkey/DelphiGroqCloud?style=flat-square)](https://github.com/MaxiDonkey/DelphiGroqCloud/stargazers)<br>[![Last Commit](https://img.shields.io/github/last-commit/MaxiDonkey/DelphiGroqCloud?style=flat-square)](https://github.com/MaxiDonkey/DelphiGroqCloud/commits) | Ultra düşük gecikmeli model çıkarımı için Groq LPU bulut API bağlayıcısı. | `Groq` `Fast Inference` `LPU` |
| **[DelphiMistralAI](https://github.com/MaxiDonkey/DelphiMistralAI)** | [![Stars](https://img.shields.io/github/stars/MaxiDonkey/DelphiMistralAI?style=flat-square)](https://github.com/MaxiDonkey/DelphiMistralAI/stargazers)<br>[![Last Commit](https://img.shields.io/github/last-commit/MaxiDonkey/DelphiMistralAI?style=flat-square)](https://github.com/MaxiDonkey/DelphiMistralAI/commits) | Codestral, görüntü işleme, embedding ve ajan sohbetlerini kapsayan Mistral SDK sı. | `Mistral` `Codestral` `Embeddings` |

---

## Test ve GUI Otomasyonu

*Delphi uygulamalarının davranışlarını doğrulamak için yapay zekâ odaklı ve otomatik test araçları.*

🔍 **Canlı GitHub Aramaları:** [`delphi test automation`](https://github.com/search?q=delphi+test+automation&type=repositories&s=updated&o=desc) · [`claude code delphi`](https://github.com/search?q=claude+code+delphi&type=repositories&s=updated&o=desc)

| Proje | Yıldız ve Durum | Açıklama | Etiketler |
| :--- | :---: | :--- | :--- |
| **[Autopilot for Delphi](https://github.com/GabrielOnDelphi/Autopilot-for-Delphi)** | [![Stars](https://img.shields.io/github/stars/GabrielOnDelphi/Autopilot-for-Delphi?style=flat-square)](https://github.com/GabrielOnDelphi/Autopilot-for-Delphi/stargazers)<br>[![Last Commit](https://img.shields.io/github/last-commit/GabrielOnDelphi/Autopilot-for-Delphi?style=flat-square)](https://github.com/GabrielOnDelphi/Autopilot-for-Delphi/commits) | MCP veya DUnitX aracılığıyla çalışan VCL/FMX formlarını yönetir: fiziksel fareyi oynatmadan bileşenlere tıklar, etiketleri doğrular, pencereleri kapatır ve ekranları test eder. | `VCL` `FMX` `GUI Automation` `DUnitX` |
| **[ClaudeCode TokenVampire](https://github.com/GabrielOnDelphi/ClaudeCode_TokenVampire)** | [![Stars](https://img.shields.io/github/stars/GabrielOnDelphi/ClaudeCode_TokenVampire?style=flat-square)](https://github.com/GabrielOnDelphi/ClaudeCode_TokenVampire/stargazers)<br>[![Last Commit](https://img.shields.io/github/last-commit/GabrielOnDelphi/ClaudeCode_TokenVampire?style=flat-square)](https://github.com/GabrielOnDelphi/ClaudeCode_TokenVampire/commits) | Claude Code oturumları için gerçek zamanlı token kullanım monitörü. Çevrimdışı log analiziyle kotaları, önbellek isabet oranlarını ve maliyet tahminlerini gösterir. | `Claude Code` `DevEx` `Token Optimization` |

---

## Derlenmiş Listeler ve Topluluk Dizinleri

*Delphi ekosistemindeki diğer meta-kataloglar ve rehberler.*

🔍 **Canlı GitHub Aramaları:** [`awesome delphi`](https://github.com/search?q=awesome+delphi&type=repositories&s=updated&o=desc) · [`awesome pascal`](https://github.com/search?q=awesome+pascal&type=repositories&s=updated&o=desc)

| Proje | Yıldız ve Durum | Açıklama | Etiketler |
| :--- | :---: | :--- | :--- |
| **[Awesome-AI-For-Delphi](https://github.com/GabrielOnDelphi/Awesome-AI-For-Delphi)** | [![Stars](https://img.shields.io/github/stars/GabrielOnDelphi/Awesome-AI-For-Delphi?style=flat-square)](https://github.com/GabrielOnDelphi/Awesome-AI-For-Delphi/stargazers)<br>[![Last Commit](https://img.shields.io/github/last-commit/GabrielOnDelphi/Awesome-AI-For-Delphi?style=flat-square)](https://github.com/GabrielOnDelphi/Awesome-AI-For-Delphi/commits) | Delphi topluluğunda yapay zekâ farkındalığını ilk başlatan öncü kürasyon dizini. Bu projenin modernize edilmiş, MCP/LSP odaklı ve otomatik keşif sürümü için temel ilham kaynağı olmuştur. | `Curated List` `Community Pioneer` `Delphi AI` |
| **[Awesome Delphi](https://github.com/PassKit/Awesome-Delphi)** | [![Stars](https://img.shields.io/github/stars/PassKit/Awesome-Delphi?style=flat-square)](https://github.com/PassKit/Awesome-Delphi/stargazers)<br>[![Last Commit](https://img.shields.io/github/last-commit/PassKit/Awesome-Delphi?style=flat-square)](https://github.com/PassKit/Awesome-Delphi/commits) | Açık kaynaklı Delphi kütüphaneleri, çatıları, bileşenleri ve araçlarının klasik ve kapsamlı dizini. | `Awesome List` `Delphi` `General Catalog` |

---

## Topluluk ve Kaynaklar

### Küresel Topluluklar
* **[Delphi-PRAXiS (İngilizce)](https://en.delphipraxis.net/)** & **[Almanca Sürüm](https://www.delphipraxis.net/)**  
  Dünyanın en büyük bağımsız Delphi forumu; [AI-Assisted Coding](https://en.delphipraxis.net/forum/43-ai-assisted-coding/) özel bölümü, LLM entegrasyonu ve modern Pascal tartışmaları.
* **[Embarcadero Topluluk ve Geliştirici Blogları](https://blogs.embarcadero.com/)**  
  Resmi geliştirici blogları, sürüm güncellemeleri, SmartCore AI haberleri ve Embarcadero mimarlarından teknik makaleler.
* **[Reddit r/delphi](https://www.reddit.com/r/delphi/)**  
  Delphi ve Object Pascal haberleri, araçları ve açık kaynak proje tanıtımları için aktif topluluk alt dizini.
* **[Claude Code Training for Delphi Developers](https://training.gdksoftware.com/)**  
  GDK Software tarafından sunulan; CLAUDE.md mimarisi, MCP kurulumları ve Delphi ajan iş akışlarını kapsayan özel eğitim. `[Ticari]`

### Türkiye Toplulukları
* **[DelphiCan](https://www.delphican.com/)**  
  Türkiye nin en aktif ve kapsamlı Delphi & Object Pascal geliştirici topluluğu; VCL, FMX, modern mimariler, API ve yapay zekâ tartışmaları.
* **[Delphi Türkiye Forum](https://www.delphiturkiye.com/forum/)**  
  1998 den beri Türkiye Delphi ekosisteminin en köklü bilgi bankası ve teknik tartışma forumu (`delphiturkiye.com`).

---

## Katkıda Bulunma (Contributing)

Katkılarınız ve proje önerileriniz memnuniyetle karşılanır!
1. **Odak:** Eklenen proje; yapay zekâ, MCP, LSP, AST analizi veya modern geliştirici araçlarıyla Delphi/Object Pascal geliştirmesini güçlendirmelidir.
2. **Kalite ve Dağıtım:** Açık kaynaklı ve aktif olarak güncellenen depolar önceliklidir. Ticari veya kapalı kaynak dağıtım araçları özel bir değer sunmalı ve açıkça `[Ticari]` olarak etiketlenmelidir.
3. **Format:** Belirlenen kategori kurallarına, 4 sütunlu tablo yapısına ve etiketleme standartlarına uyarak bir Pull Request gönderin.

---

## Güvenlik Uyarısı ve Sorumluluk Reddi (Disclaimer)

> ⚠️ **Önemli Güvenlik Bildirimi ve Geliştirici Sorumluluğu**
>
> 1. **Yalnızca Dizin ve Katalogdur:** Bu depo, otomatik ve topluluk tarafından derlenmiş bir açık kaynak kataloğudur. Bir projenin bu listede yer alması; güvenlik doğrulaması, kod denetimi veya resmi bir onay anlamına **gelmez**.
> 2. **Derlenmemiş ve Denetlenmemiş Üçüncü Taraf Kodlar:** Bu listenin yöneticileri, burada bağlantısı verilen tüm üçüncü taraf depoları, ikili dosyaları (`.dll`, `.bpl`), betikleri veya kütüphaneleri bizzat derlememiş, denetlememiş ve çalıştırmamıştır.
> 3. **Geliştiricinin Kendi İnceleme Yükümlülüğü:** Herhangi bir üçüncü taraf kodu, derlenmiş kütüphaneyi veya MCP sunucusunu yerel geliştirme ortamınıza, şirket ağınıza veya canlı üretim sistemlerinize entegre etmeden önce kaynak kod incelemesi, bağımlılık taraması ve güvenlik denetimi yapmak **tamamen sizin sorumluluğunuzdadır**.
> 4. **Garanti Verilmez:** Tüm bağlantılar ve kaynaklar hiçbir garanti (açık veya zımni) olmaksızın, tamamen *"olduğu gibi"* sağlanmaktadır. Bağlantılı yazılımların kullanımından kaynaklanabilecek herhangi bir veri kaybı, güvenlik açığı, sistem arızası veya zarardan depo yöneticileri hiçbir koşulda sorumlu tutulamaz.
