# AI-Powered Restaurant Order & Inventory Engine 🍔

DineBot is an end-to-end automation solution built with **n8n** that transforms a standard WhatsApp chat into a fully functional restaurant management system. By leveraging **Google Gemini AI**, it handles natural language ordering, customer FAQs, and real-time inventory synchronization via **Google Sheets**.

---

## 🚀 Overview

The goal of this project was to eliminate manual order entry and provide 24/7 customer support without human intervention. The system doesn't just "chat"—it executes business logic by checking stock levels and updating databases in real-time.

### Key Features
* **NLP Ordering:** Customers can place orders using natural language (e.g., "Can I get two spicy chicken burgers and a Coke?").
* **Instant FAQ:** Automated responses for restaurant hours, location, and menu details using Google Gemini.
* **Live Inventory Management:** Automatically checks Google Sheets for stock availability and deducts items upon successful ordering.
* **WhatsApp Integration:** A familiar, frictionless interface for the end-user.

---

## 🛠️ Tech Stack

* **Workflow Orchestration:** [n8n](https://n8n.io/)
* **Artificial Intelligence:** Google Gemini API (LLM)
* **Database/Storage:** Google Sheets
* **Communication:** WhatsApp Business API (via Webhooks)
* **Logic:** JavaScript (within n8n nodes)

---

## 🏗️ System Architecture

1.  **Trigger:** User sends a message via WhatsApp.
2.  **Processing:** n8n receives the webhook and sends the text to **Google Gemini**.
3.  **Intent Classification:** Gemini determines if the user is asking a question or placing an order.
4.  **Validation:** If it's an order, the system queries **Google Sheets** to verify stock.
5.  **Execution:** * If in stock: Updates sheet (Inventory - 1), logs the order, and sends confirmation.
    * If out of stock: Informs the user and suggests alternatives.
6.  **Response:** The final output is sent back to the user via WhatsApp.

---

## 📋 Documentation

I have included the formal business and product documentation for this project:

* [Business Requirements Document (BRD)](./Business Requirements Document (BRD).md)
* [Product Requirements Document (PRD)](./Product Requirements Document (PRD).md)

---

## 🔧 Setup & Installation

1.  **n8n Setup:** Import the provided JSON workflow into your n8n instance.
2.  **API Keys:** * Add your `GEMINI_API_KEY` to the AI node.
    * Configure your WhatsApp Business API credentials.
3.  **Database:** Create a Google Sheet with headers: `Item_Name`, `Stock_Level`, `Price`, and `Orders`.
4.  **Environment Variables:** Set up the credentials in n8n for Google Sheets and WhatsApp.

---

## 📈 Impact
* **100% Automation** of the ordering pipeline.
* **Zero Latency** in inventory updates.
* **Reduced Overhead** by automating basic customer service queries.
