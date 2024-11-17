# BreakoutAI.tech
The Breakout AI Assessment is an AI-driven project focused on building an intelligent system for real-time data analysis and decision-making. It includes machine learning model development, real-time processing, and an interactive interface, demonstrating how AI can automate tasks and provide valuable insights.

# Custom Email Sender
## Overview
The Custom Email Sender is an intelligent email automation tool that reads data from a CSV file or Google Sheets, extracts specific information, and sends personalized emails to each contact. Users can upload their files, specify email templates with placeholders (such as names, email addresses, etc.), and the system will automatically send emails with the required details. This project includes a simple dashboard for users to upload files, define email templates, and view the status of sent emails.

## Features
File Upload & Google Sheets Integration: Users can upload CSV files or connect directly to Google Sheets, select a column with contact details (e.g., names, email addresses), and preview the data.
Custom Email Template Input: Users can create custom email templates with placeholders (e.g., "Hello {name}, your order is ready for pickup at {address}").
Automated Email Sending: The tool automatically sends emails to each contact by filling in the placeholders with data from the selected column.
Email Delivery Status: Track the status of emails sent, including any failed deliveries or errors.
Data Display & Download: View the email sending results, and download the status report as a CSV file or update the information in Google Sheets.

## Setup Instructions

1. Clone the Repository
   ```bash
   git clone https://github.com/rimo02/BreakoutAI.tech-Assignment.git
   ```

2. Create a Virtual Environment
   ```bash
   python -m venv venv
   ```

3. Activate the Virtual Environment
   - On Windows:
     ```bash
     venv\Scripts\activate
     ```
   - On macOS and Linux:
     ```bash
     source venv/bin/activate
     ```

4. Install Dependencies
   ```bash
   pip install -r requirements.txt
   ```

5. Set Up Environment Variables
   - Create a `.env` file in the root directory.
   - Add the following details:
     ```plaintext
     SEARCH_API_KEY=<Your serp  API Key>
     GROQ_API_KEY=<Your LLM API Key>
     MAX_REQUESTS=10  # Set request limit to handle rate limiting. This represents the maximum value of requests you can make to the agent before getting the desired output.
     ```
 6. Go to [Google Cloud Console](https://console.cloud.google.com).
   - Create a new project and navigae to API and Services
   -  Search for Google Sheets API and click enable to enable it.
   -  Go to API & Services > Credentials. Click Create Credentials and select Service account. Fill Service account details. For role select Editor > Done
   -  Go to Credentials > Add Key > Create New Key. Select JSON as the key type.
   -  Download  it in the same directory of the project.

## Usage Guide
1. Running the Application
   ```bash
   streamlit run app.py
   ```

2. Using the Dashboard
   - Upload a CSV or connect to Google Sheets by entering credentials.
   - Choose the primary column with entities (e.g., companies) for information retrieval.
   - Enter a custom query with placeholders, like “Get the address of {company}.”
   - View the extracted information, and download it as a CSV or update Google Sheets.

## API Keys and Environment Variables
Add the required API keys for web search (e.g., SerpAPI, ScraperAPI) and the LLM (e.g., Groq or OpenAI). These should be stored securely in the `.env` file as shown above.

## Optional Features
This project includes:
- Advanced Query Templates: Extract multiple fields in a single prompt, e.g., “Get the email and address for {company}.”

## Loom Video Walkthrough
For a quick overview, check out the [video walkthrough](https://www.loom.com/share/2ba192aa81d849369b8df693fc91f9a8?sid=942791d2-3bd1-47b7-a8c6-be3dbdcfbe21) of the project.


