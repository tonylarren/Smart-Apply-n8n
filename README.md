# Smart-Apply-n8n

# Job Scraper & Automation Workflow

## Description
This workflow automatically collects remote job postings, filters them to keep only relevant and new opportunities, sends notifications via email, and can generate motivation letters automatically. It helps streamline the process of discovering and applying to positions with minimal manual effort.  

## Features
- Fetches jobs from multiple sources  
- Filters out previously seen jobs to avoid duplicates  
- Sends email notifications with job details and direct application links  
- Optionally triggers automated motivation letter creation  

## Technologies Used
- **n8n**: workflow automation  
- **HTTP Request**: for fetching job data from APIs  
- **Supabase**: for storing and checking previously notified jobs  
- **SMTP / Gmail node/ Discord bot**: for sending email notifications


## Workflow Steps
1. **Trigger**: Scheduled or manual to fetch new jobs  
2. **Fetch Jobs**: Pulls data from APIs or web sources  
3. **Filter**: Compares with Supabase database to exclude already notified jobs  
4. **Email Notification**: Sends a styled email with new job postings
5. **Discord Notification**: Sends notifications in your own channel or dm
6. **Motivation Letter**: Optional step to generate a letter via webhook  

## Setup
1. Import the workflow into **n8n**.  
2. Configure the **Supabase credentials** for storing jobs.  
3. Configure the **SMTP or Gmail node** with your email settings.  
4. Set up a **schedule trigger** if you want automatic updates.
5. Set up discord with your credentials
6. Configure the **Google Docs node** with your API credentials. 
 

## Email Template
- Each job includes title, company, and a direct “Apply Here” link.  
- A button can trigger the motivation letter generation via a webhook.  

## Notes
- Make sure your email provider allows SMTP or API access.  
- Keep your Supabase database updated to prevent duplicate notifications.  
- Customize job filters based on your preferred tags or technologies.
- Still so much to improve

## Coming Soon
- **Relevant data sources**: Getting data from popular job board
- **CV Generation**: Automatically create tailored CVs for each application.  
- **Enhanced Motivation Letters**: Smarter templates and personalized content based on job description.  
- **Additional Notification Channels**: Slack, Telegram, or other integrations for job alerts. 
