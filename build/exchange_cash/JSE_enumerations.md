# Johannesburg Stock Exchange Enumerations

Trades, quotes and bars from the Johannesburg Stock Exchange (JSE), Africa’s largest stock exchange, with history from February 2015, covering the Main Board and AltX for smaller companies. Many JSE companies are also listed in London. Covered stocks include constituents of the FTSE/JSE Top 40 and All Share indices.

The following fields have Enumerations:

* AUCTION_TYPE - Type of auction from which an indicative auction price / auction imbalance originates.
* BOOK_TYPE - Type of order book or trading mechanism through which a trade was executed.
* EVENT_CODE - Event that triggered an instrument status update
* MKT_PHASE - Indicates the instrument’s current market phase, as specified by the trading venue
* OMD_STATUS - Indicates an instrument’s current trading status. Values are normalized across all DBs.
* REASON_CODE - Reason for an instrument status update
* TRADE_PERIOD - Market period during which a trade was executed.
* TRADE_TYPE - Type of trade

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
|                6 | Auction book              |

#### EVENT_CODE - Enumeration

| Enumeration ID   | Enumeration Description   |
|------------------|---------------------------|
| ‘””’             | Unspecified               |
| 0                | Scheduled transition      |
| 1                | Extended by Market Ops    |
| 2                | Shortened by Market Ops   |
| 3                | Market order imbalance    |
| 4                | Price outside range       |
| 5                | Circuit breaker           |
| 9                | Unspecified               |

#### MKT_PHASE - Enumeration

| Enumeration ID   | Enumeration Description   |
|------------------|---------------------------|
| a                | Opening auction call      |
| b                | Post-close                |
| c                | Market close              |
| d                | Closing auction call      |
| E                | EOD volume auction call   |
| e                | Volatility auction call   |
| f                | Re-opening auction call   |
| H                | Halted                    |
| I                | Inactive                  |
| l                | Pause                     |
| p                | Futures close out auction |
| s                | Closing price crossing    |
| S                | Suspended                 |
| T                | Regular trading           |
| u                | Intraday auction call     |
| v                | End of trade reporting    |
| w                | No active session         |
| x                | End of post-close         |
| y                | Pre-trading               |
| z                | Closing price publication |

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

#### REASON_CODE - Enumeration

| Enumeration ID   | Enumeration Description            |
|------------------|------------------------------------|
| ‘””’             | Unspecified                        |
| 1                | System issues                      |
| 101              | Instrument-level circuit breaker   |
| 102              | Halted                             |
| 2                | Company announcement expected      |
| 3                | Halt requested by company          |
| 4                | Suspension requested by company    |
| 5                | Halt / suspension initiated by JSE |
| 9998             | Matching partition suspended       |
| 9999             | System suspended                   |

#### TRADE_PERIOD - Enumeration

| Enumeration ID   | Enumeration Description   |
|------------------|---------------------------|
| -                | Regular trading           |
| A                | Auction                   |
| C                | Closing auction           |
| I                | Intraday auction          |
| O                | Opening auction           |
| T                | Trading at closing price  |
| U                | Unscheduled auction       |

#### TRADE_TYPE - Enumeration

| Enumeration ID   | Enumeration Description                   |
|------------------|-------------------------------------------|
| A                | Auction trade (volatility auction)        |
| AT               | Automated trade                           |
| BK               | Book build trade                          |
| BT               | Block trade                               |
| C                | Auction trade (closing auction)           |
| CF               | Corporate finance trade                   |
| E                | Auction trade (re-opening auction)        |
| HO               | Automated trade against hidden order      |
| K                | Auction trade (intraday auction)          |
| L                | Auction trade (futures close out auction) |
| LC               | Off-book post contra trade                |
| LT               | Late trade                                |
| O                | Auction trade (opening auction)           |
| OP               | Off order book principal trade            |
| PC               | On-book post contra trade                 |
| PF               | Portfolio trade                           |
| UT               | Uncrossing trade [until 20210531]         |
| VT               | EOD volume auction                        |
| XT               | Cross trade                               |

