## 📝 Table of Contents

*   [Overview](#の概要)
*   [Modules and Libraries](#ライブラリとモジュール)
*   [Environment Variables](#環境変数)
*   [Client Initialization](#クライアントの初期化)
    *   [on_ready Event](#on_readyイベント)
    *   [on_message Event](#on_messageイベント)

##の概要
This Python script establishes a basic Discord bot functionality using the Discord API. It imports necessary modules, loads environment variables, creates a Discord client, and defines event handlers for when the bot connects to Discord and receives messages.

## ライブラリとモジュール
*   **os**: Provides operating system functionality.
*   **discord**: Enables interaction with the Discord API.
*   **dotenv**: Facilitates loading environment variables from a .env file.

## 環境変数
*   **DISCORD_TOKEN**: Stores the bot's access token to connect to Discord.

## クライアントの初期化
```python
client = discord.Client()
```

This line creates a Discord client object named client.

### on_ready Event
```python
@client.event
async def on_ready():
    print(f'{client.user} has connected to Discord!')
```
*   The @client.event decorator registers the function as an event listener for the on_ready event.
*   The async keyword indicates that the function will run asynchronously, allowing other parts of the program to run concurrently.
*   The function prints a message to the console indicating that the bot has successfully connected to Discord.

### on_message Event
```python
@client.event
async def on_message(message):
    if message.author == client.user:
        return

    if message.content.startswith('!hello'):
        await message.channel.send('Hi there!')
```
*   The @client.event decorator registers the function as an event listener for the on_message event.
*   The if statement checks if the message was sent by the bot itself (client.user) and returns if true, preventing the bot from responding to its own messages.
*   The second if statement checks if the message content starts with the "!hello" command. If true, it sends a "Hi there!" response to the channel where the message was received using await message.channel.send('Hi there!').

## 🏃‍♀️ Running the Bot
```python
client.run(TOKEN)
```
*   The client.run(TOKEN) statement starts the bot and keeps it running until manually stopped or an error occurs. It passes the bot's access token (stored in the DISCORD_TOKEN environment variable) as an argument for authentication.