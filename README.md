# 📚 Exam Engine 2.0

> **A modular AI-powered engine for generating, validating and exporting high-quality reading comprehension exams inspired by the Colombian Saber 11 assessment.**

![Version](https://img.shields.io/badge/version-2.0-blue)
![Status](https://img.shields.io/badge/status-active-success)
![License](https://img.shields.io/badge/license-MIT-green)

---

## 📖 Overview

**Exam Engine 2.0** is an extensible web application designed to generate complete reading comprehension assessments using Large Language Models (LLMs) and image generation models.

Unlike traditional exam generators, Exam Engine separates:

- exam logic
- prompt generation
- AI providers
- rendering
- validation
- export

into independent modules, making the project scalable, maintainable and provider-agnostic.

The project is inspired by the structure and philosophy of the Colombian **Saber 11 Reading Test**, while remaining flexible enough to support other educational assessment formats.

---

# ✨ Main Features

- 🧠 AI-assisted exam generation
- 📖 Seven Reading Test sections
- 🖼 AI image generation for visual questions
- 🔄 Multiple LLM providers
- 🎨 Multiple image generation models
- 📄 PDF / HTML / JSON export
- ⚙ Modular architecture
- 📱 Responsive interface
- 🔌 Bring Your Own Provider (BYOP)
- ✅ JSON schema validation
- 🧩 Template-based rendering
- 🌍 English and Spanish support

---

# 🏗 Architecture

Exam Engine follows a layered architecture.

```
User Interface

↓

Controllers

↓

Exam Engine

↓

Prompt Engine

↓

AI Providers

↓

Validation Engine

↓

Render Engine

↓

Export Engine
```

Each module has a single responsibility, allowing future providers or rendering engines to be added without modifying the application core.

---

# 🧠 Supported AI Providers

The architecture is provider-independent.

Current and planned providers include:

- Pollinations
- OpenAI
- Google Gemini
- OpenRouter
- Ollama
- LM Studio
- Local providers

---

# 🎨 Supported Image Models

The image generation engine supports multiple models, including:

- flux
- zimage
- klein
- grok-imagine
- nanobanana
- gptimage
- gptimage-large
- wan-image
- qwen-image
- gpt-image-2

The architecture allows new models to be added without changing application logic.

---

# 📂 Project Structure

```
exam-engine/

├── css/
├── js/
│   ├── core/
│   ├── engine/
│   ├── providers/
│   ├── renderers/
│   ├── ui/
│   └── utils/
│
├── config/
├── prompts/
├── schemas/
├── templates/
├── assets/
├── docs/
└── exports/
```

---

# 🧩 Design Principles

Exam Engine is built following modern software engineering principles:

- Single Responsibility Principle (SRP)
- Separation of Concerns
- Low Coupling
- High Cohesion
- Provider Abstraction
- Configuration over Hardcoding
- Modular Components
- JSON Schema Validation
- Event-driven workflow

---

# 📄 Reading Test Structure

The application supports the seven sections commonly found in reading comprehension assessments.

Examples include:

- Signs and Notices
- Short Dialogues
- Visual Interpretation
- Short Texts
- Long Texts
- Multiple Matching
- Extended Reading

Each section is generated independently using dedicated templates and JSON schemas.

---

# 🖼 Image Generation

Visual questions use an independent Image Engine.

Features include:

- POST API requests
- Base64 response handling
- Multiple image models
- Configurable quality
- BYOP authentication
- Image caching
- Automatic retries

---

# 📦 Export Options

Generated exams can be exported as:

- HTML
- PDF
- JSON

Additional formats such as DOCX are planned.

---

# 🔑 Bring Your Own Provider (BYOP)

Exam Engine never stores API keys in the source code.

Each user configures their preferred provider independently.

Supported authentication includes:

- API Keys
- Local Providers
- Self-hosted models

See:

```
docs/README_BYOP.md
```

---

# 🚀 Roadmap

### Version 2.0

- Modular architecture
- Provider Manager
- Image Engine
- Export Engine
- Responsive Workspace
- AI Model Selector
- Exam State Manager

### Future Releases

- Collaborative editing
- Question bank
- Adaptive testing
- Learning analytics
- LMS integration
- Multi-language interface

---

# 🤝 Contributing

Contributions are welcome.

Before submitting a pull request, please read:

- CONTRIBUTING.md
- ARCHITECTURE.md
- LOVABLE_RULES.md

Every contribution should preserve the architectural principles of Exam Engine.

---

# 📜 License

This project is released under the MIT License.

---

# 👨‍💻 Author

**Edgar Herrera**

Educational researcher, software designer and AI enthusiast focused on building innovative tools for language learning and educational assessment.

---

## ⭐ Vision

Exam Engine is not simply an exam generator.

It is a **next-generation assessment platform** that combines artificial intelligence, modular software architecture and educational best practices to create scalable, reusable and high-quality learning experiences.
