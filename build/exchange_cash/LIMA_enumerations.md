# Lima Stock Exchange Enumerations

Trades, quotes and bars from the Lima Stock Exchange (Bolsa de Valores de Lima, BVL), Peru’s stock exchange, with history from June 2016. BVL lists many mining companies, and covered stocks include constituents of the S&P/BVL Peru General and S&P/BVL Lima 25 indices. BVL is now part of the nuam regional exchange group with the Santiago and Colombia exchanges.

The following fields have Enumerations:

* OMD_STATUS - Indicates an instrument’s current trading status. Values are normalized across all DBs.
* TRADE_PERIOD - Market period during which a trade was executed.
* TRADE_TYPE - Type of trade

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

| Enumeration ID   | Enumeration Description       |
|------------------|-------------------------------|
| -                | Regular trading               |
| A                | Auction                       |
| C                | Closing auction               |
| I                | Intraday auction              |
| O                | Opening auction               |
| P                | IPO / Public offering auction |
| T                | Trading at closing price      |
| U                | Unscheduled auction           |

#### TRADE_TYPE - Enumeration

| Enumeration ID   | Enumeration Description                        |
|------------------|------------------------------------------------|
| 0                | Significant trade                              |
| 1                | Insignificant trade                            |
| 2                | Auction trade (significant)                    |
| 3                | Auction trade (insignificant)                  |
| 4                | Trade on hidden order quantity (significant)   |
| 5                | Trade on hidden order quantity (insignificant) |
| AU               | Special auction trade                          |
| BK               | Block trade                                    |
| ES               | Early settlement trade                         |
| RP               | Repo trade                                     |

