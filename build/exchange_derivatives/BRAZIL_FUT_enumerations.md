# B3 - Derivatives (BM&F) Enumerations

Futures, options and spreads with bars from B3’s listed derivatives segment (formerly BM&F), with futures from December 2009 and options from January 2024. Key contracts include Ibovespa and mini-Ibovespa index futures, US dollar and mini-dollar futures, DI1 interbank rate futures and agricultural futures such as live cattle and coffee.

The following fields have Enumerations:

* BOOK_TYPE - Type of order book or trading mechanism through which a trade was executed.
* CALL_PUT_IND - “C” - Call option, “P” - Put option
* OMD_STATUS - Indicates an instrument’s current trading status. Values are normalized across all DBs.
* TRADE_PERIOD - Market period during which a trade was executed.
* TRADE_SESSION - Trading session from which a trade originates, e.g. “Day”, “Night”
* TRADE_TYPE - Type of trade

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
| I                | Intraday auction          |
| O                | Opening auction           |
| U                | Unscheduled auction       |

#### TRADE_SESSION - Enumeration

| Enumeration ID   | Enumeration Description    |
|------------------|----------------------------|
| Ext              | Extended hours T+0 trading |
| T+0              | Regular hours (T+0)        |
| T+1              | After-hours T+1 trading    |

#### TRADE_TYPE - Enumeration

|   Enumeration ID | Enumeration Description                                       |
|------------------|---------------------------------------------------------------|
|                0 | Regular trade                                                 |
|                1 | Cross trade                                                   |
|               24 | After-hours trade                                             |
|               25 | Retail Liquidity trade                                        |
|               26 | Out of sequence trade [e.g. reinsertion of a cancelled trade] |

