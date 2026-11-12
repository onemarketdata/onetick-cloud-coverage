# Singapore Exchange - FX Derivatives Enumerations

Futures and spreads with Trades, Quotes and bars for SGX FX futures, with history from September 2014. SGX is one of Asia’s largest FX futures exchanges, with key contracts in USD/CNH, INR/USD and other Asian currency pairs.

The following fields have Enumerations:

* AGGRESSOR_SIDE - Indicates whether a trade resulted from an incoming buy or sell order.
* AUCTION_TYPE - Type of auction from which an indicative auction price / auction imbalance originates.
* BOOK_TYPE - Type of order book or trading mechanism through which a trade was executed.
* OMD_STATUS - Indicates an instrument’s current trading status. Values are normalized across all DBs.
* QUOTE_SESSION - Trading session from which the quote originates, e.g. “Day”, “Night”
* TRADE_PERIOD - Market period during which a trade was executed.
* TRADE_SESSION - Trading session from which a trade originates, e.g. “Day”, “Night”
* TRADE_TYPE - Type of trade

#### AGGRESSOR_SIDE - Enumeration

| Enumeration ID   | Enumeration Description                                          |
|------------------|------------------------------------------------------------------|
| ‘””’             | Undefined (e.g. auction trades, implied trades, off-book trades) |
| B                | Buy                                                              |
| S                | Sell                                                             |

#### AUCTION_TYPE - Enumeration

| Enumeration ID   | Enumeration Description                 |
|------------------|-----------------------------------------|
| A                | Unspecified auction                     |
| C                | Closing auction                         |
| I                | Intraday auction                        |
| O                | Opening auction                         |
| P                | IPO / Public offering auction           |
| S                | Settlement (EDSP) auction               |
| U                | Unscheduled auction                     |
| c                | Post-close auction                      |
| o                | Opening auction (extended hours)        |
| p                | Auction initiated by market participant |
| u                | Unscheduled auction (extended hours)    |

#### BOOK_TYPE - Enumeration

|   Enumeration ID | Enumeration Description   |
|------------------|---------------------------|
|                0 | Lit order book            |
|                1 | Off-book                  |

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

| Enumeration ID   | Enumeration Description          |
|------------------|----------------------------------|
| T                | T session (current business day) |
| T+1              | T+1 session (next business day)  |

#### TRADE_PERIOD - Enumeration

| Enumeration ID   | Enumeration Description   |
|------------------|---------------------------|
| -                | Regular trading           |
| A                | Auction                   |
| C                | Closing auction           |
| O                | Opening auction           |

#### TRADE_SESSION - Enumeration

| Enumeration ID   | Enumeration Description          |
|------------------|----------------------------------|
| T                | T session (current business day) |
| T+1              | T+1 session (next business day)  |

#### TRADE_TYPE - Enumeration

|   Enumeration ID | Enumeration Description               |
|------------------|---------------------------------------|
|                0 | Regular trade                         |
|                1 | Combo to combo trade [until 20200424] |
|                2 | Combo to Leg trade [until 20200424]   |
|                3 | Spread trade                          |
|                4 | Off-book trade                        |

