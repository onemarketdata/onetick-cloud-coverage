# Bursa Malaysia - Equities Enumerations

Trades, quotes and bars from Bursa Malaysia’s securities market, with history from November 2008, covering the Main and ACE markets, including many Sharia-compliant securities. Covered stocks include constituents of the FTSE Bursa Malaysia KLCI.

The following fields have Enumerations:

* BOOK_TYPE - Type of order book or trading mechanism through which a trade was executed.
* TRADE_PERIOD - Market period during which a trade was executed.
* TRADE_TYPE - Type of trade

#### BOOK_TYPE - Enumeration

|   Enumeration ID | Enumeration Description   |
|------------------|---------------------------|
|                0 | Lit order book            |
|                1 | Off-book                  |
|                3 | Odd lot book              |
|                5 | Buy-in                    |

#### TRADE_PERIOD - Enumeration

| Enumeration ID   | Enumeration Description   |
|------------------|---------------------------|
| -                | Regular trading           |
| C                | Closing auction           |
| I                | Intraday auction          |
| O                | Opening auction           |
| T                | Trading at closing price  |
| U                | Unscheduled auction       |

#### TRADE_TYPE - Enumeration

| Enumeration ID   | Enumeration Description   |
|------------------|---------------------------|
| 0                | Regular trade             |
| 1                | Cross trade               |
| 2                | Auction trade             |
| 6                | Off-market trade          |
| 7                | Off-market cross trade    |
| BN               | Buy-in                    |
| DB               | Negotiated trade          |
| OM               | Odd lot                   |

