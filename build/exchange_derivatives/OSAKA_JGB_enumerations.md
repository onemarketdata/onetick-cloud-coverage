# Osaka Exchange - JGB Futures Enumerations

Futures and spreads with Trades, Quotes and bars for Japanese Government Bond (JGB) futures on Osaka Exchange, Japan’s largest derivatives exchange, with history from March 2014. The 10-year JGB future is the benchmark for hedging Japanese interest rate risk.

The following fields have Enumerations:

* BOOK_TYPE - Type of order book or trading mechanism through which a trade was executed.
* CALL_PUT_IND - “C” - Call option, “P” - Put option
* OMD_STATUS - Indicates an instrument’s current trading status. Values are normalized across all DBs.
* TRADE_PERIOD - Market period during which a trade was executed.
* TRADE_TYPE - Type of trade
* TRADE_SESSION - Trading session from which a trade originates, e.g. “Day”, “Night”

#### BOOK_TYPE - Enumeration

|   Enumeration ID | Enumeration Description   |
|------------------|---------------------------|
|                0 | Lit order book            |
|                1 | Off-book                  |

#### CALL_PUT_IND - Enumeration

| Enumeration ID   | Enumeration Description   |
|------------------|---------------------------|
| C                | Call option               |
| P                | Put option                |

#### OMD_STATUS - Enumeration

| Enumeration ID   | Enumeration Description       |
|------------------|-------------------------------|
| A                | Auction                       |
| B                | Break / Pause                 |
| C                | Closing auction               |
| D                | Delisted / Pending deletion   |
| H                | Halted                        |
| I                | Scheduled intraday auction    |
| M                | Mandatory quoting period      |
| N                | New instrument / Pre-listing  |
| O                | Opening auction               |
| P                | Pre-market                    |
| Q                | Indicative quoting period     |
| R                | Off-book trade reporting      |
| S                | Suspended                     |
| T                | Continuous trading            |
| U                | Unscheduled auction           |
| c                | Closed                        |
| i                | IPO / Public offering auction |
| n                | No market phase / Unspecified |
| o                | Order management              |
| p                | Post-market                   |
| t                | Trading at last price         |

#### TRADE_PERIOD - Enumeration

| Enumeration ID   | Enumeration Description   |
|------------------|---------------------------|
| -                | Regular trading           |
| A                | Auction                   |
| C                | Closing auction           |
| O                | Opening auction           |
| U                | Unscheduled auction       |

#### TRADE_TYPE - Enumeration

|   Enumeration ID | Enumeration Description           |
|------------------|-----------------------------------|
|                0 | Regular trade                     |
|               20 | Auction trade                     |
|                3 | J-Net trade                       |
|               36 | Tailor-Made Combination leg trade |
|               43 | Trade from implied order          |
|                5 | J-Net cross trade                 |
|                7 | Standard Combination leg trade    |

#### TRADE_SESSION - Enumeration

| Enumeration ID   | Enumeration Description   |
|------------------|---------------------------|
| Day              | Day session               |
| Night            | Night session             |

