# Customer Support Chatbot (n8n + Google Sheets)

An automated customer support chatbot workflow built using n8n, designed to handle customer inquiries, manage orders, and process refunds and cancellations based on predefined business rules.

The system integrates with a Google Sheets database to store and retrieve customer and order information, and uses a JSON workflow file that can be directly imported into n8n.

# Features

💬 Handles customer inquiries automatically  
📦 Retrieves and manages order details  
🔁 Processes order cancellations  
💸 Handles refund requests based on business rules  
📊 Uses Google Sheets as a lightweight database  
⚙️ Fully automated workflow using n8n  
📁 Easily importable JSON workflow file

# Tech Stack

n8n – Workflow automation tool  
Google Sheets API – Database for customers and orders  
JSON Workflow File – Prebuilt automation logic  
Webhook Trigger – Entry point for chatbot requests

# Project Structure

/repo-root
│── chatbot-workflow.json   # n8n workflow export file  
│── README.md               # Project documentation

# Setup Instructions

### 1. Import Workflow into n8n
Open your n8n dashboard  
Click on Import Workflow  
Upload the chatbot-workflow.json file from this repository

### 2. Configure Google Sheets
Create a Google Sheet with:  
Customer details (Name, ID, Email, etc.)  
Order details (Order ID, Status, Amount, etc.)  
Connect your Google Sheets account in n8n using credentials

### 3. Set Up Webhook
Activate the workflow  
Copy the generated webhook URL  
Use it as the chatbot endpoint  

# How It Works
Customer sends a request (chat message)  
Webhook receives input in n8n  
Workflow processes intent:  
Order inquiry → fetch from Google Sheets  
Cancellation → validate & update status  
Refund → apply business logic  
Response is returned to the customer  

# Example Use Cases
“Where is my order?”  
“I want to cancel my order”  
“Request a refund”  
“Check order status”  

# Notes
Ensure Google Sheets permissions are properly configured  
Secure webhook endpoints before production use  
Add authentication layer if exposing publicly  


