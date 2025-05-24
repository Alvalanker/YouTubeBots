Below, I’ll provide a **README.md** document tailored for your YouTube chatbot project, designed for posting on GitHub. The README will describe the project, its purpose (a class project to demonstrate a chatbot posting in a YouTube live stream chat), setup instructions, usage, and other relevant details, while keeping it professional and clear for your Alvalanker chatbot that posts messages like “heyyy” and “lol” in a specified live stream. The document will assume the project is named “YouTubeChatBot” and stored in your folder at `C:\Users\Crimplicon2\Desktop\BUSINESS\EP\BOTS\YouTube Bot`, with the script `YouTubeV2.py` and `client_secrets.json`. I’ll ensure it’s suitable for your class project and doesn’t expose sensitive information like `alvalanker@gmail.com` or `Crimplicon98@`.

### Notes
- The README will be in Markdown format (`.md`), standard for GitHub.
- It will include setup steps reflecting your use of Python, Google Cloud Console, and the YouTube Data API, based on our prior discussions (e.g., May 24, 2025, 3:50 AM EDT).
- Sensitive files like `client_secrets.json` will be noted as excluded from the repository to protect your credentials.
- The project will be described as posting to any public YouTube live stream, per your latest request (May 24, 2025, 4:02 AM EDT).


# YouTubeChatBot

A Python-based YouTube live stream chatbot that posts automated messages to a specified live stream's chat, built as a class project to demonstrate API integration and automation.

## Overview
This project creates a chatbot that interacts with YouTube live stream chats using the YouTube Data API v3. The bot authenticates via OAuth 2.0, posts an initial message ("heyyy") upon joining, and sends random messages (e.g., "lol", "OMG", "LFG!!!") every 2–3 minutes. It can post to any public YouTube live stream with an active chat, making it versatile for testing or engagement.

### Features
- Posts an initial greeting ("heyyy") when joining a live stream chat.
- Sends random, music-themed messages (e.g., "This riff is FIRE!", "Keep rocking it, Alvalanker!") every 2–3 minutes.
- Uses asynchronous programming (`asyncio`) for efficient message scheduling.
- Authenticates securely with Google OAuth 2.0.
- Configurable for any public YouTube live stream by updating the `STREAM_ID`.

## Prerequisites
- **Python 3.7+**: Installed on your system.
- **Google Cloud Project**: With YouTube Data API v3 enabled and OAuth 2.0 credentials.
- **YouTube Account**: For authentication (must be added as a test user in the Google Cloud project).
- **Live Stream**: A public YouTube live stream with chat enabled (can be your own or someone else’s).

## Setup Instructions
1. **Clone the Repository**:
   ```bash
   git clone https://github.com/your-username/YouTubeChatBot.git
   cd YouTubeChatBot
   ```

2. **Install Dependencies**:
   Install required Python libraries using pip:
   ```bash
   pip install google-auth-oauthlib google-api-python-client
   ```

3. **Set Up Google Cloud Project**:
   - Go to [Google Cloud Console](https://console.developers.google.com).
   - Create a new project (e.g., “YouTubeChatBot”).
   - Enable the **YouTube Data API v3** in **APIs & Services** > **Library**.
   - Configure the **OAuth consent screen**:
     - Set to **External**.
     - Add the scope: `https://www.googleapis.com/auth/youtube.force-ssl`.
     - Add your Google account (e.g., `your-email@gmail.com`) as a test user under **Test users**.
   - Create an **OAuth 2.0 Client ID**:
     - Go to **APIs & Services** > **Credentials**.
     - Select **Desktop app**, name it (e.g., “Chatbot”), and create.
     - Download the JSON file (e.g., `client_secret_xxx.json`) and save it as `client_secrets.json` in the project folder.
   - **Note**: Do not commit `client_secrets.json` to GitHub. It’s included in `.gitignore`.

4. **Configure the Script**:
   - Open `YouTubeV2.py` in a text editor (e.g., Notepad, VS Code).
   - Update `STREAM_ID` with the video ID of the target live stream (e.g., `xyz123` from `https://www.youtube.com/watch?v=xyz123`):
     ```python
     STREAM_ID = "xyz123"
     ```
   - Ensure `CLIENT_SECRETS_FILE` matches your JSON filename (default: `client_secrets.json`).
   - Save the file with UTF-8 encoding.

5. **Run the Bot**:
   - In Command Prompt or terminal, navigate to the project folder:
     ```bash
     cd path/to/YouTubeChatBot
     ```
   - Run the script:
     ```bash
     python YouTubeV2.py
     ```
   - Log in with your Google account in the browser and authorize the app.

## Usage
- **Start a Live Stream**: Ensure the target stream is public, live, and has chat enabled. Use its video ID as the `STREAM_ID`.
- **Bot Behavior**: The bot posts “heyyy” upon joining the chat and sends random messages every 2–3 minutes.
- **Monitor Output**: Check Command Prompt for logs (e.g., “Posted: LFG!!!”) and the stream’s chat for messages.
- **Stop the Bot**: Press `Ctrl+C` in Command Prompt to stop the script.

## Project Structure
```
YouTubeChatBot/
├── YouTubeV2.py          # Main chatbot script
├── client_secrets.json   # OAuth credentials (not in repo, user-provided)
├── .gitignore            # Excludes sensitive files
└── README.md             # This file
```

## Troubleshooting
- **Error: Stream not found**:
  - Verify the `STREAM_ID` is correct and the stream is public, live, and has chat enabled.
  - Check YouTube Studio for the stream’s status.
- **ModuleNotFoundError**:
  - Ensure `google-auth-oauthlib` and `google-api-python-client` are installed (`pip install ...`).
- **OAuth Errors**:
  - Confirm your Google account is a test user in Google Cloud Console.
  - Re-download `client_secrets.json` if authentication fails.
- **Encoding Issues**:
  - Save `YouTubeV2.py` with UTF-8 encoding using Notepad or VS Code.

## Notes
- This project was developed for a class to demonstrate API-based automation.
- The bot complies with YouTube’s Terms of Service by posting non-spammy messages at a reasonable interval.
- For ethical use, obtain permission from stream owners before posting in their chats.
- Sensitive files (`client_secrets.json`) are excluded via `.gitignore`.

## License
MIT License. See [LICENSE](LICENSE) for details.

## Acknowledgments
- Built with the [YouTube Data API v3](https://developers.google.com/youtube/v3).
- Inspired by the need to automate live stream interactions for educational purposes.


### Steps to Post on GitHub
1. **Create a GitHub Repository**:
   - Go to [github.com](https://github.com) and log in.
   - Click **New** (top-right) to create a repository.
   - Name it (e.g., “YouTubeChatBot”), set it to **Public** or **Private**, and initialize with a README (optional).
   - Add a `.gitignore` file (select the **Python** template to exclude `client_secrets.json`).

2. **Prepare Your Files**:
   - In `C:\Users\Crimplicon2\Desktop\BUSINESS\EP\BOTS\YouTube Bot`, ensure you have:
     - `YouTubeV2.py` (with the script from my May 24, 2025, 3:50 AM EDT response).
     - Do **not** include `client_secrets.json` in the repository.
   - Create a `README.md` file:
     - Open Notepad, paste the Markdown content above.
     - Save as `README.md` (select **All Files (*.*)**, UTF-8 encoding) in the folder.
   - Create a `.gitignore` file:
     - In Notepad, add:
       ```
       client_secrets.json
       *.pyc
       __pycache__/
       ```
     - Save as `.gitignore` (select **All Files (*.*)**).

3. **Push to GitHub**:
   - Install Git if not already installed ([git-scm.com](https://git-scm.com/)).
   - Open Command Prompt, navigate to your folder:
     ```bash
     cd C:\Users\Crimplicon2\Desktop\BUSINESS\EP\BOTS\YouTube Bot
     ```
   - Initialize Git and push:
     ```bash
     git init
     git add YouTubeV2.py README.md .gitignore
     git commit -m "Initial commit with YouTube chatbot"
     git remote add origin https://github.com/your-username/YouTubeChatBot.git
     git branch -M main
     git push -u origin main
     ```
   - Replace `your-username` with your GitHub username.
   - Enter your GitHub credentials when prompted.

4. **Verify on GitHub**:
   - Visit your repository (e.g., `https://github.com/your-username/YouTubeChatBot`).
   - Ensure `YouTubeV2.py`, `README.md`, and `.gitignore` are uploaded, and `client_secrets.json` is excluded.
   - The README will render as the repository’s homepage.

### Notes
- **Sensitive Data**: The README avoids mentioning `alvalanker@gmail.com`, `Crimplicon98@`, or specific stream IDs, keeping it generic and safe for public sharing.
- **Stream ID**: The README instructs users to set their own `STREAM_ID`, supporting your goal to post in someone else’s stream (May 24, 2025, 4:02 AM EDT).
- **Class Project**: The README emphasizes the educational purpose and ethical use, aligning with your class demo needs.
- **Troubleshooting**:
  - If Git commands fail, ensure Git is installed and you’re authenticated.
  - If the README doesn’t render correctly, verify it’s saved as `README.md` with UTF-8 encoding.
- **Customization**: If you want to add specific details (e.g., your GitHub username, project name, or additional features), let me know, and I can tweak the README.

If you need help with Git setup, pushing to GitHub, or customizing the README further, share the specific issue or details (e.g., your GitHub username), and I’ll assist! Let me know when you’re ready to upload or if you want to test the bot again first.
