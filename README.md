# Awesome-Multi-Language-Translation-Localization

# Awesome Multi-Language Translation & Localization

> A curated list of top Multi-Language Translation and Localization platforms — both SaaS/Hosted commercial solutions and open-source alternatives for managing translation workflows, translation memory, and machine translation engines.
> 🌟 Star this repo if you find it useful! 🌟

---

## 📋 Table of Contents

- [SaaS / Hosted Platforms](#-saas--hosted-platforms)
  - [Crowdin](#crowdin)
  - [Lokalise](#lokalise)
  - [Phrase](#phrase)
  - [Transifex](#transifex)
  - [DeepL Pro](#deepl-pro)
- [Open-Source Software](#-open-source-software)
  - [Weblate](#weblate)
  - [Traduora](#traduora)
  - [Accent](#accent)
  - [Localess](#localess)
  - [Pontoon](#pontoon)
  - [LibreTranslate](#libretranslate)
  - [LTEngine](#ltengine)

---

## 🟦 SaaS / Hosted Platforms

Commercial, cloud-hosted Multi-Language Translation and Localization platforms. These are not open-source but are included as reference points for feature comparison.

### Crowdin
**Type:** Developer-friendly TMS with seamless GitHub integration
Crowdin is the most developer-friendly commercial TMS, with a genuinely seamless GitHub integration: push new strings to your repo, Crowdin detects them, translators work in the Crowdin interface, and approved translations come back as pull requests—the cycle takes minutes once set up . It offers a real free tier for open-source projects (unlimited strings and languages), broad machine translation engine support including custom engines, and over-the-air (OTA) delivery through mobile and web SDKs . **Trade-off:** The interface feels dated compared to Lokalise, project organization can get messy with many files and branches, and paid tiers (~$50/seat/month) add up quickly for larger teams .
**Best for:** Development teams and open-source projects wanting tight Git integration with a generous free tier, accepting a less polished UI than premium alternatives.

### Lokalise
**Type:** Premium TMS with best-in-class user experience
Lokalise has the best user experience of the major commercial TMS platforms, with a clean, fast, and intuitive interface that non-technical team members can navigate without training . Its standout features include **screenshot-based context** (upload app screenshots and visually map strings to their location), strong multi-step review workflows with role-based permissions, and a **Figma integration** that closes the gap between design and localization . **Trade-off:** Pricing is the highest among the four major platforms, starting at $120/month with usage-based scaling, and machine translation engine selection is more limited than Crowdin or Phrase .
**Best for:** Product teams and organizations where non-technical stakeholders need to participate in localization, accepting premium pricing for superior UX.

### Phrase
**Type:** Enterprise-grade TMS with broadest feature set
Phrase (formerly Memsource) is the most feature-complete commercial platform, especially for enterprise needs, with support for 30+ machine translation engines—the broadest selection among the major TMS platforms . It is positioned for large organizations with complex localization workflows, dedicated localization teams, and enterprise integration requirements. Pricing is custom-quoted.
**Best for:** Enterprises needing the deepest feature set and broadest MT engine coverage, accepting custom pricing and enterprise sales processes.

### Transifex
**Type:** Community-friendly TMS for open-source projects
Transifex offers a free tier for open-source projects and is positioned for community-driven translation workflows. It provides GitHub/GitLab integration, CLI tooling, translation memory, and a full REST API . It is a strong choice for open-source projects wanting a hosted platform without self-hosting overhead.
**Best for:** Open-source projects and community translation efforts wanting a hosted platform with a free tier for OSS.

### DeepL Pro
**Type:** Premium machine translation engine
DeepL Pro is a machine translation service (not a full TMS) known for translation quality that often exceeds Google Translate for European languages. It is commonly integrated into TMS platforms as a machine translation engine, and its API can be used directly for programmatic translation. It is positioned for teams prioritizing translation quality over full workflow management.
**Best for:** Teams needing high-quality machine translation as a component within a broader localization workflow, not as a standalone TMS.

---

## 🟩 Open-Source Software

Self-hosted, community-driven Multi-Language Translation and Localization tools. The open-source ecosystem spans **mature TMS platforms with VCS integration**, **lightweight API-first options**, **Mozilla's community-focused platform**, and **self-hosted machine translation engines**.

### Weblate
**Stack:** Python / Django / PostgreSQL / Redis | **License:** GPLv3
Weblate is the most feature-complete and widely used open-source TMS, supporting **50+ file formats** including PO, XLIFF, JSON, Android XML, iOS Strings, and Java Properties . Its key differentiator is **native Git and Mercurial integration**—translations are stored directly in version control, with a continuous localization workflow that syncs with source code changes . Features include built-in translation memory, machine translation integration (DeepL, Google Translate, LibreTranslate), **50+ automated quality checks**, glossary management, an add-ons system for automated tasks, and a comprehensive REST API . It is available as both self-hosted and hosted SaaS (hosted.weblate.org) . **Trade-off:** Resource-intensive for large instances (100+ projects), the UI can feel dense for non-technical users, and advanced customization requires Python/Django knowledge .
**Best for:** Organizations requiring full VCS integration and extensive file format support, particularly development teams and open-source projects wanting translations committed directly to Git.

### Traduora
**Stack:** Node.js / Angular / PostgreSQL | **License:** AGPL-3.0
Traduora is a lightweight, modern TMS built for developer teams wanting a simple, API-first approach to managing translations . Key features include support for **JSON, PO/gettext, XLIFF, Android XML, iOS strings, CSV, and YAML** file formats, a REST API with secured access for build-time fetching or automation, roles and permissions for project-level access control, and Docker-based self-hosting . It is explicitly positioned as suitable for smaller teams wanting simplicity over the feature density of Weblate . **Trade-off:** Less feature-complete than Weblate, with a smaller community and fewer integrations .
**Best for:** Smaller developer teams wanting a lightweight, API-first TMS with Docker deployment, accepting a narrower feature set than Weblate.

### Accent
**Stack:** (Check repository) | **License:** Open Source
Accent is a free, open-source web-based collaboration platform for translation and localization projects, with a clean interface for translators working across JSON, YAML, Properties, and Gettext PO formats . Features include **real-time collaboration** with conflict resolution, **version control integration** with Git repositories, **translation memory** for consistency, and comprehensive reporting tools . It provides an API and CLI tools for automation and integration with development workflows. The latest version is v1.29.0 (April 2026) .
**Best for:** Teams wanting a collaborative TMS with real-time editing and Git integration, accepting a smaller ecosystem than Weblate.

### Localess
**Stack:** Angular / Firebase | **License:** Open Source
Localess is a translation management tool and CMS built on Angular and Firebase, with **AI-assisted translation** via Google Translate . Key features include real-time localization content editing without requiring application rebuilds, a CMS with schematics for content data definition and validation, hierarchical content creation, user management with granular permissions, API integration with any application, and **Google CDN integration** (~20ms response for 5,000 translations) . It is free forever with no licensing costs—you pay only for infrastructure . **Trade-off:** Firebase dependency ties it to Google Cloud, and it is more of a CMS+translation hybrid than a pure TMS .
**Best for:** Teams already using Firebase or wanting a lightweight, AI-assisted translation tool with CDN-backed fast delivery, accepting the Firebase infrastructure dependency.

### Pontoon
**Stack:** Python / Django / PostgreSQL | **License:** BSD
Pontoon is Mozilla's in-house TMS, built to manage localization for Firefox, MDN, and other Mozilla projects . Its standout feature is **in-context translation**—translators can edit strings directly within the live website, seeing exactly how translations appear . It is designed for large volunteer communities with role management, team leads, and translation suggestions, with shared translation memory across Mozilla projects and native support for Mozilla's Fluent localization format (.ftl files) . **Trade-off:** Heavily tailored to Mozilla's workflow, adaptation for other use cases requires effort; smaller community than Weblate and less frequent release cadence .
**Best for:** Community-driven translation projects with volunteer contributors, particularly those using Fluent or requiring in-context translation.

### LibreTranslate
**Stack:** Python / Argos Translate | **License:** AGPL-3.0
LibreTranslate is a free and open-source **machine translation API** that is entirely self-hosted and does not rely on proprietary software like Google or Azure . Its translation engine is powered by the open-source Argos Translate library, with offline capability and easy Docker deployment . It supports language detection, batch translation, and multiple language bindings (Rust, Node.js, TypeScript, .NET) . **Trade-off:** Translation quality is generally lower than DeepL or Google Translate, particularly for less common language pairs; it is a translation engine rather than a full TMS .
**Best for:** Teams wanting a fully self-hosted, offline-capable machine translation API to integrate into their localization workflow, accepting quality trade-offs versus commercial engines.

### LTEngine
**Stack:** Rust / llama.cpp / LLM models | **License:** Open Source
LTEngine is a free and open-source **local AI machine translation API** written in Rust, entirely self-hosted and compatible with LibreTranslate . Its translation capabilities are powered by **large language models (LLMs)** that run locally via llama.cpp, with models significantly larger than LibreTranslate's lightweight transformers—for some languages, quality is reported as on par with or better than DeepL . It supports CUDA, Metal, and Vulkan accelerators, with the largest model (gemma3-27b) fitting on a single RTX 3090 with 24GB VRAM . **Trade-off:** Active development with current limitations; requires significant GPU resources for best quality, and CPU-only operation is possible but slow .
**Best for:** Teams with GPU resources wanting high-quality, fully local machine translation that rivals DeepL, accepting the hardware requirements and active-development status.

---

## 📊 Comparison at a Glance

| Software | License | Stack | Translation Memory | Git Integration | Machine Translation | Self-Hosted | Best For |
|----------|---------|-------|-------------------|-----------------|---------------------|-------------|----------|
| **Crowdin** | Proprietary | Cloud | ✅ | ✅ Seamless | ✅ 10+ engines | ❌ | Dev teams + OSS free tier |
| **Lokalise** | Proprietary | Cloud | ✅ | ✅ | ✅ Limited | ❌ | Non-technical stakeholders |
| **Phrase** | Proprietary | Cloud | ✅ | ✅ | ✅ 30+ engines | ❌ | Enterprise breadth |
| **Weblate** | GPLv3 | Python/Django | ✅ | ✅ Native VCS | ✅ DeepL/Google/Libre | ✅ | Full VCS integration + 50 formats |
| **Traduora** | AGPL-3.0 | Node.js/Angular | (Check) | (API-based) | (Check) | ✅ | Lightweight API-first |
| **Accent** | Open Source | (Check) | ✅ | ✅ | (Check) | ✅ | Real-time collab + Git |
| **Localess** | Open Source | Angular/Firebase | ❌ | ❌ | ✅ Google Translate | ✅ (Firebase) | AI-assisted + CDN delivery |
| **Pontoon** | BSD | Python/Django | ✅ | (Mozilla workflow) | (Check) | ✅ | In-context + Fluent |
| **LibreTranslate** | AGPL-3.0 | Python/Argos | N/A (Engine) | ❌ | ✅ Self-hosted MT | ✅ | Offline MT API |
| **LTEngine** | Open Source | Rust/llama.cpp | N/A (Engine) | ❌ | ✅ LLM-based MT | ✅ | High-quality local MT |

---

## 🤝 Contributing

Contributions are welcome! If you know of an open-source Multi-Language Translation or Localization tool that should be listed here, please open a pull request with:

- Project name and URL
- Brief description (1–2 sentences)
- Stack and license
- Why it stands out

Please ensure the project is actively maintained (releases within the last 12 months) and genuinely open-source.

**Note on the open-source ecosystem:** The localization space splits between **full TMS platforms** (Weblate, Traduora, Accent, Pontoon) that manage translation workflows, and **machine translation engines** (LibreTranslate, LTEngine) that provide the translation capability itself. **Weblate** is the clear open-source leader, with 50+ file formats, native VCS integration, translation memory, and active development—it is the only open-source TMS that matches the feature depth of commercial platforms like Crowdin . **Traduora** and **Accent** offer lighter alternatives for teams wanting simplicity or real-time collaboration . **Pontoon** is purpose-built for community translation with in-context editing, but is tightly coupled to Mozilla's workflow . On the machine translation side, **LibreTranslate** provides a proven, offline-capable engine with lower quality, while **LTEngine** leverages local LLMs to achieve quality rivaling DeepL at the cost of significant GPU resources . No open-source TMS fully replicates Lokalise's UX polish or Phrase's 30+ MT engine breadth, but Weblate covers the core workflow comprehensively for self-hosted deployments.

---

## 📄 License

This list is released under CC0 1.0 Universal (Public Domain). The software projects listed retain their respective licenses.

---

⭐ **If this list helped you discover a useful tool, please star the repo!** ⭐
