# 📧 Enterprise Gmail MCP Server

A production-ready **Model Context Protocol (MCP) Server** built using Python and the official MCP SDK that enables AI assistants like **Google Antigravity** to securely interact with Gmail using natural language.

The server supports **multiple Gmail accounts**, OAuth2 authentication, and exposes Gmail operations as MCP tools for searching, reading, sending, labeling, and organizing emails.

---

## ✨ Features

### 📬 Gmail Operations

- 🔍 Search emails using Gmail search queries
- 📖 Read complete emails
- 🧵 Read email threads
- ✉️ Send emails
- 📝 Create drafts
- 📥 Download attachments

### 🏷️ Label Management

- Create labels
- Delete labels
- List labels
- Apply labels
- Remove labels

### 📂 Email Management

- Move emails to Trash
- Permanently delete emails
- Restore emails
- Mark as Read
- Mark as Unread
- Star / Unstar emails

### 👥 Multi-Account Support

Manage multiple Gmail accounts from a single MCP server.

Example:

- Personal Gmail
- Work Gmail
- College Gmail
- Organization Gmail
- Google Workspace Accounts

Each request can target a specific account:

```text
account_name="personal"

account_name="greatlakes"

account_name="secondary"
```

---

## 🚀 MCP Tools

The server exposes the following tools to any MCP-compatible client.

| Tool | Description |
|------|-------------|
| gmail_search | Search emails |
| gmail_read_email | Read an email |
| gmail_read_thread | Read an email thread |
| gmail_send_email | Send email |
| gmail_create_draft | Create draft |
| gmail_create_label | Create Gmail label |
| gmail_delete_label | Delete Gmail label |
| gmail_apply_label | Apply label to email |
| gmail_remove_label | Remove label from email |
| gmail_list_labels | List Gmail labels |
| gmail_delete_email | Permanently delete email |
| gmail_trash_email | Move email to Trash |
| gmail_restore_email | Restore email |
| gmail_mark_read | Mark email as Read |
| gmail_mark_unread | Mark email as Unread |
| gmail_star_email | Star email |
| gmail_unstar_email | Remove Star |
| gmail_download_attachment | Download attachment |
| gmail_list_threads | List email threads |
| gmail_get_profile | Retrieve Gmail profile |

---

## 🏗️ Project Structure

```text
gmail-mcp/

├── auth/
├── config/
├── models/
├── services/
├── tools/
├── server_mcp/
├── tests/
├── tokens/
├── utils/
│
├── requirements.txt
├── README.md
└── .env
```

---

## 🔐 Authentication

Authentication is handled using **Google OAuth2**.

Each Gmail account maintains its own OAuth token, enabling secure access to multiple accounts simultaneously.

```text
accounts.json
      │
      ▼
Account Manager
      │
      ▼
Auth Manager
      │
      ▼
Google OAuth2
      │
      ▼
Gmail API
```

---

## ⚙️ Technology Stack

- Python 3
- Official MCP Python SDK
- Google Gmail API
- Google OAuth2
- Google API Client
- Pydantic
- FastMCP
- JSON
- OAuth Credentials

---

## 📦 Installation

Clone the repository

```bash
git clone https://github.com/<username>/gmail-mcp.git

cd gmail-mcp
```

Create a virtual environment

```bash
python -m venv .venv
```

Activate the environment

Windows

```bash
.venv\Scripts\activate
```

Linux / macOS

```bash
source .venv/bin/activate
```

Install dependencies

```bash
pip install -r requirements.txt
```

---

## 🔧 Configuration

1. Create a Google Cloud Project.
2. Enable the Gmail API.
3. Configure the OAuth Consent Screen.
4. Download the OAuth Client credentials.
5. Place the credentials file in:

```text
config/credentials.json
```

Configure Gmail accounts in:

```text
config/accounts.json
```

Generate OAuth tokens for each configured account.

---

## ▶️ Running the MCP Server

```bash
python -m server_mcp.server
```

---

## 🧪 Running Tests

Run all unit tests

```bash
python -m unittest discover tests
```

Run Gmail integration test

```bash
python test_gmail.py
```

---

## 💡 Example Prompts

Search emails

```text
Search my Gmail for "Business Intelligence"
```

Search a specific account

```text
Search my Great Lakes Gmail for MAQ emails.
```

Apply labels

```text
Apply the label MAQ to all MAQ emails in my Great Lakes account.
```

Read emails

```text
Read the latest email from Microsoft.
```

Create a draft

```text
Draft a reply thanking the recruiter for the interview opportunity.
```

---

## 🔒 Security

- OAuth2 Authentication
- Local Token Storage
- No Credentials Hardcoded
- Per-Account Token Isolation
- Secure Gmail API Access
- Local Execution

---

## 📈 Future Enhancements

- AI Email Summarization
- Cross-Account Search
- Smart Email Categorization
- Semantic Search
- Inbox Cleanup Automation
- Duplicate Email Detection
- Calendar Integration
- Google Drive Integration
- Outlook MCP Server
- Microsoft Graph Support

---

## 🤝 Contributing

Contributions, feature requests, and suggestions are welcome.

Feel free to fork the repository and submit a pull request.

---

## 📄 License

This project is licensed under the MIT License.

---

## 👨‍💻 Author

**Praveen Kumar**

MBA | Business Analyst | AI & Data Analytics Enthusiast

- GitHub: https://github.com/<your-github-username>
- LinkedIn: https://linkedin.com/in/<your-linkedin-profile>

---

⭐ If you found this project useful, consider giving it a star!
