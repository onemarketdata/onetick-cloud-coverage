# Johannesburg Stock Exchange Enumerations

The Johannesburg Stock Exchange is the largest stock exchange in Africa, trading South African stocks across sectors.

The following fields have Enumerations:

* BOOK_TYPE - Type of order book or trading mechanism through which a trade was executed.
* EVENT_CODE - Event that triggered an instrument status update
* MKT_PHASE - Indicates the instrument’s current market phase, as specified by the trading venue
* REASON_CODE - Reason for an instrument status update
* TRADE_PERIOD - Market period during which a trade was executed.
* TRADE_TYPE - Type of trade

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

