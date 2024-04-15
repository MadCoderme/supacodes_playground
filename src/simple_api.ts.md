## 📝 Table of Contents

- [Overview](#overview)
- [Endpoints](#endpoints)
    - [Welcome Message](#welcome-message)
    - [Get Users](#get-users)
- [System Requirements](#system-requirements)
- [Example Usage](#example-usage)

## 🧐 Overview

This document provides a comprehensive overview of the simple TypeScript Express API, outlining its endpoints, functionality, and system requirements.

## 🕹️ Endpoints

### 欢迎 Welcome Message 🫂

**Endpoint:** `/`

**Method:** GET

**Description:** Serves a welcome message to the API.

**Response:**

```json
{
  "message": "Welcome to the simple TypeScript Express API!"
}
```

### 👤 Get Users

**Endpoint:** `/users`

**Method:** GET

**Description:** Retrieves a list of users from the API.

**Response:**

```json
[
  {
    "id": 1,
    "name": "John Doe"
  },
  {
    "id": 2,
    "name": "Peter Parker"
  }
]
```

## ⚙️ System Requirements

The API requires the following system requirements:

- Node.js 12+
- npm or yarn

## 💻 Example Usage

```typescript
// Import the necessary modules
import axios from 'axios';

// Create an instance of the API client
const client = axios.create({
  baseURL: 'http://localhost:3000',
});

// Send a GET request to the welcome message endpoint
const welcomeMessageResponse = await client.get('/');
console.log(welcomeMessageResponse.data);

// Send a GET request to the users endpoint
const usersResponse = await client.get('/users');
console.log(usersResponse.data);
```