<div align="center">

# 🎨 ArtisanAi.v2 - ATS-Friendly Resume Builder

### AI-Powered Professional Document Generation Platform
### *Transform Your Career Story into ATS-Optimized, Recruiter-Ready Documents*

[![Live Demo](https://img.shields.io/badge/demo-live-success?style=for-the-badge&logo=vercel)](https://artisanai-v2-ats-friendly-one-pager-resume-buil-rqpnncje4.vercel.app)
[![TypeScript](https://img.shields.io/badge/TypeScript-007ACC?style=for-the-badge&logo=typescript&logoColor=white)](https://www.typescriptlang.org/)
[![React](https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB)](https://reactjs.org/)
[![Google Gemini](https://img.shields.io/badge/Google%20Gemini-8E75B2?style=for-the-badge&logo=google&logoColor=white)](https://ai.google.dev/)
[![Vercel](https://img.shields.io/badge/Vercel-000000?style=for-the-badge&logo=vercel&logoColor=white)](https://vercel.com/)

[🎯 Try Live Demo](#) • [📖 Documentation](docs/) • [💼 Portfolio](https://portfolio.w3jdev.com) • [📧 Contact](#contact)

---

</div>

> **⚠️ PORTFOLIO SHOWCASE REPOSITORY**  
> This is a **public demonstration** of an AI-powered HR system designed for **Malaysian SMEs**. This demo showcases the frontend architecture, UX design, and AI integration capabilities. Full proprietary implementation (backend services, advanced AI models, enterprise integrations) is maintained privately for client deployments.

---

## 📚 Table of Contents

- [The Problem We Solve](#-the-problem-we-solve)
- [Our Solution](#-our-solution)
- [System Architecture](#%EF%B8%8F-system-architecture)
- [AI Processing Pipeline](#-ai-processing-pipeline)
- [Key Features](#-key-features)
- [Technology Stack](#%EF%B8%8F-technology-stack)
- [Real-World Impact](#-real-world-impact)
- [Getting Started](#-getting-started)
- [Technical Deep Dive](#-technical-deep-dive)
- [For Recruiters & Employers](#-for-recruiters--employers)
- [License](#-license--usage)

---

## 💡 The Problem We Solve

### The Job Application Paradox

**Traditional Resume Creation Problems:**
- 📊 **75% of resumes** are rejected by ATS before human review
- ⏱️ **90% of applicants** spend 3-5 hours formatting resumes
- ❌ **No standardization** - every job needs different formatting
- 🎯 **Poor keyword optimization** - missing critical ATS keywords
- 📝 **Generic templates** - don't highlight unique value propositions
- 🔄 **Endless revisions** - manual editing for each application

**Personal Story:**
> "I needed to apply for senior engineering roles across Malaysian tech companies. Each application required tailored resumes, cover letters, and formatting to pass ATS systems. Spending 2-3 hours per application wasn't sustainable. **There had to be a smarter way.**" - W3JDEV

---

## ✨ Our Solution

**ArtisanAi.v2** transforms raw career information into polished, ATS-optimized documents:

```
Raw Input (5 minutes)  →  AI Processing  →  Professional Documents (Ready in 30s)
        ↓                        ↓                      ↓
   Basic info              Google Gemini          ATS-optimized resume
   Work history            Context analysis       Tailored cover letter
   Skills list             Content generation     Perfect formatting
```

### Transform Your Application Process

| Before ArtisanAi | After ArtisanAi |
|------------------|-----------------|
| 3-5 hours per resume | 30 seconds generation time |
| Manual ATS optimization | AI-powered keyword matching |
| Generic templates | Role-specific customization |
| Multiple revisions | One-click perfection |
| Formatting struggles | Professional design guaranteed |
| Low ATS pass rate (25%) | High ATS pass rate (85%+) |

---

## 🏗️ System Architecture

### High-Level Architecture

```mermaid
graph TB
    subgraph "User Layer"
        A[Web Interface<br/>React PWA]
        B[Mobile Browser<br/>Responsive]
    end

    subgraph "Frontend Application"
        C[Input Form<br/>Career Data Collection]
        D[Document Generator<br/>UI Controller]
        E[Preview System<br/>Real-time Rendering]
    end

    subgraph "AI Processing Engine"
        F[Google Gemini 2.5 Flash<br/>Content Analysis]
        G[Resume Optimizer<br/>ATS Enhancement]
        H[Cover Letter Generator<br/>Role Matching]
        I[Format Compiler<br/>PDF/DOCX Builder]
    end

    subgraph "Data Layer"
        J[(Local Storage<br/>Draft Management)]
        K[(Session State<br/>User Progress)]
    end

    subgraph "Export Services"
        M[PDF Generation<br/>Print-Ready]
        N[DOCX Export<br/>Editable Format]
        O[Plain Text<br/>ATS Copy-Paste]
    end

    A --> C
    B --> C
    C --> F
    F --> G
    G --> H
    H --> I
    I --> D
    D --> E
    E --> M
    E --> N
    E --> O
    C --> J
    D --> K

    style F fill:#8E75B2,stroke:#fff,stroke-width:3px,color:#fff
    style G fill:#8E75B2,stroke:#fff,stroke-width:3px,color:#fff
    style H fill:#8E75B2,stroke:#fff,stroke-width:3px,color:#fff
    style I fill:#8E75B2,stroke:#fff,stroke-width:3px,color:#fff
```

---

## 🤖 AI Processing Pipeline

### Input → AI → Output Transformation Flow

```mermaid
graph LR
    subgraph "Input"
        A1[User Career Data]
    end

    subgraph "Extraction"
        B1[Profile Analysis<br/>Skills, Experience]
        B2[Role Context<br/>Job Requirements]
        B3[Industry Keywords<br/>ATS Terms]
    end

    subgraph "AI Analysis"
        C1[Gemini 2.5 Flash<br/>Content Understanding]
        C2[Achievement Extraction<br/>Impact Quantification]
        C3[Keyword Optimization<br/>ATS Matching]
    end

    subgraph "Generation"
        D1[Resume Generation<br/>Structured Format]
        D2[Cover Letter<br/>Role-Specific]
        D3[ATS Optimization<br/>Keyword Density]
    end

    subgraph "Output"
        E1[Professional Documents<br/>Ready to Apply]
    end

    A1 --> B1
    A1 --> B2
    A1 --> B3
    B1 --> C1
    B2 --> C1
    B3 --> C1
    C1 --> C2
    C2 --> C3
    C3 --> D1
    C3 --> D2
    C2 --> D3
    D1 --> E1
    D2 --> E1
    D3 --> E1

    style C1 fill:#4285F4,stroke:#fff,stroke-width:2px,color:#fff
    style C2 fill:#4285F4,stroke:#fff,stroke-width:2px,color:#fff
    style C3 fill:#4285F4,stroke:#fff,stroke-width:2px,color:#fff
```

### AI Prompt Engineering

```typescript
// System Prompt for Resume Generation
const RESUME_GENERATION_PROMPT = `
Analyze this candidate's career information and generate an ATS-optimized resume.

CANDIDATE DATA:
- Name: {name}
- Target Role: {role}
- Experience: {experience}
- Skills: {skills}
- Education: {education}

TASK:
Generate a professional one-page resume that:

1. **ATS Optimization**
   - Include {role}-specific keywords
   - Match industry standard terminology
   - Maintain 15-20% keyword density
   - Use standard section headers

2. **Content Structure**
   - **Professional Summary** (3-4 sentences, highlight unique value)
   - **Core Competencies** (8-12 key skills)
   - **Professional Experience** (Impact-driven bullet points)
   - **Education & Certifications** (Relevant credentials)
   - **Technical Skills** (Grouped by category)

3. **Achievement Formatting**
   - Use action verbs (Led, Developed, Architected, Optimized)
   - Quantify impact (%, $, time saved, metrics)
   - Follow STAR method (Situation, Task, Action, Result)
   - Example: "Architected microservices platform reducing deployment time by 70%, serving 2M+ users"

4. **Quality Criteria**
   - One page maximum
   - Professional tone
   - No generic statements
   - Industry-specific language
   - Clear hierarchy and scanning flow

OUTPUT FORMAT: JSON
{
  "summary": "Professional summary paragraph",
  "skills": ["skill1", "skill2", ...],
  "experience": [
    {
      "title": "Job Title",
      "company": "Company Name",
      "duration": "Jan 2020 - Present",
      "achievements": [
        "Quantified achievement 1",
        "Quantified achievement 2"
      ]
    }
  ],
  "education": [...],
  "certifications": [...]
}
`;
```