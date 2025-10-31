```
# WA Base Bot

A powerful, modular WhatsApp bot built with Node.js using the Baileys library. This bot features a dynamic plugin system that allows you to easily extend functionality without modifying the core code.

## 🎯 Aim

The goal of this project is to provide a clean, maintainable, and extensible base for WhatsApp bot development. With its plugin architecture, developers can easily add new commands and features while keeping the core system stable and efficient.

## 📺 YouTube Tutorial Series

Follow along with the complete tutorial series on my YouTube channel where I build and explain this bot step by step:

**YouTube Channel:** [Debraj's Tech Tutorials](https://youtube.com/@debrajzero)  
**Playlist:** WA Base Bot Development Series

In this series, you'll learn:
- How to set up the bot from scratch
- Understanding the plugin system
- Creating custom commands
- Deploying your bot
- Advanced features and optimizations

## ✨ Features

- **Dynamic Plugin System** - Load commands from external plugins automatically
- **Modern Baileys Library** - Latest WhatsApp Web protocol implementation
- **Organized Menu System** - Commands categorized into intuitive sections
- **Hot Reload** - Reload plugins without restarting the bot
- **Permission System** - Owner-only, group-only, and admin commands
- **System Monitoring** - Built-in runtime and performance tracking
- **Media Downloaders** - YouTube audio/video downloader plugins
- **Tool Commands** - Various utility and fun commands

## 🏗️ Project Structure

```

WA-Base-Bot/
├──settings/
│└── config.js
├──library/
│├── function.js
│├── serialize.js
│├── exif.js
│├── uploader.js
│├── quoted.js
│├── Api.js
│└── converter.js
├──plugins/
│├── ping.js
│├── runtime.js
│├── play.js
│└── song.js
├──thumbnail/
│├── image.jpg
│└── document.jpg
├──message.js
├──index.js
└──package.json

```

## 🚀 Quick Start

### Prerequisites
- Node.js 16+
- WhatsApp account

### Installation

1. **Clone the repository**
```bash
git clone https://github.com/FuriousGamer414/WA-Base-Bot.git
cd WA-Base-Bot
```

1. Install dependencies

```bash
npm install
```

1. Configure the bot
   Editsettings/config.js with your preferences.
2. Start the bot

```bash
npm start
```

1. Scan the QR code with your WhatsApp app

🔌 Plugin Development

Creating a Plugin

Create a new file in the plugins/ directory:

```javascript
// plugins/example.js
module.exports = {
    command: 'example',
    description: 'Example command',
    category: 'general',
    owner: false,
    group: false,
    admin: false,
    
    execute: async (sock, m, {
        args,
        text,
        reply,
        sender,
        isCreator,
    }) => {
        await reply('Hello World!');
    }
};
```

Available Categories

· ai - AI Commands
· downloader - Downloader Commands
· fun - Fun Commands
· general - General Commands
· group - Group Management
· owner - Owner Commands
· tools - Tool Commands
· video - Video Commands
· other - Other Commands

📋 Basic Commands

· .menu - Show all available commands
· .ping - Check bot response time
· .runtime - Check bot uptime (owner)
· .reload - Reload all plugins (owner)
· .plugins - List loaded plugins
· .play - Download YouTube audio
· .song - Download YouTube audio

🛠️ Configuration

Edit settings/config.js to customize:

· Bot owner number
· Session name
· API keys
· Public/private mode
· Thumbnail URLs

🤝 Contributing

1. Fork the repository
2. Create your feature branch
3. Commit your changes
4. Push to the branch
5. Open a Pull Request

📝 License

This project is licensed under the MIT License.

⚠️ Disclaimer

This bot is for educational purposes only. Users are responsible for complying with WhatsApp's Terms of Service.

📞 Contact

· YouTube: Hector Manuel
· Telegram: @official_kango
· GitHub: OfficialKango 

🙏 Credits

Base Developer: Debraj
Baileys Library: WhiskeySockets

---

Made with ❤️ by Hector Manuel
