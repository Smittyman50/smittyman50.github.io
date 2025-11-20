[← Back to Home](./index.md)

## Knowledge Systems & Second Brain

This page highlights how I use Obsidian, Zettelkasten, and AI-augmented workflows to build a structured personal knowledge system. My setup integrates local LLMs running in my homelab, automated note generation pipelines, and deeply cross-linked evergreen notes that support research, writing, and continuous learning.

---

### Architectural Overview

My knowledge system combines Obsidian’s flexibility with a disciplined note architecture and locally hosted AI models. The system focuses on creating durable, interconnected knowledge that supports both long-term retention and rapid retrieval.

<div align="center">
  <img src="./assets/images/knowledge/second-brain-architecture.png" width="750" alt="Second Brain Architecture Diagram"/>
</div>

*Figure: High-level flow of how notes move through my system and how local LLMs augment the process.*

---

### Vault Structure & Note Architecture

Obsidian serves as the primary interface for capturing, organizing, and synthesizing knowledge. My vault is structured around clear, purpose-driven note types:

#### **Note Types**
- **Fleeting Notes** – Quick ideas and observations captured during reading, meetings, or hands-on work.
- **Literature Notes** – Structured notes summarizing academic papers, books, articles, and documentation.
- **Permanent Notes** – Evergreen Zettels that represent atomic concepts, directly linked to related ideas.
- **Project Notes** – Documentation, diagrams, and work logs tied to specific implementations.
- **Daily Notes** – Journals, daily logs, and auto-generated summaries.

#### **Cross-Linking**
Knowledge is built through deliberate, bi-directional linking:

```
[[machine-learning-overfitting]]
[[aws-proxmox-network-architecture]]
[[emotion-recognition-cnn-notes]]
[[obsidian-ai-workflow]]
```

This creates a resilient network of ideas rather than a static folder tree.

---

### AI-Augmented Workflows

Local AI tools enhance the capture and synthesis of information without relying on cloud-based inference.

#### **Text Generator Plugin**
- Converts rough ideas into structured notes  
- Summarizes long passages or transcripts  
- Extracts key points and action items  
- Generates outlines and expanding bullet points  

#### **Companion Plugin**
- Provides inline AI completion  
- Suggests next steps, definitions, or clarifications  
- Works on-demand as I write

#### **Msty.AI Integration**
Msty acts as an intelligent retrieval engine over selected “knowledge stacks” inside Obsidian:

- Uses embeddings to understand context  
- Searches across curated note collections  
- Returns relevant notes, insights, and references  
- Integrates with local LLMs through API  

#### **Local LLM Integration**
I run multiple models in my homelab and access them through OpenWebUI:

- **Ollama** for endpoint-based inference  
- **DeepSeek-R1**, **LLaMA**, and code-focused models  
- Fast, private, offline access  
- Consistent performance and predictable latency  

<div align="center">
  <img src="./assets/images/knowledge/local-llm-architecture.png" width="750" alt="Local LLM Architecture Diagram"/>
</div>

*Figure: How Obsidian, Msty, and local LLMs integrate to support retrieval and synthesis.*

---

### Automated Note Pipelines

A core principle in my system is reducing manual overhead and letting automation handle repetitive work.

#### **Automations include:**
- Summarizing meeting transcripts into literature notes  
- Extracting atomic notes from long-form content  
- Converting daily journals into actionable summaries  
- Auto-tagging and categorizing new notes  
- Generating cross-links based on semantic similarity  
- Transforming project documentation into evergreen entries  

---

### Example Use Cases

#### **1. Academic Research**
During my MSCS (AI & ML) program, I used this system to manage:
- Academic papers  
- D804 capstone notes  
- Model design documentation  
- Experiment logs and findings  
- Classification and evaluation artifacts  
- Literature summaries that fed directly into academic writing  

#### **2. Professional Architecture Work**
I use the system to track:
- Cloud architecture patterns  
- CX integration design notes  
- Network automation approaches  
- Troubleshooting logs and RCA documentation  

#### **3. Homelab Documentation**
My Obsidian vault stores:
- Proxmox cluster configuration notes  
- MikroTik routing diagrams  
- VRRP and High Availability strategy notes  
- TrueNAS ZFS pool design rationale  
- Automation workflows for Ansible and Terraform  

#### **4. Personal Projects**
This includes:
- Raspberry Pi greenhouse automation logic  
- Ham radio (APRS, Direwolf, APRX) configurations  
- LLM experiments hosted in SmittyNet  

---

### Tools & Platforms

- **Obsidian** (primary interface)  
- **Zettelkasten note architecture**  
- **Text Generator & Companion plugins**  
- **Msty.AI** for contextual retrieval  
- **Local LLMs** via Ollama  
- **OpenWebUI API**  
- **Proxmox cluster** powering AI models  
- **TrueNAS SCALE** backing storage for the vault  
- **Incus containers** for lightweight AI utilities  

---

### Why This Matters

This knowledge system is more than a note-taking workflow — it’s an active part of how I learn, build, and design. It accelerates my ability to:

- Connect new ideas with existing knowledge  
- Generate new concepts rapidly  
- Maintain high-quality technical documentation  
- Support academic writing and thought leadership  
- Build complex systems with clear reasoning and recall  

It’s a force multiplier across everything I do — from AI model development and network automation to homelab experimentation and professional consulting.

---

[← Back to Home](./index.md)