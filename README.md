Finance Web Application

A simple stock trading simulation built with Flask, Python, and SQLite as part of CS50's Web track.

Features

User registration and login with password hashing.

View portfolio: see owned stocks and cash balance.

Buy stocks: purchase shares if sufficient cash is available.

Sell stocks: sell shares that you own.

View transaction history.

Stock quotes: get real-time stock prices using lookup.

Requirements

Python 3.x

Flask

Flask-Session

Werkzeug

CS50 Library (cs50)

SQLite

Install dependencies:

pip install flask flask-session werkzeug cs50

Setup

Clone the repository:

git clone <your-repo-url>
cd finance


Initialize the database:

sqlite3 finance.db < finance.sql


Run the application:

export FLASK_APP=app.py
export FLASK_ENV=development
flask run


Open your browser at http://127.0.0.1:5000/.

Usage
Pages

/ (Index): Displays user's portfolio with stocks and cash balance.

/buy: Form to buy stocks.

/sell: Form to sell stocks.

/quote: Form to get a stock quote.

/history: Shows all past transactions.

/login: User login page.

/logout: Logs out the current user.

/register: User registration page.

Notes

Use real stock symbols to buy and sell.

All financial transactions update the SQLite database.

Flash messages show the result of operations (Bought!, Sold!, etc.).

Project Structure
finance/
│
├─ app.py             # Main Flask application
├─ helpers.py         # Helper functions (login_required, apology, lookup, usd)
├─ finance.db         # SQLite database
├─ finance.sql        # Database schema
├─ templates/         # HTML templates (layout.html, index.html, buy.html, sell.html, quote.html, history.html, login.html, register.html)
└─ static/            # CSS and other static files
