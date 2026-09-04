# AI Email Intelligence & Automation

An AI-powered Gmail automation workflow built with **n8n, Groq, and Google Sheets** to classify incoming emails, apply appropriate Gmail labels, and generate reply drafts when required.

## 🚀 Features

- 📩 Automatically reads incoming Gmail emails
- 🤖 Uses an AI Agent for email classification
- 🏷️ Classifies emails into:
  - `spamm`
  - `Personal`
  - `Work`
  - `draft`
- 📨 Applies the appropriate Gmail label
- ✍️ Generates AI-powered reply drafts for Personal, Work, and Draft emails
- 🚫 Spam emails are labeled without creating a reply draft
- 📊 Logs processed emails and classification details in Google Sheets
- 🔒 Emails are never sent automatically

## 🔄 Workflow

```text
Gmail Trigger
      ↓
Edit Fields
      ↓
AI Agent
      ↓
Switch
 ┌────┼────────┬────────┐
 ↓    ↓        ↓        ↓
spamm Personal Work    draft
 ↓      ↓        ↓        ↓
Label  Label    Label    Label
        ↓        ↓        ↓
      Draft    Draft    Draft
        └────────┼────────┘
                 ↓
          Google Sheets
