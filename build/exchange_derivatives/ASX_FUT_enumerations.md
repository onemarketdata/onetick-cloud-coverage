# ASX 24 (Sydney Futures Exchange) Enumerations

Futures and spreads with bars from ASX 24 (formerly the Sydney Futures Exchange), with history from April 2011. Key contracts include the SPI 200 equity index future, 3-year and 10-year Australian Treasury bond futures, 90-day bank bill futures and 30-day interbank cash rate futures, plus electricity and agricultural contracts.

The following fields have Enumerations:

* BOOK_TYPE - Type of order book or trading mechanism through which a trade was executed.
* OMD_STATUS - Indicates an instrument’s current trading status. Values are normalized across all DBs.
* TRADE_PERIOD - Market period during which a trade was executed.
* TRADE_TYPE - Type of trade

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

#### TRADE_PERIOD - Enumeration

| Enumeration ID   | Enumeration Description   |
|------------------|---------------------------|
| -                | Regular trading           |
| I                | Intraday auction          |
| O                | Opening auction           |
| U                | Unscheduled auction       |

#### TRADE_TYPE - Enumeration

|   Enumeration ID | Enumeration Description                           |
|------------------|---------------------------------------------------|
|                0 | Regular trade                                     |
|                1 | Auction trade [prior to 20170319: Sweeping trade] |
|                2 | Levelling trade [until 20170320]                  |
|                3 | Spread to underlying trade                        |
|                4 | Spread to spread trade                            |
|                5 | Inter-product spread trade                        |
|                6 | Strip to strip trade                              |
|                7 | Strip to outright trade                           |

