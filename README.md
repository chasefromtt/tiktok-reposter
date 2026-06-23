# tiktok-reposter
reposts tiktok videos to Instagram &amp; Youtube for easier reposting and if you want to save a quick buck from the overly priced nonsense. Made 100% skidded from ai, props to Codex because im a skid at heart. Ill never touch a while true loop in my lifespan
OOH YEA forgot to mention theres a tutorial if you are stupid like me for instagram instagram is like 90x more tedious than youtube is so good lucck!!
# TikTok Repost Studio

A Windows desktop app for downloading TikTok clips, choosing which videos to repost, and uploading them to YouTube Shorts or Instagram Reels.

## Public Repo Notes
- This export is intentionally cleaned for GitHub.
- No live Google OAuth secret, Instagram token, tester account, downloaded media, build output, or local upload history is included.
- The app starts with blank credential fields so each person can connect their own accounts.

## What You Need Before Running
1. Python 3.10 or newer.
2. A Google OAuth Desktop App JSON for YouTube uploads.
3. A Meta/Instagram professional account setup if you want Instagram uploads.

## Setup
1. Open Terminal or Command Prompt inside this folder.
2. Install dependencies:

```bash
pip install -r requirements.txt
```

3. Create your own YouTube OAuth client:
   - Open Google Cloud Console.
   - Create or select a project.
   - Enable `YouTube Data API v3`.
   - Create an OAuth Client ID for a `Desktop app`.
   - Download the JSON file.
   - In this app, click `Browse` and select that JSON file.

4. For Instagram uploads, use your own:
   - Instagram professional account ID
   - Meta access token with publishing access

## Optional Credentials Template
A safe example file is included at:

```txt
resources/client_secrets.example.json
```

Do not commit your real OAuth JSON. If you want a local copy in the repo folder, place it at:

```txt
resources/client_secrets.json
```

That filename is already ignored by Git.

## Run The App

```bash
python app.py
```

## Build A Windows .exe

```bash
pip install pyinstaller
pyinstaller --onefile --windowed --name TikTokRepostStudio app.py
```

The finished app will be created in:

```txt
dist/
```

## Local Files The App Creates
- `tiktok_downloads/` for downloaded clips and upload logs
- a YouTube `token.pickle` in your Windows local app data folder
- local UI settings in your Windows app data folder

These are ignored or stored outside the repo so the project can stay clean.

## Safety Reminder
Only download or repost content you own or have permission to use. Platform rules and copyright rules still apply.
