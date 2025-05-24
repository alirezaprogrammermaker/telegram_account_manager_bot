# Telegram Account Manager Bot

A secure and extensible Telegram bot for managing multiple Telegram accounts, built
using [Telethon](https://docs.telethon.dev) – a powerful Python library for interacting with the Telegram API.  
This bot supports session persistence, Two-Factor Authentication (2FA), and automated interaction with multiple
accounts, making it ideal for use cases such as account management, marketing automation, and bot-driven services.

## Features

- ✨ Add multiple phone numbers
- 🔐 Secure session management
- 🛡️ Two-factor authentication support
- 📱 Private chat only (secure)
- 💾 SQLite database storage
- 📋 Account status tracking

## Security Features

- Sessions stored locally with encryption
- No data stored on external servers
- Comprehensive error handling
- Flood protection
- Private chat enforcement

## Installation

### Prerequisites

- Python 3.8+
- Telegram account
- Bot token from @BotFather
- API credentials from my.telegram.org

### Setup Steps

1. **Clone the repository:**
   ```bash
   git clone https://github.com/alirezaprogrammermaker/telegram_account_manager_bot.git
   cd telegram_account_manager_bot
   ```

2. **Create virtual environment:**
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```

3. **Install dependencies:**
   ```bash
   pip install -r requirements.txt
   ```

4. **Configure environment:**
   ```bash
   cp example.env.example example.env
   ```
   Edit .env with your credentials:
   ```dotenv
   BOT_TOKEN=YOUR_BOT_TOKEN_HERE
   API_ID=YOUR_API_ID_HERE
   API_HASH=YOUR_API_HASH_HERE
   ```

5. **Run the bot:**
   ```bash
   python main.py
   ```

### Getting Credentials

#### Bot Token

- Message @BotFather on Telegram
- Send /newbot
- Follow instructions to create bot
- Copy the token to your .env file

#### API Credentials

- Visit https://my.telegram.org
- Log in with your phone number
- Go to "API Development tools"
- Create new application
- Copy API ID and API Hash to your .env file

## Usage

- Start the bot: /start
- Click "➕ Add Number"
- Enter phone number in international format (+1234567890)
- Enter verification code received via Telegram
- If 2FA is enabled, enter your password
- View your numbers with "📱 My Numbers"

### Bot Commands

- /start - Initialize bot and show main menu
- /help - Show help information

## File Structure

```plaintext
telegram_account_manager_bot/
├── main.py                # Main bot application
├── requirements.txt       # Python dependencies
├── .env.example           # Environment template
├── .gitignore             # Git ignore rules
├── README.md              # This file
├── sessions/              # Session files (auto-created)
└── telegram_manager.db    # SQLite database (auto-created)
```

## Database Schema

The bot uses SQLite with three main tables:

- telegram_bot_users - User information
- numbers - Phone numbers and authentication status
- telegram_bot_user_sessions - Session data

## Security Notes

⚠️ Important Security Considerations:

- Never share your verification codes
- Use strong 2FA passwords
- Keep your .env file secure
- Sessions are stored locally – keep your server secure
- Bot only works in private chats for security
- Regular backups recommended

## Error Handling

The bot includes comprehensive error handling for:

- Invalid phone numbers
- Expired verification codes
- Rate limiting (flood protection)
- Network connectivity issues
- 2FA authentication errors

## Logging

All activities are logged to:

- telegram_manager.log (file)
- Console output

## Contributing

1. Fork the repository
2. Create feature branch (git checkout -b feature/amazing-feature)
3. Commit changes (git commit -m 'Add amazing feature')
4. Push to branch (git push origin feature/amazing-feature)
5. Open Pull Request

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Disclaimer

This bot is for educational and legitimate account management purposes only. Users are responsible for complying with
Telegram's Terms of Service and applicable laws.

## Support & Contact

If you encounter issues or have questions:

- GitHub Issues: Create an issue on this repository for bug reports or feature requests
- Email: alirezaprogrammermaker@gmail.com
- Telegram: @alireza_offleft
- Check the logs for error messages in telegram_manager.log
- Verify credentials in your .env file

## Author

👨‍💻 Alireza Programmer Maker

- GitHub: @alirezaprogrammermaker
- Email: alirezaprogrammermaker@gmail.com
- Telegram: @alireza_offleft

Feel free to reach out for questions, collaborations, or project discussions!

## Changelog

### v1.0.0

- Initial release
- Basic account management
- Session persistence
- 2FA support
