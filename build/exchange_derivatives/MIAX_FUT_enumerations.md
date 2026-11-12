# MIAX Futures Exchange Enumerations

Futures, options and spreads with Trades, Quotes and bars from MIAX Futures (formerly the Minneapolis Grain Exchange, MGEX), with history from June 2025. Its main contract is Hard Red Spring Wheat futures and options, the benchmark for the high-protein wheat grown in the northern US and Canada.

The following fields have Enumerations:

* AGGRESSOR_SIDE - Indicates whether a trade resulted from an incoming buy or sell order.
* AUCTION_TYPE - Type of auction from which an indicative auction price / auction imbalance originates.
* BOOK_TYPE - Type of order book or trading mechanism through which a trade was executed.
* CALL_PUT_IND - “C” - Call option, “P” - Put option
* MKT_PHASE - Indicates the instrument’s current market phase, as specified by the trading venue
* OMD_STATUS - Indicates an instrument’s current trading status. Values are normalized across all DBs.
* TRADE_PERIOD - Market period during which a trade was executed.
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

| Enumeration ID   | Enumeration Description                                                                  |
|------------------|------------------------------------------------------------------------------------------|
| 0                | Lit order book                                                                           |
| 1                | Off-book                                                                                 |
| S                | Strategy leg [trade reported in each of outright leg when two spread orders are matched] |

#### CALL_PUT_IND - Enumeration

| Enumeration ID   | Enumeration Description   |
|------------------|---------------------------|
| C                | Call option               |
| P                | Put option                |

#### MKT_PHASE - Enumeration

|   Enumeration ID | Enumeration Description   |
|------------------|---------------------------|
|                1 | Per-open                  |
|                2 | Opening freeze            |
|                3 | Trading                   |
|                4 | Halt                      |
|                5 | Operational halt          |
|                6 | Closed                    |

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
| A                | Auction                   |
| -                | Regular trading           |

#### TRADE_TYPE - Enumeration

| Enumeration ID   | Enumeration Description      |
|------------------|------------------------------|
| 0                | Regular trade                |
| A                | Adjusted / late manual trade |
| C                | Implied trade (strategy)     |
| L                | Implied trade (outright)     |
| M                | Strategy leg trade           |
| O                | Regular trade (outright)     |
| S                | Regular trade (strategy)     |

