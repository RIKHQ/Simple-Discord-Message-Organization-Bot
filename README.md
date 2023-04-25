# Simple-Discord-Message-Organization-Bot
This code is a simple Discord bot written in Python using the discord.py library. The bot listens for messages in a Discord channel and organizes numerical messages when it receives the "!organize" command.

Here's a breakdown of the code:

Import the required libraries: discord and discord.ext.commands.
Set up the Intents object to allow the bot to receive message events.
Create a bot instance with a command prefix '!' and the defined intents.
Define the 'on_ready' event function, which is called when the bot is logged in and ready.
Define the 'on_message' event function, which is called whenever a message is sent in a channel the bot has access to.
If the message is from the bot itself, the function returns immediately.
If the message starts with '!organize', call the 'organize_messages' function with the message's channel as an argument and send the result back to the channel.
Define the 'organize_messages' function that takes a channel as an argument:
Initialize an empty list to store numerical messages.
Iterate through the last 100 messages in the channel asynchronously.
Try to convert the message content to a float. If successful, append it to the 'messages' list. If not, ignore the message and move on to the next one.
Sort the numerical messages in ascending order.
Join the sorted messages into a single string, with each number on a new line, and return this string.
Finally, run the bot using the 'YOUR_BOT_TOKEN' placeholder, which should be replaced with your actual bot token.
When you run this code with a valid bot token, the bot will join your Discord server, and you can use the "!organize" command to sort any numerical messages in the channel the command is sent from.

#Written with Ai assistance.
