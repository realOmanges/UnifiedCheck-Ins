# Omanges Unified Check-In System

A streamlined Twitch check-in system built for **Streamer.bot v0.2.8**, designed to unify both manual and automatic community check-ins across Discord-linked communities. This system uses just two actions and a single log folder to track daily check-ins from viewers—either manually via command or automatically based on shared Discord check-in logs.

---

## 🎯 Features

* ✅ **Single Log File**: Combines all check-ins into one centralized `CheckIns.txt` file.
* 🔄 **Auto Check-In**: Automatically checks users in based on the `AutoCheckIns.txt` file.
* 🔔 **Manual Check-In Command**: Triggers a chat-friendly check-in and stores the user if not already listed.
* 🔒 **Duplicate Protection**: Prevents duplicate check-ins for the same user on the same day.
* 📂 **Customizable Settings**: Change folder/file names, date format, and Twitch chat messages easily.
* 🧩 **Modular Integration**: Ideal for community crossovers, shared channels, or merged check-in logs.

---

## 🧠 How It Works

The system runs off two main C# inline scripts:

### 1. `AutoCheckIn.cs`

* Reads usernames from `AutoCheckIns.txt`.
* Cross-references today's entries in `CheckIns.txt`.
* If the user hasn't checked in yet, it logs the date and username.
* Sends a success message to Twitch chat.

### 2. `ManualCheckIn.cs`

* Triggered via command or button (e.g. `!checkin`).
* Logs the user in today's `CheckIns.txt` if not already listed.
* Adds their name to `AutoCheckIns.txt` if new.
* Sends Twitch confirmation or duplicate message.

---

## 📁 Folder Structure

```
StreamerBot/
└── Check-Ins/
    ├── CheckIns.txt
    └── AutoCheckIns.txt
```

## 📝 Customization

All key strings and filenames are stored in clearly marked **`// SETTINGS`** sections. You can update:

* Folder/File Names
* Date Format
* Log Line Format
* Chat Messages for Success/Fail

---

## 🔍 Example Log Entry

Inside `CheckIns.txt`:

```
07/30/25 - omanges
```

Inside `AutoCheckIns.txt`:

```
omanges
username123
```

---

## ⚠️ Notes

* You can comment out the final line in `AutoCheckIn.cs` if you don’t want the auto file to reset daily.
* Make sure your `Check-Ins` folder path is correct and that Streamer.bot has read/write access.

---

## 📞 Support

Join the [SIDOR Community Discord](https://discord.gg/2pcKpMrxdD) to get help, suggest features, or just hang out with other creators using this system.

---

## 💬 Feedback or Contributions

Want to submit more facts or categories?

* Open a pull request
* Create an issue with your suggestion
* Or fork it and go wild

You can also suggest ideas via [GitHub Issues](https://github.com/realOmanges/UnifiedCheck-Ins/issues).

This tool is built to be modular, sharable, and Twitch-friendly.

---

## 👤 Author

**Omanges**
🟣 Twitch: [twitch.tv/omanges](https://twitch.tv/omanges)
💬 Join the [SIDOR Community Discord](https://discord.gg/2pcKpMrxdD)

---

## 📄 License

MIT License
You’re free to use, modify, and share this—just give credit.

---
