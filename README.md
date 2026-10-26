# Kreo: Autonomous Social Media Engine

![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)
![Status: Production](https://img.shields.io/badge/Status-Production-success.svg)

Kreo is a fully autonomous, closed-loop content engine designed to manage the entire lifecycle of social media posts. It scales marketing output by combining scheduled AI ideation with a secure, spreadsheet-driven human-in-the-loop approval architecture.



## 🔗 Live Demo
- **Live Website:** N/A (Internal Content Automation Pipeline)
- **Deployment Platform:** n8n (Cloud/Self-Hosted)



## 📌 Project Overview
This repository contains the exported JSON workflows and environment configurations for the Kreo Social Engine. It enables marketing teams and creators to scale their content output while maintaining strict editorial control through a familiar Google Sheets interface.

### Key Highlights
- **Automated Ideation:** A scheduled cron job triggers an LLM to brainstorm and parse unique niche topics into actionable database items.
- **Human-in-the-Loop Routing:** A Wait Node architecture pauses execution, ensuring no AI-generated content is published without explicit human approval.
- **Dynamic Asset Processing:** Conditional logic detects image attachments, processes URL fetching, and strips C2PA metadata to prevent algorithmic penalization.
- **Deduplication & Audit Logging:** Syncs execution status in real-time with Google Sheets and records live publication URLs to maintain a pristine content portfolio.



## 🛠 Tech Stack

| Category | Technology |
| :--- | :--- |
| **Workflow Engine** | n8n |
| **AI / LLM Drafting** | OpenAI API / Google Gemini |
| **Database / CRM** | Google Sheets API |
| **Asset Processing** | HTTP Request (File Buffer) |
| **Version Control** | Git & GitHub |



## 📁 Repository Structure

├── assets/                  # Static assets and architecture diagrams
├── docs/                    # Onboarding guides and technical manuals
├── sample-data/             # Synthetic testing JSON payloads
├── .env.example             # Template for API keys & OAuth setup
├── .gitignore               # Specifies local files Git should ignore
├── README.md                # Project documentation and setup guidelines
├── workflow.json            # The core drafting, approval, and distribution pipeline
└── brainbox-workflow.json   # The scheduled AI topic ideation cron job



## 🚀 Getting Started

Follow these instructions to run a copy of the project locally for development or testing purposes.

### Prerequisites

- A modern web browser (Chrome, Edge, Firefox, Safari)
- [Git](https://git-scm.com/) installed on your local machine
- An active n8n instance (Local desktop app or Cloud)
- A Google Cloud Console project with Sheets API enabled

### Installation & Local Setup

1. **Clone the repository:**

git clone https://github.com/danieldazong/kreo-social-engine.git
cd kreo-social-engine


2. **Configure Environment Variables:**

Duplicate the `.env.example` file, rename it to `.env`, and populate your OpenAI and Google Sheets OAuth credentials.


3. **Import Workflows into n8n:**

Open your n8n workspace, navigate to the workflows dashboard, and select **Import from File**. Upload `workflow.json` and `brainbox-workflow.json` directly from the root directory of this repository.


4. **Run the local development server:**

Ensure your Google Sheets audit log is created with the exact headers specified in the documentation. Click **Execute Workflow** to test the ideation pipeline.



## 📬 Contact & Connect

- **Developer:** Daniel Dazong
- **LinkedIn:** https://www.linkedin.com/in/danieldazong
- **GitHub:** https://github.com/danieldazong
- **Email:** danieldazong08@gmail.com
