# AI-Powered Resume Tailoring Assistant (n8n Workflow)

This project is a no-code/low-code workflow built with **n8n** that uses an AI Agent to analyze and tailor resumes based on a submitted job description.

##  Features

-  Resume and job description upload via form
-  AI analysis and ATS optimization
-  Field-level resume rewrites and keyword tailoring
-  Sends copy-paste ready content in the format the user chooses (Markdown, HTML, or Plain Text)

## Tech Stack

- **n8n** workflow automation
- **Google Generative AI / OpenAI**
- Custom prompt engineering and schema validation
- Optional: Markdown/HTML render options for copy/paste blocks

## How It Works

```mermaid
flowchart TD
  A[" Form Submission"] --> B["🔍 Extract Content"]
  B --> C[" AI Analysis"]
  C --> D{" Valid Output?"}
  D -->|No| E[" Repair JSON"]
  E --> D
  D -->|Yes| F["Email Report"]
