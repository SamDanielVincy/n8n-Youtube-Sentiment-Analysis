# 🎯 Real-Time YouTube Sentiment Analysis using AI & Automation

> **An end-to-end, production-style AI automation pipeline that fetches live YouTube comments, classifies sentiment using GPT-4o Mini, stores structured data in Google Sheets, and visualizes emotions in real time.**

---

## 🚀 Project Overview

This project demonstrates how **AI, workflow automation, and data visualization** can be combined to build a **scalable, real-time sentiment analysis system** for YouTube comments. The system continuously monitors video comments, processes and cleans them, applies AI-based sentiment classification, and updates a live dashboard for instant emotional insights.

## 🎥 Live Demo



https://github.com/user-attachments/assets/9fc6edf2-ff97-44ea-a4e1-3474cafd4e7b


### 🔍 Use Cases

* 📢 **Brand Monitoring** – Track audience sentiment on product or campaign videos
* 🧑‍💻 **Customer Feedback Analysis** – Understand viewer reactions in real time
* 📊 **Content Performance Analytics** – Measure emotional impact of content
* 🏗️ **AI Automation Pipelines** – Demonstrates no-code/low-code AI system design

---

## 🧠 System Architecture

<img width="1536" height="1024" alt="Architecture Sentiment n8n" src="https://github.com/user-attachments/assets/c2626413-2e44-4825-aac5-6302cdf1b200" />


## ⚙️ Tech Stack

| Technology             | Purpose                             |
| ---------------------- | ----------------------------------- |
| **n8n**                | Workflow automation & orchestration |
| **OpenAI GPT-4o Mini** | NLP & sentiment classification      |
| **YouTube Data API**   | Fetch video comments                |
| **Google Sheets API**  | Store structured results            |
| **Dashboard / Charts** | Visualize sentiment distribution    |
| **HTTP Requests**      | API communication                   |

---

## ✨ Features

* 🔄 **Real-Time Comment Fetching**
* 🧠 **AI-Powered Sentiment Analysis** (Positive | Neutral | Negative)
* 📊 **Live Visualization Dashboard**
* 📁 **Cloud-Based Data Storage**
* 🧩 **Modular Workflow Design** (Easy to extend)
* ⚡ **Low-Code / No-Code AI Automation**



---

## 🛠️ Setup & Installation

### 🔹 Prerequisites

Make sure you have:

* ✅ **n8n** (Cloud or Self-Hosted)
* ✅ **OpenAI API Key** (GPT-4o Mini access)
* ✅ **Google Cloud Account**
* ✅ **YouTube Data API Key**
* ✅ Google Sheets

---

## 🔐 API Setup Guide

### 1️⃣ YouTube Data API

1. Go to: [https://console.cloud.google.com](https://console.cloud.google.com)
2. Create a new project
3. Enable **YouTube Data API v3**
4. Generate an **API Key**

---

### 2️⃣ OpenAI API (GPT-4o Mini)

1. Visit: [https://platform.openai.com](https://platform.openai.com)
2. Generate an API key
3. Store it securely

---

### 3️⃣ Google Sheets API

1. Go to **Google Cloud Console**
2. Enable **Google Sheets API**
3. Create **Service Account Credentials**
4. Download the JSON key file
5. Share your Google Sheet with the service account email

---

## 📦 Environment Configuration

Create a `.env` file in the root directory:

```env
OPENAI_API_KEY=your_openai_api_key
YOUTUBE_API_KEY=your_youtube_api_key
GOOGLE_SHEETS_ID=your_google_sheet_id
GOOGLE_SERVICE_ACCOUNT=path_to_credentials.json
```

---

## 🔄 n8n Workflow Setup

### Step 1 — Install n8n

#### Option A: n8n Cloud

* Visit: [https://n8n.io](https://n8n.io)
* Create an account

#### Option B: Docker (Self-Hosted)

```bash
docker run -it --rm \
  -p 5678:5678 \
  -v ~/.n8n:/home/node/.n8n \
  n8nio/n8n
```

---

### Step 2 — Import Workflow

1. Open n8n Dashboard
2. Click **Import Workflow**
3. Upload `workflows/n8n_workflow.json`

---

### Step 3 — Configure Credentials

In n8n, add:

* 🔑 **HTTP Credentials** (YouTube API Key)
* 🧠 **OpenAI Credentials** (GPT-4o Mini)
* 📊 **Google Sheets Credentials** (Service Account JSON)

---

## 🔁 Workflow Breakdown

| Node                  | Description                      |
| --------------------- | -------------------------------- |
| **YouTube Get Video** | Fetches video metadata           |
| **HTTP Request**      | Retrieves video comments         |
| **Split Out**         | Separates each comment           |
| **Edit Fields**       | Extracts username & text         |
| **AI Agent**          | Sends text to GPT-4o Mini        |
| **Merge Node**        | Combines AI output with metadata |
| **Append Row**        | Stores results in Google Sheets  |

---

## 📊 Dashboard Setup

You can visualize sentiment distribution using:

### Option 1 — Google Sheets Chart

1. Open your Google Sheet
2. Select sentiment column
3. Click **Insert → Chart**
4. Choose **Pie Chart**

### Option 2 — External Dashboard

* Google Looker Studio
* Power BI
* Tableau

---

## ▶️ How to Run

1. Open n8n
2. Enter a **YouTube Video ID**
3. Click **Execute Workflow**
4. Watch data flow into Google Sheets
5. View live sentiment updates on dashboard

---

## 🧪 Sample Output

| Username | Comment                | Sentiment |
| -------- | ---------------------- | --------- |
| user_01  | This video is amazing! | Positive  |
| user_02  | Not very helpful       | Negative  |
| user_03  | Thanks for sharing     | Neutral   |

---

## 🔒 Security Best Practices

* ❌ Never commit API keys
* ✅ Use `.env` for secrets
* 🔐 Restrict API key usage by domain/IP

---

## 🛣️ Roadmap

* [ ] Multi-language sentiment support
* [ ] Emotion detection (Happy, Angry, Excited, Sad)
* [ ] Real-time alerts via Slack/Email
* [ ] Cloud database integration (Firebase / PostgreSQL)
* [ ] Web-based dashboard (React / Streamlit)

---

## 🤝 Contributing

Contributions are welcome!

1. Fork the repo
2. Create a feature branch
3. Commit changes
4. Open a Pull Request

---

## 🏷️ License

This project is licensed under the **MIT License**.

---

## 👨‍💻 Author

**Sam Vincy**
B.Tech AI & Data Science | AI Automation | Python Developer

🔗 LinkedIn: [https://www.linkedin.com/in/sam-daniel-vincy/](https://www.linkedin.com/in/sam-daniel-vincy/)
📧 Email: [samdanielvincy1029@gmail.com](mailto:samdanielvincy1029@gmail.com)

---

## ⭐ Support

If you found this project helpful, please consider giving it a **star ⭐** and sharing it with the community!

---

