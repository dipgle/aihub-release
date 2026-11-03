# AI Hub — a coding agent on free models

**Give coding tasks in AI Hub's own window, or from your phone over Telegram, and they get done on your computer,
the way paid coding agents do them. It runs on free AI models, with no API key and no subscription.**

> **Donate:** AI Hub is free. If it saves you time, support it with Binance Pay (account **User-7da9b**):
> [the QR code](#donate). No Binance account yet? [Sign up with our referral link](https://account.binance.com/register?ref=147135668&registerChannel=user_center).

- **An app for Mac and Windows.** Install it like any app. Its window is where you talk to the agent, and it is
  also the browser the agent works in: nothing else to install. It opens by itself at every login.
- **Free models.** The agent works through AI chat sites you sign in to. Gemini (free tier, Flash) is on from the
  start. You can turn on others too: ChatGPT, Claude, DeepSeek, Grok, Copilot, Qwen and Perplexity. If one of them
  hits its limit, the task moves on to the next one you turned on.
- **It codes like the paid agents.** The agent reads and searches your project, edits and writes files, runs
  commands and tests, takes screenshots of your UI, and sends files back to you. It asks before every write or
  command: you press **Đồng ý** (yes), **Không** (no) or **Đồng ý cả cuộc** (yes for this conversation). Or press
  **🤖 Tự làm cả cuộc** (auto) and let it work alone, still only inside its project folder.
- **In its window, or over Telegram.** Type a task as you would to a person: *"make a hello folder with a
  README"*, *"run the shop project's tests"*. Attach files or paste a picture with it. Connect your own Telegram
  bot to give tasks from your phone too. The bot's own buttons and messages are in Vietnamese.

## What you need

- A Mac (Apple Silicon or Intel), or a PC with Windows 10 or 11 (64-bit).
- A Google account for gemini.google.com (you sign in inside AI Hub's window).
- Optional: Telegram, to give tasks from your phone.

## Install the app

From the [latest release](https://github.com/dipgle/aihub-release/releases/latest) download the file for your
computer. Each file's sha256 is in `SHA256SUMS.txt` there.

**Mac** — `AIHub-<version>-mac-arm64.dmg` (Apple Silicon: M1 and later) or `AIHub-<version>-mac-x64.dmg` (Intel).

1. Open the .dmg and drag **AI Hub** onto **Applications**.
2. Open **AI Hub** from Applications. It is not notarized by Apple yet, so the first time macOS refuses: open
   **System Settings → Privacy & Security**, and next to «AI Hub was blocked» press **Open Anyway**.

**Windows** — `AIHub-<version>-windows-x64-setup.exe`.

1. Run it. It is not signed yet, so Windows SmartScreen may warn: **More info** → **Run anyway**.
2. Press **Install** (no administrator rights needed), leave **Open AI Hub** ticked and press **Finish**.

The first time it opens, AI Hub sets the agent's working folder (`~/AIHub` on a Mac, `%USERPROFILE%\AIHub` on
Windows; the agent reads and writes only there) and opens at every login from then on. Its window opens a few seconds
later: the chat on the left, the AI site on the right. Sign in to Google there once, then type a task.

**Telegram (optional):** in AI Hub's window press **⚙ Cài đặt** and follow **Hướng dẫn kết nối Telegram**: create
a bot with **@BotFather**, paste its token, then connect your chat with the code the window shows.

## Or, on a Mac: install from Terminal (Telegram, in your own browser)

This way the agent works in your own Chrome, Brave or Edge, signed in to Google, and you give it tasks over Telegram.
Open **Terminal**, paste this and press Enter:

```
curl -fsSL https://github.com/dipgle/aihub-release/releases/latest/download/install.sh | sh
```

The installer downloads the program, checks its sha256, installs it into `~/.aihub`, then walks you through:

1. **Your Telegram bot.** In Telegram, send `/newbot` to **@BotFather** and paste the token it gives you.
2. **Link your chat.** Terminal shows `/start 123456`. Send exactly that to your new bot. Only that chat can use it.
3. **Working folder.** Press Enter for `~/AIHub`. The agent only reads and writes inside it.
4. **Extension.** Open `chrome://extensions` (Brave: `brave://extensions`, Edge: `edge://extensions`), turn on
   **Developer mode**, click **Load unpacked** and pick `~/.aihub/share/aihub/extension`. The path is already on
   your clipboard: press ⌘⇧G, then ⌘V.

macOS then asks whether **aihub-launch** may control System Events, Finder and your browser. Click **OK** each time:
the agent uses this to open its own browser window. When the bot says **"✅ AI Hub đã sẵn sàng"** ("AI Hub is ready"), it is
ready. Update or reinstall: run the same command again; your settings are kept.

## Use it

In AI Hub's window or in your Telegram chat with the bot:

| Command | What it does |
|---|---|
| any message | a task for the agent |
| `/moi` | start a new conversation |
| `/tudong` · `/tudong tat` | turn auto on / off (writes and allowed commands without asking) |
| `/nguon` | list the AI sources (Gemini is on) |
| `/bat <key>` · `/tat <key>` | turn a source on / off (sign in to that site where the agent works) |
| `/hoi <question>` | ask every source that is on: a plain question, not a task |
| `/hanmuc` | usage so far |

## Remove it

- **Mac app:** quit AI Hub, drag it from Applications to the Bin, and remove it from **System Settings → General →
  Login Items**. Your data stays in `~/Library/Application Support/aihub`, the agent's folder in `~/AIHub`.
- **Windows:** **Settings → Apps → Installed apps → AI Hub → Uninstall**.
- **Installed from Terminal:**
  `curl -fsSL https://github.com/dipgle/aihub-release/releases/latest/download/install.sh | sh -s -- --uninstall`

## Donate

AI Hub is free. If it saves you time, you can support it with **Binance Pay**: scan the QR code with the Binance
app (account **User-7da9b**).

<img src="donate-binance.jpg" alt="Binance Pay QR code — User-7da9b" width="240">

No Binance account yet? Sign up with our referral link (referral ID **147135668**):
<https://account.binance.com/register?ref=147135668&registerChannel=user_center>
