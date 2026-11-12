# Stock Exchange of Thailand Enumerations

Trades, quotes, bars and book depth from the Stock Exchange of Thailand (SET), with history from September 2014, covering the SET main board and the Market for Alternative Investment (mai). Index data includes the SET Index, SET50 and SET100.

The following fields have Enumerations:

* AUCTION_TYPE - Type of auction from which an indicative auction price / auction imbalance originates.
* BOOK_TYPE - Type of order book or trading mechanism through which a trade was executed.
* MKT_PHASE - Indicates the instrument’s current market phase, as specified by the trading venue
* OMD_STATUS - Indicates an instrument’s current trading status. Values are normalized across all DBs.
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
|                3 | Odd lot book              |

#### MKT_PHASE - Enumeration

| Enumeration ID    | Enumeration Description                                     |
|-------------------|-------------------------------------------------------------|
| AUTO_PAUSE_E      | Trading pause (due to unusually high order volume)          |
| CIRCUIT_BREAKER_E | Circuit breaker                                             |
| CLOSE_E           | Closed                                                      |
| CLOSE_L           | Closed                                                      |
| DAY_E             | Continuous trading (day session)                            |
| EXPIRED_E         | Expired                                                     |
| FREEZE1_E         | Freeze (no orderbook access or trade reporting)             |
| FREEZE2_E         | Freeze (no orderbook access or trade reporting)             |
| FREEZE3_E         | Freeze (no orderbook access or trade reporting)             |
| FULLHALT_E        | Halted, no orderbook access                                 |
| FULLHALT_L        | Halted, no orderbook access                                 |
| HALT_E            | Halted                                                      |
| HALT_L            | Halted                                                      |
| HALT_N_E          | Halted (no trade reporting)                                 |
| INTERMISSION_E    | Intermission (break between morning + afternoon sessions)   |
| INTERMISSION1_E   | Intermission (break after end of day session)               |
| INTERMISSION2_E   | Intermission (break before start of night session)          |
| MARKETCLOSE_E     | Market close                                                |
| MARKETCLOSE_L     | Market close                                                |
| NIGHT_E           | Continuous trading (night session)                          |
| NO-MATCHING1_E    | No order matching                                           |
| NO-MATCHING2_E    | No order matching                                           |
| OFF-HOUR_E        | Post-market                                                 |
| OFF-HOUR_L        | Post-market                                                 |
| OPEN_E            | Continuous trading                                          |
| OPEN1_E           | Continuous trading (morning session)                        |
| OPEN2_E           | Continuous trading (afternoon session)                      |
| PAUSE_E           | Pause                                                       |
| PRE-CLOSE_E       | Closing auction                                             |
| PRE-CLOSE1_E      | Closing auction (night session)                             |
| PRE-DAY_E         | Pre-open (day session)                                      |
| PRE-NIGHT_E       | Pre-open (night session)                                    |
| PRE-OPEN_CB_E     | Re-opening auction (after instrument-level circuit breaker) |
| PRE-OPEN_E        | Pre-open                                                    |
| PRE-OPEN_L        | Pre-open                                                    |
| PRE-OPEN1_E       | Pre-open (morning session)                                  |
| PRE-OPEN2_E       | Pre-open (afternoon session)                                |
| PRE_OPEN_P_E      | Re-opening auction (after a trading pause)                  |
| RESET_STAT_E      | Reset statistics at end of day                              |
| RESET_STAT_L      | Reset statistics at end of day                              |
| SAVECLOSING_E     | Closing price calculation                                   |
| SAVECLOSING_L     | Closing price calculation                                   |
| STARTUP_E         | Start of day                                                |
| STARTUP_L         | Start of day                                                |
| SUSPEND_E         | Suspended                                                   |
| SUSPEND_L         | Suspended                                                   |
| SUSPEND_N_E       | Suspended (no trade reporting)                              |
| TRANSITION1_E     | End of morning session                                      |
| TRANSITION2_E     | End of afternoon session                                    |
| TRANSITION3_E     | End of night session                                        |

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
| I                | Intraday auction          |
| O                | Opening auction           |
| U                | Unscheduled auction       |

#### TRADE_TYPE - Enumeration

|   Enumeration ID | Enumeration Description       |
|------------------|-------------------------------|
|                0 | Regular trade                 |
|                1 | Trade report                  |
|                2 | Auction trade                 |
|                4 | Odd lot trade [from 20200113] |
|                5 | Trade report [until 20200110] |

