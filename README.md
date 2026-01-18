# Self-Evolution Skills

This repository contains a collection of evolving skills designed to enhance the capabilities of AI agents. These skills cover areas such as knowledge management, session recording, and specialized domain expertise.

## Available Skills

### 1. Check Tips (`check-tips`)

- **Directory**: `skills/check-tips/`
- **Description**: Automatically checks for existing tips in `./.tips/tips.md` before executing tasks or answering questions. This ensures that the agent applies best practices and lessons learned from previous interactions.

### 2. Record Session (`record-session`)

- **Directory**: `skills/generate-records/`
- **Description**: A comprehensive skill for recording session content into structured documents. It emphasizes structured output, consistent file organization, and detailed technical documentation.
- **Key Capabilities**:
  - **Structured Output**: Generates templated Markdown responses.
  - **Context-Aware Analysis**: Breaks down complex problems into logical sections.
  - **Technical Documentation**: Logs debugging steps, error messages, and solutions.
  - **Prompt Optimization**: Transforms vague requests into actionable instructions.

### 3. Tip Manager (`tip-manager`)

- **Directory**: `skills/generate-tips/`
- **Description**: Enables the agent to "evolve" by learning from mistakes. It manages a persistent list of concise debugging tips, adding new ones only when explicitly instructed.
- **Usage**:
  - **Trigger**: User commands like "Save this as a tip" or "Remember this fix".
  - **Format**: Distills lessons into `IF [condition], THEN [action]` format.
  - **Storage**: Appends tips to `./tips/tips.md`.

### 4. Project Knowledge (`project-knowledge`)

- **Directory**: `skills/proj-knowledge/`
- **Description**: Imbues the agent with the persona of a Senior Full-Stack Quantitative Developer specializing in a Bitcoin macro-analysis system.
- **Expertise**:
  - **Tech Stack**: FastAPI, React, Pandas, SQLite/PostgreSQL.
  - **Architecture**: Strict separation of concerns (Modules A-D), time-series alignment ("The Step Function"), and rigorous backtesting logic.
- **Commands**:
  - `/roadmap`: Display project status.
  - `/code [Component]`: Generate production-ready code.
  - `/math`: Explain quantitative logic.
  - `/debug`: Analyze code for look-ahead bias.

## Directory Structure

```
.
├── skills/
│   ├── check-tips/         # Skill: check-tips
│   ├── generate-records/   # Skill: record-session
│   ├── generate-tips/      # Skill: tip-manager
│   └── proj-knowledge/     # Skill: project-knowledge
└── README.md
```
