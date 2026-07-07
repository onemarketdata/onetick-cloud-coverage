# Taiwan Consolidated Equities Enumerations

Consolidated data from all Taiwan equities exchanges.

The following fields have Enumerations:

* ASK_COND - Quote condition applicable to the best ask
* BID_COND - Quote condition applicable to the best bid
* BOOK_TYPE - Type of order book or trading mechanism through which a trade was executed.
* OMD_STATUS - Indicates an instrument’s current trading status. Values are normalized across all DBs.
* QUOTE_VENUE - Venue (MIC) from which a quote originates
* TRADE_PERIOD - Market period during which a trade was executed.
* TRADE_TYPE - Type of trade
* TRADE_VENUE - Identifies the venue where a trade was executed.   Typically a MIC, with the special values “XOFF” for off-exchange and “SINT” for Systematic Internaliser trades.

#### ASK_COND - Enumeration

| Enumeration ID   | Enumeration Description   |
|------------------|---------------------------|
| ‘””’             | No condition              |
| 1                | Ask price on lower limit  |
| 2                | Ask price on upper limit  |

#### BID_COND - Enumeration

| Enumeration ID   | Enumeration Description   |
|------------------|---------------------------|
| ‘””’             | No condition              |
| 1                | Bid price on lower limit  |
| 2                | Bid price on upper limit  |

#### BOOK_TYPE - Enumeration

|   Enumeration ID | Enumeration Description   |
|------------------|---------------------------|
|                0 | Lit order book            |
|                1 | Off-book                  |
|                3 | Odd lot book              |
|                6 | Auction book              |

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
| ROCO             | Taipei Exchange           |
| XTAI             | Taiwan Stock Exchange     |

#### TRADE_PERIOD - Enumeration

| Enumeration ID   | Enumeration Description                          |
|------------------|--------------------------------------------------|
