# India Consolidated Equities Enumerations

Consolidated data from all Indian equities exchanges.

The following fields have Enumerations:

* AGGRESSOR_SIDE - Indicates whether a trade resulted from an incoming buy or sell order.
* BOOK_TYPE - Type of order book or trading mechanism through which a trade was executed.
* OMD_STATUS - Indicates an instrument’s current trading status. Values are normalized across all DBs.
* QUOTE_VENUE - Venue (MIC) from which a quote originates
* TRADE_PERIOD - Market period during which a trade was executed.
* TRADE_TYPE - Type of trade
* TRADE_VENUE - Identifies the venue where a trade was executed.   Typically a MIC, with the special values “XOFF” for off-exchange and “SINT” for Systematic Internaliser trades.

#### AGGRESSOR_SIDE - Enumeration

| Enumeration ID   | Enumeration Description         |
|------------------|---------------------------------|
| ‘””’             | Undefined (e.g. auction trades) |
| B                | Buy                             |
| S                | Sell                            |

#### BOOK_TYPE - Enumeration

|   Enumeration ID | Enumeration Description   |
|------------------|---------------------------|
|                0 | Lit order book            |
|                1 | Off-book                  |
|                3 | Odd lot book              |

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

| Enumeration ID   | Enumeration Description          |
|------------------|----------------------------------|
| XBOM             | Bombay Stock Exchange            |
| XNSE             | National Stock Exchange of India |

#### TRADE_PERIOD - Enumeration

| Enumeration ID   | Enumeration Description   |
|------------------|---------------------------|
| -                | Regular trading           |
| I                | Intraday auction          |
| O                | Opening auction           |
| T                | Trading at closing price  |

#### TRADE_TYPE - Enumeration

| Enumeration ID   | Enumeration Description   |
|------------------|---------------------------|
| ‘””’             | As for underlying venues  |

#### TRADE_VENUE - Enumeration

| Enumeration ID   | Enumeration Description          |
|------------------|----------------------------------|
| XBOM             | Bombay Stock Exchange            |
| XNSE             | National Stock Exchange of India |

