# Japannext J-Market Enumerations

Trades, quotes, bars and book depth from Japannext’s J-Market, a proprietary trading system (PTS) for Japanese equities, with history from March 2014. Japannext is one of Japan’s main alternatives to the Tokyo Stock Exchange, often offering finer price increments for TSE-listed stocks. Covered stocks include Nikkei 225 and TOPIX constituents.

The following fields have Enumerations:

* BOOK_TYPE - Type of order book or trading mechanism through which a trade was executed.
* OMD_STATUS - Indicates an instrument’s current trading status. Values are normalized across all DBs.
* QUOTE_SESSION - Trading session from which the quote originates, e.g. “Day”, “Night”
* TRADE_PERIOD - Market period during which a trade was executed.
* TRADE_SESSION - Trading session from which a trade originates, e.g. “Day”, “Night”

#### BOOK_TYPE - Enumeration

|   Enumeration ID | Enumeration Description   |
|------------------|---------------------------|
|                0 | Lit order book            |

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

#### QUOTE_SESSION - Enumeration

| Enumeration ID   | Enumeration Description   |
|------------------|---------------------------|
| Day              | Day session               |
| Night            | Night session             |

#### TRADE_PERIOD - Enumeration

| Enumeration ID   | Enumeration Description   |
|------------------|---------------------------|
| -                | Regular trading           |

#### TRADE_SESSION - Enumeration

| Enumeration ID   | Enumeration Description   |
|------------------|---------------------------|
| Day              | Day session               |
| Night            | Night session             |

