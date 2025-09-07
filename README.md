# 🤖 AI-Powered Customer Feedback Automation with n8n & Google Gemini

This project demonstrates how to build an **AI Agent workflow in n8n** that automatically processes customer feedback submitted through a form.  
The workflow uses **Google Gemini (Flash 2.5)** as the LLM, integrates with **Airtable, Slack, and Gmail**, and intelligently routes customer feedback into categories for seamless customer support.

---

## 🚀 Features

- **Form Submission Capture**  
  Collects customer details (Name, Contact Number, Email, Feedback).  

- **AI-Powered Classification**  
  Uses Google Gemini to analyze feedback and classify it into:
  - 🟥 Complaint  
  - 🟩 Compliment  
  - 🟦 Feature Addition Request  

- **Automated Actions**  
  - Saves categorized feedback in **Airtable**.  
  - Sends notifications to the **Slack developer team**.  
  - Sends acknowledgment emails to customers.  

---

## 🛠️ Tech Stack

- [n8n](https://n8n.io) – Workflow Automation  
- [Google Gemini Flash 2.5](https://deepmind.google/technologies/gemini/) – LLM Model for AI Agent  
- [Airtable](https://airtable.com) – Feedback Database  
- [Slack](https://slack.com) – Team Notifications  
- [Gmail](https://mail.google.com) – Customer Acknowledgement Emails  

---

## 📂 Workflow Overview

![Workflow Screenshot](./workflow.png)  
*(Replace `workflow.png` with your actual exported screenshot)*  

### Workflow Steps
1. **Form Submission** triggers workflow.  
2. **Google Gemini AI Agent** classifies the feedback.  
3. **Switch Node** routes the response into one of three categories:  
   - 🟥 **Complaint** → Save in Airtable → Notify Slack → Email user.  
   - 🟩 **Compliment** → Save in Airtable.  
   - 🟦 **Feature Request** → Save in Airtable → Notify Slack.  

---

## 📦 Setup Instructions

### 1. Clone this repository
```bash
git clone https://github.com/<your-username>/n8n-ai-feedback-agent.git
cd n8n-ai-feedback-agent
