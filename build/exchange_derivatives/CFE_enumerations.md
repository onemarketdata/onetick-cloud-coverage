# Cboe Futures Exchange (CFE) Enumerations

Futures, options and spreads with Trades, Quotes, bars and real-time data from Cboe Futures Exchange (CFE), with history from June 2012. CFE is best known for VIX and Mini VIX futures, which trade the market’s expectation of 30-day S&P 500 volatility, and also lists other volatility and index products.

The following fields have Enumerations:

* BOOK_TYPE - Type of order book or trading mechanism through which a trade was executed.
* CALL_PUT_IND - “C” - Call option, “P” - Put option
* OMD_STATUS - Indicates an instrument’s current trading status. Values are normalized across all DBs.
* TRADE_PERIOD - Market period during which a trade was executed.
* TRADE_TYPE - Type of trade

#### BOOK_TYPE - Enumeration

|   Enumeration ID | Enumeration Description   |
|------------------|---------------------------|
|                0 | Lit book                  |
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
| O                | Opening auction           |

#### TRADE_TYPE - Enumeration

|   Enumeration ID | Enumeration Description                          |
|------------------|--------------------------------------------------|
|                0 | Regular trade                                    |
|               12 | Re-opening trade                                 |
|               14 | Spread trade                                     |
|               17 | Trade cancellation                               |
|               22 | Block trade                                      |
|               23 | Exchange of contract for related position (ECRP) |
|                4 | Late reported (in correct sequence)              |
|                5 | Opening trade                                    |

