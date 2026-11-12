# A3 Markets - Matba Rofex Enumerations

Futures, options, spreads and indices from A3 Mercados, Argentina’s main derivatives exchange, formed in 2024 by the merger of Matba Rofex and MAE, with history from July 2026. A3 lists contracts on the US dollar/Argentine peso exchange rate, agricultural products such as soybeans, corn and wheat, and the Merval equity index.

The following fields have Enumerations:

* AGGRESSOR_SIDE - Indicates whether a trade resulted from an incoming buy or sell order.
* TRADE_TYPE - Type of trade
* TRADE_PERIOD - Market period during which a trade was executed.
* BOOK_TYPE - Type of order book or trading mechanism through which a trade was executed.
* MKT_PHASE - Indicates the instrument’s current market phase, as specified by the trading venue
* OMD_STATUS - Indicates an instrument’s current trading status. Values are normalized across all DBs.

#### AGGRESSOR_SIDE - Enumeration

| Enumeration ID   | Enumeration Description                          |
|------------------|--------------------------------------------------|
| ‘””’             | Undefined (e.g. auction trades, off-book trades) |
| B                | Buy                                              |
| S                | Sell                                             |

#### TRADE_TYPE - Enumeration

| Enumeration ID   | Enumeration Description                                                                                                       |
|------------------|-------------------------------------------------------------------------------------------------------------------------------|
| ‘””’             | Regular trade                                                                                                                 |
| BLK              | Block trade                                                                                                                   |
| LEG              | Strategy leg trade  [Synthetic trade reported on each outright leg when two spread orders are matched - price is always null] |

#### TRADE_PERIOD - Enumeration

| Enumeration ID   | Enumeration Description   |
|------------------|---------------------------|
| -                | Regular trading           |

#### BOOK_TYPE - Enumeration

|   Enumeration ID | Enumeration Description   |
|------------------|---------------------------|
|                0 | Lit order book            |
|                1 | Off-book                  |

#### MKT_PHASE - Enumeration

| Enumeration ID   | Enumeration Description   |
|------------------|---------------------------|
| 0                | Pre-trading               |
| 1                | Trading                   |
| 2                | Post-trading              |
| 3                | After hours               |
| 4                | Closed                    |
| 8                | Closing price crossing    |
| H                | Halted                    |

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

