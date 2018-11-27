# amazon-auto-reload

This python scripts automates the process of reloading Amazon.com gift cards with user-defined amounts and user-defined transactions per execution. This is useful to maximize credit and debit card rewards or to prevent the closure of a credit account due to inactivity.

## Dependencies

- Python 2.7 or newer.
- Selenium
- Chromedriver

## Instructions

1. Install Selenium by typing `pip install -U selenium` into your command line.
2. Download [Chromedriver](https://sites.google.com/a/chromium.org/chromedriver/) and place into the root directory (where `run.py` is).
3. Modify `config.json` with your Amazon credentials and the cards you wish to reload.
```json
{
    "username": "amazon_username",
    "password": "amazon_password",
    "cards": [
        { 
            "cardNumber": "XXXXXXXXXXXX5555",
            "reloadAmount": 0.50,
            "reloadTimes": 1
        },
        {
            "cardNumber": "XXXXXXXXXXXX1234", 
            "reloadAmount": 1.25, 
            "reloadTimes": 3
        }
    ],
    "reloadDelay": 300
}
```
4. Run `bot.py`.