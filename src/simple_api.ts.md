## 📑 Table of Contents

*   [Overview](#-overview)
*   [Modules and Imports](#-modules-and-imports)
*   [Application Setup](#-application-setup)
*   [Data Definition](#-data-definition)
*   [Endpoints](#-endpoints)
    *   [Welcome Message](#-welcome-message)
    *   [Get Users](#-get-users)
*   [Server啟動](#-server啟動)

## 🧭 Overview

This code establishes a basic TypeScript Express API with functionalities like displaying a welcome message, retrieving a list of users, and listening for incoming requests.

## 🧱 Modules and Imports

The code imports the `express` module from 'express' and creates an application instance. It also defines the port for the API.

```typescript
import express, { Application, Request, Response } from 'express';

const app: Application = express();
const port = process.env.PORT || 3000;
```

## ⚙️ Application Setup

No code in this section.

## 💽 Data Definition

The code includes a sample list of users for demonstration purposes. In a real-world application, this data would likely be stored in a database.

```typescript
// Define a list of users
const users = [
  { id: 1, name: 'John Doe' },
  { id: 2, name: 'Peter Parker' },
];
```

## 🗺️ Endpoints

### 🏡 Welcome Message

```typescript
app.get('/', (req: Request, res: Response) => {
  res.send('Welcome to the simple TypeScript Express API!');
});
```

*   **Route:** `/`
*   **Method:** GET
*   **Description:** Displays a welcome message.

### 👥 Get Users

```typescript
app.get('/users', (req: Request, res: Response) => {
  res.json(users);
});
```

*   **Route:** `/users`
*   **Method:** GET
*   **Description:** Retrieves the list of users.

## 🎧 Server Startup

```typescript
app.listen(port, () => {
  console.log(`Server is listening on port ${port}`);
});
```

*   **Port:** The server listens on the specified port (default: 3000) for incoming requests.
*   **Callback:** The server logs a message indicating it's listening on the chosen port.