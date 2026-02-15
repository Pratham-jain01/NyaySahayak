# ⚖️ Nyay Sahayak (न्याय सहायक)

**Democratizing Indian Justice through Agentic AI.**

Nyay Sahayak is an AI-powered legal assistant system designed for the Indian judicial ecosystem. It bridges the gap between complex legal frameworks and the people who need them by providing a specialized three-tier interface for **Citizens**, **Lawyers**, and **Judges**.

---

## 🚀 Project Overview

The Indian legal system often presents barriers in language, complexity, and speed. **Nyay Sahayak** leverages Retrieval-Augmented Generation (RAG) and Agentic AI to provide role-specific legal intelligence while ensuring strict data sovereignty within Indian jurisdiction.

### The Three Pillars
* **Common Citizens**: Simplified, jargon-free explanations of rights and step-by-step procedural guidance in regional languages.
* **Legal Professionals**: High-speed research tools, case law search across Supreme and High Courts, and automated judgment summarization.
* **Judiciary**: Neutral decision-support summaries, conflict detection between precedents, and judicial hierarchy analysis.

---

## 🛠️ Technical Architecture

The system employs a microservices architecture with role-based access control and a comprehensive legal knowledge base.

### Tech Stack
| Component | Technology |
| :--- | :--- |
| **Primary LLM** | Anthropic Claude 3.5 Sonnet (200K Context) |
| **Backend** | Python with FastAPI (Async) |
| **Frontend** | Next.js 14, Tailwind CSS, shadcn/ui |
| **Vector DB** | Pinecone (Production Scale) / Qdrant (Self-hosted option) |
| **Data Layers** | PostgreSQL (Audit Data), MongoDB (Legal Documents), Redis (Cache) |

### Advanced AI/ML Pipeline
* **Hierarchical RAG**: A multi-level chunking strategy (Summary, Section, and Sliding Window) to process Indian legal judgments that often exceed 100 pages.
* **PII Masking**: Automatic detection and masking of sensitive personal information (names, Aadhaar, phone numbers) before LLM processing to ensure privacy.
* **Semantic Search**: Precise retrieval of precedents using cosine similarity within the vector space:
    $$\text{similarity} = \cos(\theta) = \frac{\mathbf{A} \cdot \mathbf{B}}{\|\mathbf{A}\| \|\mathbf{B}\|}$$

---

## 📂 Documentation

Detailed specifications are available in the repository:
* **[Requirements Specification](./requirements.md)**: Features MoSCoW prioritization, regional language scope (Hindi, Marathi, Gujarati, etc.), and verified data sources like JUDIS and India Code.
* **[Design Document](./design.md)**: Deep dive into the API architecture, database schemas, and the full AI/ML pipeline.

---

## 🛡️ Compliance & Ethics
* **Data Sovereignty**: All components are hosted within the AWS Mumbai region to ensure compliance with Indian data residency requirements.
* **Legal Compliance**: Built to align with the IT Act 2000 and the Digital Personal Data Protection Act 2023.
* **Neutrality**: Decision-support summaries for judges maintain strict neutrality without suggesting specific legal outcomes.

---

## 🌍 Regional Language Scope (Phase 1)
Nyay Sahayak is committed to breaking language barriers by supporting:
* English
* Hindi
* Marathi
* Gujarati
* Tamil
* Telugu
