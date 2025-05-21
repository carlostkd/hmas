
# 🧠 HMAS API & CLI – Hackable Messaging Automation System

A command-line and browser-accessible API that blends 🕵️ hacker vibes with 💼 practical utility.

> Perfect for red teamers, sysadmins, developers and privacy enthusiasts.

## Visit https://carlostkd.ch/hmas

## Follow the blog to get real uses cases for the API

   https://blog.carlostkd.ch

## 💬 Themed Hacker Messaging

Great for generating synthetic hacker-style banter or educational content.

| Parameter       | Description                                                                 |
|------------------|----------------------------------------------------------------------------|
| `msg=`          | Fetch a themed message (e.g. msg=admin)                                     |
| `as=`           | Custom sender name                                                          |
| `talk=on`       | Enable system response (default bot reply)                                  |
| `talk=`         | Custom responder name                                                       |
| `chat=on`       | Enable informal "chat-style" banter                                         |
| `chatstyle=`    | Set the chat style (casual, sarcastic, panic, neutral, misc)                |
| `search=`       | Search for specific terms in the hacker message database                    |
| `diff=`         | Compare keywords and return a diff                                          |
| `diffmode=`     | Style the diff (classic, redacted, corrupt, strike, delta, tagged)          |
| `scenario=`     | Cheat-sheet for real-world tasks (e.g. ssh, sqlmap, nmap, grep)             |
| `format=`       | Output format (json, txt, html, md, yaml)                                   |
| `category=`     | Choose a specific hacker theme category (see `/categories.php`)             |
| `max=`          | Choose on many results 1 to 10                                              |
| `page`          | Navigate trough pages/results                                               |
| `mode`          | Daily/weekly rotation mode                                                  |
---

## ❤️ Favorites and Sharing

| Parameter       | Description                                                                 |
|------------------|----------------------------------------------------------------------------|
| `like`          | Mark the last message you received as "liked"                               |
| `liked`         | View all your previously liked messages                                     |
| `share=`        | Email the message (or cheat sheet) to any email address                     |
---

## 📈 API Tools & Inf

| Parameter       | Description                                                                 |
|------------------|----------------------------------------------------------------------------|
| `usage`         | View your API usage stats (`api.php?usage&apikey=...`)                      |
| `help`          | Print all available commands (`api.php?help&apikey=...`)                    |

---

## 🧪 Example API Calls (Raw)

```http
GET /api.php?msg=admin&talk=on&chatstyle=casual&format=json
GET /api.php?send=Meet%20me%20offline&rec=PUB-ABC123&apikey=KEY123&selfdestruct=1
GET /api.php?inbox=read&apikey=KEY123&secret=SECRET456
GET /api.php?diff=ssh+cron&diffmode=corrupt&format=txt
```

---

## 🚀 CLI Example

```bash
# Send a secure message
hmas --send="root pw is hidden" --rec=PUB-XYZ --apikey=KEY123 --selfdestruct

# Read your inbox
hmas --inbox=read --apikey=KEY123 --secret=SECRET456

# Delete a message
hmas --delete=42 --apikey=KEY123 --secret=SECRET456

# Themed hacker message
hmas --msg="exploit" --talk=on --chat --chatstyle=panic --format=md
```

---

## 📍 Setup Your CLI

```bash
git clone https://github.com/yourname/hmas-cli.git
cd hmas-cli
npm install
npm link
```

Now you can run `hmas` from any terminal.


---

## 🔐 Secure Message Features

You can use the API to send, receive, and manage secure messages **between users**, 

protected by **end-to-end encryption** and private access keys.

📍 **Web dashboard**:
- `/hmas/secure.php` → Generate your `public_key` and `secret_key`
- `/hmas/inbox.html` → Send and read messages through a clean UI

📍 **CLI**: Use `hmas` (CJS or ESM) for full automation power

---


## 📬 Message Exchange Parameters

| Parameter       | Description                                                                 |
|------------------|----------------------------------------------------------------------------|
| `send=`         | Send an encrypted message (requires `rec=` and `apikey=`)                   |
| `rec=`          | Recipient public key                                                        |
| `apikey=`       | Your private API key                                                        |
| `selfdestruct=1`| Message deletes itself after being read                                     |
| `inbox=read`    | Fetch messages for your secret key (`apikey` + `secret`)                    |
| `inbox=delete&id=` | Delete a message by ID                                                   |
| `secret=`       | Your personal inbox key (used only to read/delete your messages)            |
---




---

## 🛡️ Final Tips

- 🔐 Keep your **secret key** private. It controls inbox access.
- 📢 Share only your **public key** when receiving messages.
- 💣 Use `--selfdestruct` for extra-sensitive messages.
- 🧠 Combine with `--scenario`, `--chatstyle`, or `--diff` for hacking-themed workflows.

---

## 🧑‍💻 Built For

- Red teamers
- Hackathon participants
- Sysadmins with secrets
- Privacy nerds
- Anyone who loves encryption + style

---

## 📜 License

🛸 Powered by Carlostkd — Injecting chaos into your stack since 1337
