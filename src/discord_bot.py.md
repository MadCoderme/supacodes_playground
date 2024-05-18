## 🤖 Discord Bot Documentation

### 📑 Table of Contents

*   [Imports](#-import-statements)
*   [Environment Variables](#-environment-variables)
*   [Client Initialization](#-client-initialization)
*   [Event Listeners](#-event-listeners)
    *   [onReady](#-onready-event)
    *   [onMessage](#-onmessage-event)

---

### 📥 Import Statements

```python
import os
import discord
from dotenv import load_dotenv
```

*   `os`: Provides operating system functionality.
*   `discord`: Core library for creating Discord bots.
*   `dotenv`: Facilitates loading environment variables from a file.
```python
load_dotenv()  # Load environment variables from .env
```

*   Loads values from a `.env` file into Python's `os.environ` dictionary, making them accessible throughout the script.

### 🔑 Environment Variables

```python
TOKEN = os.getenv('DISCORD_TOKEN')
```

*   Stores the Discord bot's authentication token.

### 🤖 Client Initialization

```python
client = discord.Client()
```

*   Creates a `discord.Client` object representing the bot.

### 🎧 Event Listeners

#### onReady 🔈

```python
@client.event  # Decorator to mark a function as an event listener
async def on_ready():
    print(f'{client.user} has connected to Discord!')
```

*   **Event Trigger:** When the bot successfully connects to the Discord server.
*   *   Prints a message to the console indicating the bot's username and that it has connected.

#### onMessage 💬

```python
@client.event  # Handles message events
async def on_message(message):
    if message.author == client.user:  # Don't respond to itself
        return

    if message.content.startswith('!hello'):  # Check for the command
        await message.channel.send('Hi there!')
```

*   **Event Trigger:** When a message is received in any channel the bot has access to.
*   *   Checks if the message was sent by the bot itself (to avoid infinite loops).
*   *   Looks for messages starting with the `!hello` command.
*   *   Responds with a friendly greeting.

### 🏃‍♀️ Running the Bot

```python
client.run(TOKEN)  # Starts the bot
```

*   *   Attempts to connect the bot to the Discord server using the provided token.