---
title: Authorization
description: Learn how to authorize access to the Uganda Data Project API.
weight: 3
---

## Authorization

The Uganda Data Project API utilizes API keys for authorization, ensuring secure access to its services. To interact with the API, users must possess valid API credentials, which can be generated from the "API Keys" section within their Uganda Data Project account.

### API Key Authorization

API Key Authorization involves including a unique API key in the HTTP headers of the API request. The Uganda Data Project API utilizes this method to authenticate and authorize users.

### Generating API Key

Follow these steps to generate an API key:

1. **Log in to Your Uganda Data Project Account:**

   - Visit [uganda.rapharm.shop](https://uganda.rapharm.shop) and log in to your Uganda Data Project account.

2. **Navigate to API Keys:**

   - In your account profile settings, find the "API Keys" section. This is where you can generate and manage your API keys.

3. **Generate API Key:**

   - Inside the "API Keys" section, find an option to generate a new API key. Click on this option to create a unique key for API access.

4. **Copy Your API Key:**
   - Once generated, copy your API key. This key serves as your authentication token.

### Using API Key

To make API requests, include your API key in the HTTP headers of your requests. Here is an example using the `curl` command-line tool:

```bash
curl -H "Authorization: Bearer YOUR_API_KEY" https://api.uganda-data-project.com/v1/endpoint
```
