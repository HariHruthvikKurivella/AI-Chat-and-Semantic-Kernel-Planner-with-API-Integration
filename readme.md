# AI Chat and Semantic Kernel Planner

AI-powered conversational application built with .NET 8, React, Microsoft Semantic Kernel, and Azure AI services. The system supports intelligent chat, semantic planning, contextual reasoning, and API integrations.

## Overview

This project provides a hybrid AI assistant that can operate in both cloud and local modes. It integrates Azure OpenAI with optional Bing Search, Azure AI Search, Cosmos DB, and Azure Storage Queue.

## Key Features

* AI-powered conversational chat
* Semantic Kernel based planning and reasoning
* Cloud and local execution modes
* REST API integration
* Plugin-based architecture
* Optional web and AI search
* Optional conversation storage
* Error handling and fallback support

## Technology Stack

| Category        | Technology                   |
| --------------- | ---------------------------- |
| Frontend        | React.js / Next.js           |
| Backend         | ASP.NET Core 8 Web API       |
| AI              | Azure OpenAI / OpenAI        |
| Semantic AI     | Microsoft Semantic Kernel    |
| Search          | Bing Search, Azure AI Search |
| Database        | Azure Cosmos DB              |
| Storage         | Azure Storage Queue          |
| API Testing     | Postman                      |
| Version Control | Git, GitHub                  |

## Architecture

```text
React Frontend
      |
      v
.NET 8 Web API
      |
      v
Semantic Kernel
      |
      +---- Azure OpenAI
      +---- Bing Search
      +---- Azure AI Search
      +---- Cosmos DB
      +---- Azure Storage Queue
```

## Project Structure

```text
copilotFullStackApp/
|
+-- backend/
|   +-- Controllers/
|   +-- StorageQueue/
|   +-- Dtos/
|   +-- Program.cs
|
+-- frontend/
    +-- src/
    +-- public/
    +-- package.json
```

## Local Setup

### Prerequisites

* .NET 8 SDK
* Node.js 18 or later
* Visual Studio 2022 or VS Code
* Git
* Chrome or Edge

### Clone Repository

```bash
git clone https://github.com/yourusername/copilotFullStackApp.git
cd copilotFullStackApp
```

### Backend

```bash
cd backend
dotnet restore
dotnet run
```

Backend URL:

```text
http://localhost:5124
```

### Frontend

```bash
cd frontend
npm install
npm start
```

Frontend URL:

```text
http://localhost:5173
```

## API

### Chat Endpoint

```http
POST http://localhost:5124/Chat
```

Request:

```json
{
  "userQuery": "Hello, how are you?"
}
```

Example response:

```json
{
  "assistantResponse": "I'm an AI assistant running locally!"
}
```

## Configuration

Cloud mode can use the following configuration values:

```text
OPENAI_KEY
OPENAI_ENDPOINT
OPENAI_CHAT_MODEL
BING_API_KEY
BING_ENDPOINT
COSMOS_DB_CONNECTION_STRING
STORAGE_CONNECTION_STRING
```

For local testing, cloud configuration can remain empty or use dummy values.

## Security

API keys and connection strings should not be hard-coded or committed to GitHub. Use environment variables, secure configuration, or Azure Key Vault for production environments.

## Future Enhancements

* Additional Semantic Kernel plugins
* Improved AI reasoning
* Real-time analytics
* GitHub Copilot extensions
* Production-ready SaaS deployment

## Project Summary

This project demonstrates the integration of conversational AI, semantic planning, Azure services, REST APIs, and a React frontend to build a flexible AI assistant that supports both local development and cloud-based deployment.
