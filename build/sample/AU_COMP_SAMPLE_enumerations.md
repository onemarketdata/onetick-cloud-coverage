# Australian Consolidated Equities Sample Enumerations

A sample of the AU_COMP consolidated tape database covering a subset of symbols across all Australian equity venues (ASX and Cboe Australia), between January 2, 2024 and March 31, 2024. It includes consolidated trades, NBBO, quotes and bars, so you can test cross-venue analysis of ASX-listed stocks before subscribing to the full history from 2008. The full database covers constituents of the S&P/ASX 200 and All Ordinaries.

The following fields have Enumerations:

* BOOK_TYPE - Type of order book or trading mechanism through which a trade was executed.
* OMD_STATUS - Indicates an instrument’s current trading status. Values are normalized across all DBs.
* QUOTE_VENUE - Venue (MIC) from which a quote originates
* TRADE_PERIOD - Market period during which a trade was executed.
* TRADE_TYPE - Type of trade
* TRADE_VENUE - Identifies the venue where a trade was executed.   Typically a MIC, with the special values “XOFF” for off-exchange and “SINT” for Systematic Internaliser trades.

#### BOOK_TYPE - Enumeration

|   Enumeration ID | Enumeration Description   |
|------------------|---------------------------|
|                0 | Lit order book            |
|                1 | Off-book                  |
|                2 | Dark book                 |

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

#### QUOTE_VENUE - Enumeration

| Enumeration ID   | Enumeration Description   |
|------------------|---------------------------|
| CHIA             | Chi-X Australia           |
| XASX             | ASX                       |

#### TRADE_PERIOD - Enumeration

| Enumeration ID   | Enumeration Description   |
|------------------|---------------------------|
| -                | Regular trading           |
| C                | Closing auction           |
| O                | Opening auction           |
| T                | Trading at closing price  |
| U                | Unscheduled auction       |

#### TRADE_TYPE - Enumeration

| Enumeration ID   | Enumeration Description   |
|------------------|---------------------------|
| ‘””’             | As for underlying venues  |

#### TRADE_VENUE - Enumeration

| Enumeration ID   | Enumeration Description   |
|------------------|---------------------------|
| CHIA             | Chi-X Australia           |
| XASX             | ASX                       |

