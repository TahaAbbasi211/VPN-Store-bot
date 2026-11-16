# Telegram VPN Store Bot

A Telegram shop bot with a Persian UI for selling VPN plans and app subscriptions, built with Python and [pyTelegramBotAPI](https://github.com/eternnoir/pyTelegramBotAPI) (telebot).

## What it does

- Browse VPN plans (duration, data volume, price in Toman) and app subscriptions (Spotify, Apple Music, Apple TV, Disney)
- Order flow with card-payment details and admin handling
- Admin tools: broadcast messages, user management, maintenance mode
- Persistent storage with SQLAlchemy (SQLite by default, any SQLAlchemy URL works)

## Files

- `Promain.py` — the main implementation: polling bot, SQLAlchemy models (users, products, orders, settings), configuration via environment variables
- `main.py` — an earlier, simpler version: in-memory state, hardcoded catalog, no database
- `LICENCE.md` — license

## Setup (Promain.py)

```bash
pip install pyTelegramBotAPI python-dotenv sqlalchemy
```

Create a `.env` file with:

```
BOT_TOKEN=your-telegram-bot-token
SUPPORT_USERNAME=your_support_username
ADMIN_IDS=123456789,987654321
CARD_NUMBER=your-card-number
DATABASE_URL=sqlite:///bot.db
```

`DATABASE_URL` is optional (defaults to `sqlite:///bot.db`); `LOG_LEVEL` is optional too (defaults to `INFO`).

```bash
python Promain.py
```

Never commit a real `.env` file or a real bot token to the repository.

## Contact

[Telegram](https://t.me/CallMeTaha) / [Instagram](https://instagram.com/taha05abbasi)

## License

See [LICENCE.md](LICENCE.md).
