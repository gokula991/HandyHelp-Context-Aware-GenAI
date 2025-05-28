HandyHelp — Context-Aware Generative AI Support Agent

![Description of image](https://github.com/gokula991/HandyHelp-Context-Aware-GenAI/blob/main/Cover_Pic_GenAi_agent.png?raw=true)



Welcome to HandyHelp, a conversational AI support agent designed to deliver relevant, context-aware assistance by combining Generative AI, custom retrieval logic, and smart fallback strategies — all orchestrated within the Google Conversational Agent ecosystem.

Features

Generative AI Responses: Uses Google Dialogflow CX + GenAI to generate contextually relevant answers grounded in domain data.
Human Escalation: Smoothly escalates conversations to human agents when needed, with query logging.
Structured FAQs: Supports task-specific playbooks for product and service FAQs.
Retrieval Augmented Generation (RAG): Custom payloads simulate RAG-style grounding by referencing internal documents like PDFs and knowledge bases.
Live Fallback Search: Integrates Google Cloud Run + Custom Search API for real-time web fallback when internal knowledge is insufficient.
Multimodal Interaction: Supports chat and voice via Google’s Conversational Phone Gateway.
OpenAPI Spec: Defines scalable endpoint interactions for flexible integration.
Clean, Export-Ready Project: Designed for GitHub version control and easy collaboration.
Tech Stack & Architecture

Google Dialogflow CX with Generative AI integration
Google Cloud Run (for fallback API hosting)
Google Custom Search API (for live search fallback)
OpenAPI (YAML/JSON) for API endpoint definitions
Google Conversational Phone Gateway (voice interactions)
Setup & Usage Instructions

Follow these steps to set up and run the HandyHelp agent:

1. Clone the repository
git clone ---repo--name--
cd handyhelp
2. Configure Google Cloud APIs
Enable Dialogflow CX in your Google Cloud project.
Enable Google Custom Search API and create an API key.
Set up a Custom Search Engine (CSE) in Google Custom Search Console to search the web or specific sites.
Enable Cloud Run API.
3. Deploy Cloud Run Service
Implement your fallback search service (e.g., a serverless app that queries Google Custom Search API).
Deploy this service on Cloud Run.
Note the service URL — this will be called by Dialogflow CX fallback logic.
4. Set Up Dialogflow CX Agent
Import the Dialogflow CX agent project (provided in this repo or exported from Agent Studio).
In your agent workspace, configure:
GenAI integration for response generation.
Custom payloads to incorporate reference documents and context for RAG-style grounding.
Webhook or Fulfillment to connect to your Cloud Run fallback service URL.
API key as a tool: Add the Google Custom Search API key in the agent’s environment variables or secure config for the fallback mechanism.
5. Configure Conversational Phone Gateway
Set up Google’s Conversational Phone Gateway integration to enable voice interactions.
Connect the Phone Gateway number to your Dialogflow CX agent.
6. Test and Customize
Test your agent in Dialogflow CX simulator for chat and voice.
Customize FAQs, playbooks, and retrieval sources as needed.
Extend the OpenAPI spec to add or modify endpoints for your agent interactions.


Here’s a snapshot of the agent’s flow and GenAI integration in Dialogflow CX:

Open For Contributions and more than welcome.

Contact & Connect

Feel free to reach out for collaborations, discussions, or inquiries:

Email: gokulachandra119@gmail.com
LinkedIn: https://linkedin.com/in/gokulachandra


Tags

Generative AI, Conversational AI, Dialogflow CX, Google Cloud, RAG, OpenAPI, Voice AI, Cloud Run, AI Engineering, Machine Learning, Data Science
