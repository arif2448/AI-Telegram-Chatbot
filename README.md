# AI Telegram Chatbot

An AI-powered Telegram chatbot built with **n8n**, **Groq**, and **Tavily Search**. This project demonstrates how workflow automation can connect a Telegram bot to an AI agent, a language model, a web-search tool, and conversation memory.

## Project Highlights

- Receives messages through Telegram
- Uses an AI Agent to generate responses
- Connects to a Groq chat model
- Provides Tavily Search as a tool for current web information
- Uses the Telegram chat ID as the memory session key
- Sends the AI Agent's response back to the Telegram chat

## Tech Stack

- **n8n** – workflow automation
- **Telegram Bot API** – user messaging
- **Groq** – chat model provider
- **Tavily Search** – web-search tool

## Demo Examples

The following are example prompts to try with the bot. The responses below describe the expected behavior and are not recorded outputs from a live test.

### Demo 1: General question

**User prompt**

> What is artificial intelligence?

**Expected behavior**

The AI Agent generates an explanation of artificial intelligence and may include common examples and applications.

### Demo 2: Web search

**User prompt**

> Search for the latest AI news.

**Expected behavior**

The AI Agent can use the Tavily Search tool to retrieve relevant search results and summarize them, provided the tool and credentials are configured correctly.

### Demo 3: Follow-up question

**User prompt**

> Explain Python.

**Follow-up prompt**

> Give me three examples of its uses.

**Expected behavior**

The workflow is configured with a memory node keyed by Telegram chat ID. Follow-up context depends on the memory node's configuration and successful execution.

## Workflow

1. A user sends a message to the Telegram bot.
2. The Telegram Trigger receives the message.
3. The AI Agent processes the message with the Groq Chat Model.
4. The agent can call Tavily Search when appropriate.
5. The workflow sends the agent's output back to the Telegram chat.

## Screenshots and Demo

Add your own screenshots here to show the workflow and real bot responses.

Suggested screenshots:
- `screenshots/workflow.png` – the n8n workflow canvas
- `screenshots/telegram-demo-1.png` – a general question and response
- `screenshots/telegram-demo-2.png` – a web-search example

Only add screenshots after capturing them from your own workflow. Hide bot tokens, API keys, personal chat details, and other private information before publishing.

## Project Files

- `ai-telegram-chatbot.json` – exported n8n workflow
- `README.md` – project overview and demo examples

## Notes

This repository is a project showcase. To run the workflow, import the JSON file into n8n and configure your own Telegram, Groq, and Tavily credentials. Imported credential references do not grant access to the original accounts.

The workflow instructions request Tavily Search for current facts and events, but successful searching depends on valid credentials and tool execution. Sample prompts in this README are demonstrations to try, not proof of a live test.

## Security

Do not publish API keys, Telegram bot tokens, passwords, or sensitive personal information. Review the exported workflow JSON and screenshots before making the repository public.
