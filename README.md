# 📰 Article-Summary-Web-Scraper

This project is an **automated workflow built with n8n** that scrapes articles, summarizes them with AI, and sends the results by email. It is designed to streamline the process of reviewing multiple articles and sharing concise insights automatically.  

---

## 🚀 Features
- **Scheduled Triggers**: The workflow runs automatically on a scheduled basis.  
- **Google Sheets Integration**:  
  - Reads article URLs and user emails from a Google Sheet.  
  - Skips rows where the `status` column is set to **done**.  
- **Web Scraping**:  
  - Makes HTTP requests to fetch article content.  
  - Processes raw HTML to extract only the relevant information.  
- **Parallel Processing**: Can handle more than one article at the same time.  
- **AI-Powered Summaries**:  
  - Uses **Groq LLaMA Chat Model** to generate a summary.  
  - Each summary contains **3 key topics**.  
- **Email Notifications**: Sends the summarized content directly to the email specified in the sheet.  
- **Status Update**: Once processed, the article’s row in the Google Sheet is updated to **done**, avoiding duplicate work.  

---

## 🛠️ Tools & Technologies
- [n8n](https://n8n.io/) – Workflow automation  
- Google Sheets API – Storage of article links, emails, and processing status  
- HTTP Request & HTML Parsing – Article scraping and cleaning  
- [Groq](https://groq.com/) – LLaMA Chat Model for AI summaries  
- Email Node – Automatic email delivery  

---

## 📂 Workflow Overview
1. **Trigger**: Scheduled start.  
2. **Check Articles**: Reads the list of URLs and emails from Google Sheets.  
3. **Scraping**: Performs HTTP requests to fetch and parse each article.  
4. **Processing**:  
   - Joins the text of each article.  
   - Sends it to the AI model for summarization.  
5. **Output**:  
   - Sends the 3-topic summary to the corresponding email.  
   - Updates the status column in Google Sheets to **done**.  

---

## 📹 Demo
A video demonstration of this workflow is available in the repository.  

---

## 📌 Use Cases
- Automated news curation  
- Research and academic paper summaries  
- Monitoring articles for business intelligence  
- Personalized digest creation  

---

## ⚡ Getting Started
1. Clone or download this repository.  
2. Open the workflow JSON file in **n8n**.  
3. Connect your credentials for:  
   - Google Sheets  
   - Groq LLaMA Model API  
   - Email service  
4. Update the Google Sheet with article links and recipient emails.  
5. Run or schedule the workflow.  

---

## 📜 License
This project is for **educational and portfolio purposes**.  
No proprietary or confidential data has been used.  
