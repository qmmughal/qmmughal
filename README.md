# Hi, I'm Qaiser Mehmood

### Architect of AI-Native & Enterprise Software

**Building AI agents, LLM infrastructure, and scalable .NET systems**  
*Open-source when it helps the community; honest about maturity*

[![GitHub followers](https://img.shields.io/github/followers/qmmughal?style=for-the-badge&logo=github&color=0d1117)](https://github.com/qmmughal?tab=followers)
[![Website](https://img.shields.io/badge/Website-qaisermehmood.info-0A66C2?style=for-the-badge)](http://www.qaisermehmood.info)

---

### Tech Stack

![C#](https://img.shields.io/badge/C%23-239120?style=for-the-badge&logo=c-sharp&logoColor=white)
![.NET](https://img.shields.io/badge/.NET-512BD4?style=for-the-badge&logo=dotnet&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-007ACC?style=for-the-badge&logo=typescript&logoColor=white)
![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Next.js](https://img.shields.io/badge/Next.js-000000?style=for-the-badge&logo=nextdotjs&logoColor=white)
![Blazor](https://img.shields.io/badge/Blazor-512BD4?style=for-the-badge&logo=blazor&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=for-the-badge&logo=postgresql&logoColor=white)
![Redis](https://img.shields.io/badge/Redis-FF4438?style=for-the-badge&logo=redis&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white)
![T-SQL](https://img.shields.io/badge/T--SQL-CC2927?style=for-the-badge&logo=microsoftsqlserver&logoColor=white)
![PowerShell](https://img.shields.io/badge/PowerShell-5391FE?style=for-the-badge&logo=powershell&logoColor=white)

---

## Featured projects

### AI & agents

#### [UpgradePilot](https://github.com/qmmughal/upgradepilot-core) — *AI-powered .NET framework upgrade pipeline*
> 20-agent pipeline that upgrades ASP.NET Zero / ABP Framework / .NET apps without silently overwriting customizations

**Status: 19/20 agents implemented, 112 tests passing.** Every agent is real, not an LLM-prompt wrapper: actual `dotnet build`/`dotnet test`/`dotnet ef` invocations, real `git`/`gh` operations, real Roslyn AST diff/merge, real NuGet vulnerability scans. Open-core — this repo is Apache-2.0; the hosted multi-tenant product is closed-source.

| Pain | Direction |
| --- | --- |
| Manual framework upgrades take weeks and risk breaking custom code | Roslyn-based semantic three-way merge: auto-propagates safe template changes, flags everything else as an explicit conflict |
| AI code tools that rewrite everything and hope | Every agent returns a confidence score and citations — nothing overwrites without evidence |
| No visibility into what an upgrade actually changed | Real build/test/security validation, then a generated PR with the full upgrade report |

[Website](https://upgradepilot.ai/) · [Source](https://github.com/qmmughal/upgradepilot-core)

`C#` `.NET 10` `Roslyn` `MCP` `ASP.NET Zero` `ABP Framework` `#ai-agents` `#framework-upgrade`

---

#### [AgentWire](https://github.com/qmmughal/AgentWire) — *AI observability gateway (Alpha)*
> OpenTelemetry-inspired monitoring for agents, LLMs, and MCP traffic

**Status: Alpha / MVP.** Local ingest + cost endpoints run today; gateway security/replay are on the roadmap.

| Pain | Direction |
|---|---|
| Unattributed LLM spend | Cost rollups by model / packet |
| Opaque agent traces | Trace ingest + packet inspection API |
| Hard to secure agent traffic | Planned security scanner & guardrails |

`C#` `.NET 10` `ASP.NET Core` `Next.js` `#ai-observability` `#mcp`

---

#### [routellm](https://github.com/qmmughal/routellm) — *Smart LLM Router & Fallback Proxy*
> Sub-15ms local classifier & cost-optimizing fallback proxy compatible with OpenAI API

Evaluates prompt complexity locally, routes simple queries to SLMs (Ollama/gpt-4o-mini), and automatically escalates complex tasks or errors to Tier-1 models (GPT-4o/Claude 3.5). Reduces API spend by up to 80%.

`Python` `FastAPI` `OpenAI` `Ollama` `#llm-router` `#fallback-proxy`

---

#### [langchain-supabase-ingestor](https://github.com/qmmughal/langchain-supabase-ingestor) — *Privacy-first RAG ingestion*
> REST → LangChain + local Ollama → Supabase Realtime alerts

Production-oriented pipeline with migrations, docker-compose, and a Next.js dashboard.

`Python` `LangChain` `Supabase` `Ollama` `pgvector` `Next.js`

---

#### [dotnet-agent-framework](https://github.com/qmmughal/dotnet-agent-framework) — *Multi-agent orchestration for .NET*
> Lightweight agents, tools, and sequential workflows in idiomatic C#

`C#` `.NET` `RAG` `LLM` `#semantic-kernel`

---

#### [mcp-server-template](https://github.com/qmmughal/mcp-server-template) — *Enterprise MCP server starter*
> TypeScript template with Zod, Vitest, esbuild, and Pino

`TypeScript` `MCP` `Node.js`

---

### Claude Code skills (Blazor)

#### [aspnetzero-blazor-telerik.skill](https://github.com/qmmughal/aspnetzero-blazor-telerik.skill) — *ANZ / ABP + Telerik Blazor*
> Agent skill for grafting Blazor + Telerik into ASP.NET Zero (circuit DI, UoW, Metronic seams)

#### [blazor-crud-standards.skill](https://github.com/qmmughal/blazor-crud-standards.skill) — *Blazor CRUD standards*
> Scaffold/review CRUD against Microsoft Blazor patterns (any hosting model)

---

### Enterprise .NET

#### [enterprise-starter-kit-v2](https://github.com/qmmughal/enterprise-starter-kit-v2) — *.NET 10 starter (preferred)*
> Clean Architecture + CQRS + MediatR + Outbox + ABP patterns + Docker

#### [enterprise-starter-kit](https://github.com/qmmughal/enterprise-starter-kit) — *.NET 8 LTS track*
> Same patterns on .NET 8 for teams staying on LTS

---

### Database & DBA tools

#### [sql-recyclebin](https://github.com/qmmughal/sql-recyclebin) — *A recycle bin for SQL Server*
> Undo an accidental `DELETE`/`UPDATE` with one command — no restore, no downtime

Trigger-based capture with rows stored as JSON, so schema changes never break the safety net. Runs on every SQL Server edition since 2017, including Express. Source-available (PolyForm Noncommercial) with a commercial tier for production use. Also available as a PowerShell module — `Install-Module SqlRecycleBin` gives you 13 cmdlets (`Install-SqlRecycleBin`, `Restore-SqlRecycleBinLast`, etc.) instead of raw T-SQL.

[Live site & pricing](https://sqlrecyclebin.com) · [Demo & docs](https://github.com/qmmughal/sql-recyclebin) · [PowerShell Gallery](https://www.powershellgallery.com/packages/SqlRecycleBin)

`T-SQL` `SQL Server` `PowerShell` `#disaster-recovery` `#dba-tools`

---

### Blazor libraries & demos

#### [ckeditor5-blazor](https://github.com/qmmughal/ckeditor5-blazor) — *CKEditor 5 for Blazor*
> Working CKEditor 5 + custom upload adapter for Blazor Server/WASM — **community reference; maintenance welcome**

`Blazor` `CKEditor5` `JavaScript`

#### Also: [blazor-pdf-generator](https://github.com/qmmughal/blazor-pdf-generator) · [filestack-blazor](https://github.com/qmmughal/filestack-blazor) · [blazor-into-asp-net-core](https://github.com/qmmughal/blazor-into-asp-net-core)

---

### Automation & tools

#### [media-qa-bot](https://github.com/qmmughal/media-qa-bot) — *Ads campaign reconciliation*
> Asana (source of truth) vs Google Ads / Meta — catch budget & date setup errors

#### [wifi-monitor](https://github.com/qmmughal/wifi-monitor) — *Local WiFi dashboard + CLI*
> Browser dashboard + Python CLI; uses available Web APIs and documents simulation limits

#### [car-maintenance](https://github.com/qmmughal/car-maintenance) — *.NET MAUI reference app*
> Oil-change tracking on iOS/Android

---

### GitHub Stats

<a href="https://github.com/qmmughal">
  <img height="165" src="https://github-readme-stats-anuraghazra1.vercel.app/api?username=qmmughal&show_icons=true&theme=tokyonight&hide_border=true&include_all_commits=true&count_private=true&cache_seconds=86400" alt="Qaiser Mehmood GitHub Stats" />
</a>
<a href="https://github.com/qmmughal">
  <img height="165" src="https://github-readme-stats-anuraghazra1.vercel.app/api/top-langs/?username=qmmughal&layout=compact&theme=tokyonight&hide_border=true&cache_seconds=86400" alt="Qaiser Mehmood Top Languages" />
</a>

---

### Let's connect

> *"Build things that matter. Open source what you can. Label maturity honestly."*

**Open to contract work** in Blazor/.NET architecture and AI agent tooling — reach out via the site below.

What that looks like in practice: production ABP/Blazor enterprise architecture (see the starter kits above), paired with Claude Code skills that automate the exact review process this account itself went through — a sharper offer than generic ".NET developer available for hire."

See [shipped work in CASE-STUDIES.md](CASE-STUDIES.md) for working software, not just source.

[![GitHub](https://img.shields.io/badge/GitHub-qmmughal-181717?style=for-the-badge&logo=github)](https://github.com/qmmughal)
[![Website](https://img.shields.io/badge/Site-qaisermehmood.info-0A66C2?style=for-the-badge)](http://www.qaisermehmood.info)

*If a project helped you, a star helps others find it.*
