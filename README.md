<p align="center">
  <img src="screenshots/banner.png" alt="AI Bug Creator Agent Banner" width="100%">
</p>

<h1 align="center">🚀 AI Bug Creator Agent</h1>

<p align="center">
Automatically transform user bug descriptions into structured Jira bug reports using AI.<br>
Powered by <strong>n8n</strong>, <strong>Ollama</strong>, and <strong>Llama 3.1</strong>.
</p>

<p align="center">

![Last Commit](https://img.shields.io/github/last-commit/AbdulrhmanTalaat/AI-Bug-Creator-Agent)
![Repo Size](https://img.shields.io/github/repo-size/AbdulrhmanTalaat/AI-Bug-Creator-Agent)

</p>

---

# 📖 Overview

**AI Bug Creator Agent** is an AI-powered automation workflow built with **n8n** that converts natural language bug reports into structured Jira issues.

Instead of manually filling bug report fields, users simply describe the problem in plain language. The AI Agent analyzes the description, extracts the required information, formats the output into a structured JSON object, and automatically creates a Jira Bug through the Jira API.

This workflow helps QA Engineers, Developers, and Support Teams report bugs faster while ensuring consistency and completeness.

---

# ✨ Features

-  AI-powered bug understanding
-  Accept bug reports in natural language
-  Extract bug title and description automatically
-  Generate structured JSON output
-  Automatically create Jira Bug Issues
-  Built with n8n AI Agent
-  Supports Llama 3.1 running locally via Ollama
-  Create bugs through Jira REST API
-  Fully automated workflow
-  Easy to customize

---

# 🏗 Workflow Architecture

```text
User
 │
 ▼
Chat Trigger
 │
 ▼
AI Agent
(Llama 3.1 via Ollama)
 │
 ▼
Analyze Bug Description
 │
 ▼
Structured Output Parser
 │
 ▼
Validate Required Fields
 │
 ▼
Create Jira Bug
 │
 ▼
HTTP Request (Optional)
```

---

# 📸 Workflow

<p align="center">
  <img src="screenshots/workflow.png" width="100%">
</p>

---

# ⚙️ Tech Stack

| Technology | Purpose |
|------------|---------|
| n8n | Workflow Automation |
| AI Agent | Natural Language Understanding |
| Ollama | Local AI Runtime |
| Llama 3.1 | Large Language Model |
| Structured Output Parser | JSON Validation |
| Jira Cloud API | Create Jira Bugs |
| HTTP Request | External Integration |

---

# 📦 Installation

## 1. Clone the Repository

```bash
git clone https://github.com/AbdulrhmanTalaat/AI-Bug-Creator-Agent.git
```

---

## 2. Import the Workflow

Import the workflow into your n8n instance.

```text
workflow/AI Bug Creator Agent.json
```

---

## 3. Install Ollama

Install Ollama and pull the Llama model.

```bash
ollama pull llama3.1:8b
```

Connect the Ollama Chat Model node to the AI Agent.

---

## 4. Configure Jira

Update your Jira credentials inside n8n.

Configure:

- Jira URL
- Email
- API Token
- Project Key
- Issue Type (Bug)

---

## 5. Run the Workflow

Simply describe a bug.

Example:

```text
When I click the Login button after entering valid credentials, nothing happens. No error message is displayed.
```

The workflow will automatically:

- Analyze the bug description
- Extract bug details
- Generate structured output
- Create a Jira Bug
- Send the result to the configured endpoint (optional)

---

# 💬 Example

### Input

```text
When I click Save after editing my profile, the page keeps loading forever and no changes are saved.
```

### Output

- Detect Bug Title
- Generate Detailed Description
- Validate Required Fields
- Create Jira Bug
- Return Success Response

---

# 📄 Example Output

```json
{
  "summary": "Profile cannot be saved after editing",
  "description": "When editing a user profile and clicking the Save button, the page remains in a loading state indefinitely. No confirmation or error message is displayed, and the changes are not persisted.",
  "issueType": "Bug"
}
```

---

# 📂 Repository Structure

```text
.
├── README.md
├── .gitignore
├── workflow/
│   └── AI Bug Creator Agent.json
└── screenshots/
    ├── banner.png
    └── workflow.png
```

---

# 🎯 Project Scope

This project demonstrates how AI can automate the bug reporting process by converting natural language descriptions into structured Jira Bug Issues.

The workflow is lightweight, easy to extend, and can be integrated with different issue trackers or AI models.

---

# 🚀 Future Improvements

- Support screenshots and attachments
- Auto-detect bug priority
- Predict severity level
- Suggest labels/components
- Duplicate bug detection
- Multi-language support
- Integration with Slack & Microsoft Teams

---

# 🤝 Contributing

Contributions are welcome.

Feel free to fork this repository, open an Issue, or submit a Pull Request.

---

# 👨‍💻 Author

**Abdulrhman Talaat**

Senior Software Test Engineer

GitHub: https://github.com/AbdulrhmanTalaat

If you found this project useful, consider giving it a ⭐.