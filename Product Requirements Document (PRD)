🛠 Product Requirements Document (PRD)
Focus: The "How" and the technical specifications.

1. Target User
Hungry customers who prefer messaging over calling or using a dedicated third-party delivery app.

2. User Stories

As a user, I want to ask if the restaurant is open so I don't waste time.

As a user, I want to place an order in plain English and have the bot understand me.

As a manager, I want the inventory to update automatically so I know when to reorder supplies.

3. Functional Requirements

NLP Engine: Utilize Google Gemini API to identify "Intent" (Ordering, FAQ, or Greeting).

Inventory Logic: * Query Google Sheets for Current_Stock.

If Order_Qty > Current_Stock, trigger "Out of Stock" message.

If Order_Qty <= Current_Stock, proceed and subtract.

Trigger: Webhook integration with WhatsApp Business API to initiate n8n workflow on "Message Received."

4. Technical Stack

Logic Engine: n8n (Self-hosted or Cloud).

Brain: Google Gemini API (via HTTP Request or AI Node).

Database: Google Sheets.

Interface: WhatsApp. 

5. Success Metrics

Resolution Rate: Percentage of chats completed without human intervention.

Inventory Accuracy: Zero discrepancy between physical stock and Google Sheets log.
