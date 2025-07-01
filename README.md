# ZendeskConfigAPI
Zendesk testing enviromet and API json file
# 🔧 Zendesk Admin & API Testing Lab – Personal Project

This repo documents a full Zendesk setup I built as part of my preparation for a Systems Engineer interview. I wanted to go beyond the basics and simulate real-world support workflows using both the Zendesk UI and the API.

The project is split in two parts:
- Admin setup and configuration inside Zendesk
- API automation and testing using Postman

---

## 🖥️ Part 1 – Zendesk Admin Setup

I used a trial account and configured it with common features based on what support teams typically request.

### ✅ Channels & Basics
- Email channel configured (Talk wasn't available in the trial)
- Views set up by status and tags

### 🔧 Triggers
- Auto-reply to new tickets
- Trigger based on tags like `vip_customer`
- Attempted SLA-style automation (limited due to trial version)

### 🧩 Macros
- Refund approved response
- Internal escalation notes
- Tagging and status updates via macro

### 🏷 Tags Used
- `vip_customer`
- `event_cancelled`
- `solved_by_api`
- `refund_sent`

I also explored internal workflows, added internal notes, and adjusted conditions manually to mimic what an enterprise client might expect.

---

## 🔁 Part 2 – Zendesk API Integration (Postman)

This was the second half of the project, where I focused on working with the Zendesk API using Postman.

### 📁 Files Included

- `zendesk_api_collection.json` – My full Postman collection with all calls
- `zendesk_environment.json` – Optional environment setup (subdomain, token)
- `README.md` – This walkthrough

### ✅ What I Built in Postman

- `GET /tickets` – List all tickets
- `GET /search` – Search tickets by tag, subject, or priority
- `POST /tickets` – Create a ticket with tags, subject, and comment
- `PUT /tickets/{id}` – Update status, add tags, or add internal notes
- `DELETE /tickets/{id}` – Soft-delete a ticket
- `DELETE /deleted_tickets/{id}` – Attempted permanent delete (blocked in trial)

### 🧪 Internal Notes via API

Used the `public: false` flag in the body to simulate internal comments from agents or escalation notes.

---

## 🎯 Why I Did This

I wanted to combine my knowledge from working in frontline support with backend system logic — not just handling tickets but understanding how platforms like Zendesk are managed, automated, and integrated.

This repo shows that I can:
- Set up Zendesk workflows from scratch
- Handle common client configurations
- Work with the API to automate, update, and control ticket data
- Use Postman to test, iterate, and simulate support flows

---

## ⚙️ Tools Used

- Zendesk Support (Trial)
- Postman
- API Token Authentication
- GitHub

---

## 📜 License

MIT — Feel free to explore or reuse.

## 🔗 Live Zendesk Environment

This project was built using my trial Zendesk account:  
👉 [Access the Zendesk instance](https://noba-97645.zendesk.com) *(view access depends on login permissions)*
