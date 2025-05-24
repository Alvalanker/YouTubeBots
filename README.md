YouTubeChatBot
A Python-based YouTube live stream chatbot that posts automated messages to a specified live stream's chat, built as a class project to demonstrate API integration and automation.
Overview
This project creates a chatbot that interacts with YouTube live stream chats using the YouTube Data API v3. The bot authenticates via OAuth 2.0, posts an initial message ("heyyy") upon joining, and sends random messages (e.g., "lol", "OMG", "LFG!!!") every 2–3 minutes. It can post to any public YouTube live stream with an active chat, making it versatile for testing or engagement.
Features

Posts an initial greeting ("heyyy") when joining a live stream chat.
Sends random, music-themed messages (e.g., "This riff is FIRE!", "Keep rocking it, Alvalanker!") every 2–3 minutes.
Uses asynchronous programming (asyncio) for efficient message scheduling.
Authenticates securely with Google OAuth 2.0.
Configurable for any public YouTube live stream by updating the STREAM_ID.

Prerequisites

Python 3.7+: Installed on your system.
Google Cloud Project: With YouTube Data API v3 enabled and OAuth 2.0 credentials.
YouTube Account: For authentication (must be added as a test user in the Google Cloud project).
Live Stream: A public YouTube live stream with chat enabled (can be your own or someone else’s).

Setup Instructions

Clone the Repository:
git clone https://github.com/your-username/YouTubeChatBot.git
cd YouTubeChatBot


Install Dependencies:Install required Python libraries using pip:
pip install google-auth-oauthlib google-api-python-client


Set Up Google Cloud Project:

Go to Google Cloud Console.
Create a new project (e.g., “YouTubeChatBot”).
Enable the YouTube Data API v3 in APIs & Services > Library.
Configure the OAuth consent screen:
Set to External.
Add the scope: https://www.googleapis.com/auth/youtube.force-ssl.
Add your Google account (e.g., your-email@gmail.com) as a test user under Test users.


Create an OAuth 2.0 Client ID:
Go to APIs & Services > Credentials.
Select Desktop app, name it (e.g., “Chatbot”), and create.
Download the JSON file (e.g., client_secret_xxx.json) and save it as client_secrets.json in the project folder.


Note: Do not commit client_secrets.json to GitHub. It’s included in .gitignore.


Configure the Script:

Open YouTubeV2.py in a text editor (e.g., Notepad, VS Code).
Update STREAM_ID with the video ID of the target live stream (e.g., xyz123 from https://www.youtube.com/watch?v=xyz123):STREAM_ID = "xyz123"


Ensure CLIENT_SECRETS_FILE matches your JSON filename (default: client_secrets.json).
Save the file with UTF-8 encoding.


Run the Bot:

In Command Prompt or terminal, navigate to the project folder:cd path/to/YouTubeChatBot


Run the script:python YouTubeV2.py


Log in with your Google account in the browser and authorize the app.



Usage

Start a Live Stream: Ensure the target stream is public, live, and has chat enabled. Use its video ID as the STREAM_ID.
Bot Behavior: The bot posts “heyyy” upon joining the chat and sends random messages every 2–3 minutes.
Monitor Output: Check Command Prompt for logs (e.g., “Posted: LFG!!!”) and the stream’s chat for messages.
Stop the Bot: Press Ctrl+C in Command Prompt to stop the script.

Project Structure
YouTubeChatBot/
├── YouTubeV2.py          # Main chatbot script
├── client_secrets.json   # OAuth credentials (not in repo, user-provided)
├── .gitignore            # Excludes sensitive files
└── README.md             # This file

Troubleshooting

Error: Stream not found:
Verify the STREAM_ID is correct and the stream is public, live, and has chat enabled.
Check YouTube Studio for the stream’s status.


ModuleNotFoundError:
Ensure google-auth-oauthlib and google-api-python-client are installed (pip install ...).


OAuth Errors:
Confirm your Google account is a test user in Google Cloud Console.
Re-download client_secrets.json if authentication fails.


Encoding Issues:
Save YouTubeV2.py with UTF-8 encoding using Notepad or VS Code.



Notes

This project was developed for a class to demonstrate API-based automation.
The bot complies with YouTube’s Terms of Service by posting non-spammy messages at a reasonable interval.
For ethical use, obtain permission from stream owners before posting in their chats.
Sensitive files (client_secrets.json) are excluded via .gitignore.

License
MIT License. See LICENSE for details.
Acknowledgments

Built with the YouTube Data API v3.
Inspired by the need to automate live stream interactions for educational purposes.

