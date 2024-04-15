## Table of Contents 🔗

1.  Overview 💡
2.  Setup and Usage ⚙️
3.  Event Handlers 🤖
    - on_ready 🟢
    - on_message 💬

## 1. Overview 💡

This Python script is a simple Discord bot that demonstrates the integration of a bot to the Discord platform.

## 2. Setup and Usage ⚙️

### **Prerequisites:**
- Python 3.6 or later
- discord.py library
- dotenv library

### **Setup:**
1. Create a Discord bot and obtain the **TOKEN** from the Discord Developer Portal.
2. Create a `.env` file in the same directory as this script.
3. Add the following line to the `.env` file:
```
DISCORD_TOKEN=[YOUR_BOT_TOKEN]
```
4. Install the required libraries using pip:
```bash
pip install discord dotenv
```

### **Usage:**
To run the bot, simply run the following command:
```bash
python main.py
```

## 3. Event Handlers 🤖

The bot defines event handlers to respond to specific events that occur on the Discord server. Here's a summary of the event handlers included in this script:

### **on_ready 🟢**

The `on_ready` event handler is triggered when the bot has successfully connected to the Discord server. It prints a confirmation message to the console.

### **on_message 💬**

The `on_message` event handler listens for incoming messages on the Discord server. It checks if the message starts with the command `!hello`, and if so, it responds with the message `Hi there!`.

**Example Usage:**
To send a message to the Discord server using the bot, follow these steps:
1. Open Discord and go to the server where the bot is connected.
2. Type the following message:
```
!hello
```
3. The bot will respond with the message:
```
Hi there!
```