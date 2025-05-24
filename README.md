# telegram-account-reciver-VX
# ✨ AccTEL - Telegram Account Verification Bot ✨

A powerful Telegram bot built with `telethon` for managing and verifying Telegram accounts. This bot helps automate the process of checking account sessions, updating profiles, and tracking account statistics.

## ⭐ Features

### User Features:

*   **Start Bot:** Greet users and provide main menu options.
*   **Show Allowed Countries:** List countries enabled for account donation, including limits and prices.
*   **Send Number:** Initiate the process for users to donate accounts by sending their phone number.
*   **Get My Info:** Display user-specific statistics (donated, active sessions, deleted accounts) and balance.
*   **Show Donated Numbers:** List the phone numbers of accounts successfully donated by the user.
*   **Show Balance:** Display the user's current balance.
*   **Support:** Allow users to send messages to the admin.
*   **Ping:** Check bot responsiveness.

### Admin Features:

*   **Admin Panel:** Access a dedicated menu for bot management (`/admin`).
*   **Stats:** View global bot statistics (total donated, active sessions, deleted).
*   **Send Message:** Send a direct message to a specific user.
*   **Broadcast:** Send a message to all bot users.
*   **Sessions:** Download a zip file containing all active session files (`Accounts.zip`).
*   **On/Off:** Toggle bot functionality.
*   **Set 2FA Pass:** Configure a global 2FA password for accounts.
*   **Reset Stats:** Reset global or user-specific statistics.
*   **Manage Countries:** Add, edit, remove, or list allowed countries for account donation with specific limits and prices.
*   **Account Verification:** Automated process to check for active sessions, update profile (using random names/bios), and move session files upon successful verification.

## 🛠️ Dependencies

The bot requires the following Python libraries:

*   `telethon`
*   `redis`
*   `requests`
*   `sqlite3` (often included with Python)
*   `phonenumbers`
*   `lxml` (for html parsing, used by `auth2`)
*   `namegenerator` (for random names)
*   Standard Python libraries: `shutil`, `os`, `re`, `datetime`, `time`, `sys`, `random`, `json`, `string`, `geocoder`, `logging`, `asyncio`

You can install most of these using pip:
```bash
pip install telethon redis requests phonenumbers lxml namegenerator
```

## ⚙️ Setup and Installation

1.  **Clone the repository:**
    ```bashgit
    git clone https://github.com/mrVXBoT/telegram-account-reciver-VX.git 
    ```
2.  **Install dependencies:**
    ```bash
    pip install -r requirements.txt 
    ```
3.  **Set up Redis:** Ensure you have a Redis server running. The bot connects to `localhost:6379`.
4.  **Get API ID and API Hash:** Obtain your Telegram API credentials from [my.telegram.org](https://my.telegram.org). Update the `apis` list in `VX-ACC.py` with your API ID and API Hash.
5.  **Get Bot Token:** Create a new bot or use an existing one via [@BotFather](https://t.me/BotFather) and get your bot token. Update the bot initialization in `VX-ACC.py`.
6.  **Configure Admin IDs:** Add your Telegram user ID to the `admins` list in `VX-ACC.py`.
7.  **Prepare Text Files:**
    *   Create `fnames.txt` with a list of first names (one per line).
    *   Create `lnames.txt` with a list of last names (one per line).
    *   Create `about.txt` with a list of bios (one per line).
8.  **Prepare Images:**
    *   Create an `images` directory.
    *   Place a default profile photo named `default_profile_photo.jpg` inside the `images` directory.
9.  **Create `allowed_countries.json`:** This file will be created and managed via the admin panel's "Manage Countries" section after you run the bot.

## ▶️ Running the Bot

```bash
python VX-ACC.py
```

The bot should connect to Telegram, and you can start interacting with it or access the admin panel using `/admin` if you are listed as an admin.

---

```markdown
<p> Made with ❤️</p>
``` 
