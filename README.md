# fathom-to-linear-automation
Automated workflow to transform Fathom meeting notes into Linear tickets using n8n (Docker) on AWS EC2 and Groq (LLM).


🎯 Objective
To bridge the gap between client/manager requirements and technical execution by automatically extracting action items from Fathom meetings and syncing them directly into Linear as prioritized issues.

🛠️ Tech Stack
Ingestion: Fathom (AI Meeting Assistant & Transcription).

Orchestration: n8n (Dockerized on AWS EC2).

Cloud Infrastructure: AWS EC2 (t2.micro - Free Tier).

AI Inference: Groq (Llama 3.1) for high-speed NLP processing.

Project Management: Linear (Issue Tracking).

Notifications: Slack (Instant Workflow Alerts).

🏗️ System Architecture
Webhook Trigger: Fathom sends a transcript payload to the n8n webhook upon meeting completion.

Data Processing: n8n cleans the transcript and prepares a structured prompt.

LLM Reasoning: Groq processes the text via Llama 3.1 to identify technical requirements, priorities, and labels.

Issue Creation: n8n iterates through the AI-generated JSON to create individual issues in Linear.

Status Update: A summary of created tickets is posted to a designated Slack channel.

🚀 Roadmap
[ ] Provision AWS EC2 Instance and Security Groups.

[ ] Deploy n8n via Docker Compose.

[ ] Configure Fathom Webhooks and Groq API Integration.

[ ] Design and test the n8n Workflow logic.

[ ] Final integration with Linear and Slack.

📜 License
Distributed under the MIT License. See LICENSE for more information.
