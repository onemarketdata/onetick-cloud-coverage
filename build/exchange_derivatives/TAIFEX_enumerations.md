# Taiwan Futures Exchange (TAIFEX) Enumerations

Futures, options and spreads from the Taiwan Futures Exchange (TAIFEX), with history from March 2026. Established in 1998, TAIFEX is Taiwan’s derivatives exchange; its flagship TAIEX options (TXO) are among the world’s most heavily traded equity index options, alongside TAIEX futures (TX) and mini and micro TAIEX futures (MTX, TMF). It also lists equity options and futures and government bond futures.

The following fields have Enumerations:

* AGGRESSOR_SIDE - Indicates whether a trade resulted from an incoming buy or sell order.
* AUCTION_TYPE - Type of auction from which an indicative auction price / auction imbalance originates.
* TRADE_TYPE - Type of trade
* TRADE_PERIOD - Market period during which a trade was executed.
* BOOK_TYPE - Type of order book or trading mechanism through which a trade was executed.
* CALL_PUT_IND - “C” - Call option, “P” - Put option
* TRADE_SESSION - Trading session from which a trade originates, e.g. “Day”, “Night”
* QUOTE_SESSION - Trading session from which the quote originates, e.g. “Day”, “Night”
* SESSION - Trading session to which the update relates, e.g. “Day”, “Night”, “T”, “T+1”
* MKT_PHASE - Indicates the instrument’s current market phase, as specified by the trading venue
* OMD_STATUS - Indicates an instrument’s current trading status. Values are normalized across all DBs.
* EVENT_CODE - Event that triggered an instrument status update

#### AGGRESSOR_SIDE - Enumeration

| Enumeration ID   | Enumeration Description                                      |
|------------------|--------------------------------------------------------------|
| ‘””’             | Undefined (e.g. auction trades, leg trades, off-book trades) |
| B                | Buy                                                          |
| S                | Sell                                                         |

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

#### TRADE_TYPE - Enumeration

| Enumeration ID   | Enumeration Description   |
|------------------|---------------------------|
| ‘””’             | Regular trade             |
| LEG              | Strategy leg trade        |

#### TRADE_PERIOD - Enumeration

| Enumeration ID   | Enumeration Description   |
|------------------|---------------------------|
| A                | Auction                   |
| -                | Regular trading           |

#### BOOK_TYPE - Enumeration

| Enumeration ID   | Enumeration Description                                                                  |
|------------------|------------------------------------------------------------------------------------------|
| 0                | Lit order book                                                                           |
| S                | Strategy leg [trade reported in each of outright leg when two spread orders are matched] |

#### CALL_PUT_IND - Enumeration

| Enumeration ID   | Enumeration Description   |
|------------------|---------------------------|
| C                | Call option               |
| P                | Put option                |

#### TRADE_SESSION - Enumeration

| Enumeration ID   | Enumeration Description   |
|------------------|---------------------------|
| Day              | Day session               |
| Night            | Night session             |

#### QUOTE_SESSION - Enumeration

| Enumeration ID   | Enumeration Description   |
|------------------|---------------------------|
| Day              | Day session               |
| Night            | Night session             |

#### SESSION - Enumeration

| Enumeration ID   | Enumeration Description   |
|------------------|---------------------------|
| Day              | Day session               |
| Night            | Night session             |

#### MKT_PHASE - Enumeration

|   Enumeration ID | Enumeration Description   |
|------------------|---------------------------|
|              200 | Suspended                 |
|              302 | Accepting orders          |
|              304 | Open                      |
|              305 | Non-cancel period         |
|              306 | Cloed                     |

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

#### EVENT_CODE - Enumeration

|   Enumeration ID | Enumeration Description                                   |
|------------------|-----------------------------------------------------------|
|              100 | Circuit breaker cooling-off period                        |
|              101 | Price limits expanded after circuit breaker               |
|              400 | Dynamic price banding suspended                           |
|              401 | Dynamic price banding resumed                             |
|              402 | Dynamic price banding range adjusted                      |
|              403 | Dynamic price banding suspension preliminary notification |
|              404 | Dynamic price banding resumption preliminary notification |
|              405 | Dynamic price banding adjustment preliminary notification |

