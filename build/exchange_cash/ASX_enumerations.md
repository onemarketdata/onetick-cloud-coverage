# Australian Stock Exchange Enumerations

Trades, quotes and bars from the Australian Securities Exchange (ASX), with history from May 2008. ASX is Australia’s primary listing venue for equities, ETFs, hybrids and warrants, and its opening and closing auctions set official prices for S&P/ASX 200 and All Ordinaries constituents. For the Australian Equity consolidated tape including TMX Australia Exchange (formerly Cboe Australia) as well, use AU_COMP.

The following fields have Enumerations:

* BOOK_TYPE - Type of order book or trading mechanism through which a trade was executed.
* MKT_PHASE - Indicates the instrument’s current market phase, as specified by the trading venue
* OMD_STATUS - Indicates an instrument’s current trading status. Values are normalized across all DBs.
* TRADE_PERIOD - Market period during which a trade was executed.
* TRADE_REPORT_TYPE - Additional detail on the source of an off-book (reported) trade
* TRADE_TYPE - Type of trade

#### BOOK_TYPE - Enumeration

|   Enumeration ID | Enumeration Description   |
|------------------|---------------------------|
|                0 | Lit order book            |
|                1 | Off-book                  |
|                2 | Dark book                 |

#### MKT_PHASE - Enumeration

|   Enumeration ID | Enumeration Description             |
|------------------|-------------------------------------|
|                8 | OPEN / Normal Trading               |
|               14 | CSPA (Closing Single Price Auction) |
|               12 | Pre-CSPA                            |
|                5 | PRE-OPEN                            |
|               23 | OSPA (Opening Single Price Auction) |
|                2 | ADJUST                              |
|                4 | CLOSE                               |
|               24 | POST CLOSE                          |
|               10 | PRE-NR (Pre-Notice Received)        |
|               25 | DONE FOR DAY                        |

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
| C                | Closing auction           |
| O                | Opening auction           |
| T                | Trading at closing price  |
| U                | Unscheduled auction       |

#### TRADE_REPORT_TYPE - Enumeration

| Enumeration ID   | Enumeration Description                      |
|------------------|----------------------------------------------|
| ‘””’             | Not applicable                               |
| 0                | Regular trade / not applicable               |
| 10               | Special crossing tier 1                      |
| 100              | NBBO cross                                   |
| 11               | Special crossing tier 2                      |
| 12               | Special crossing tier 3                      |
| 13               | Late trade report reason code a              |
| 14               | Late trade report reason code b              |
| 15               | Late trade report reason code c              |
| 16               | Late trade report reason code d              |
| 17               | Late trade report reason code e              |
| 2                | Cross                                        |
| 3                | Derivatives special cross                    |
| 30               | Equity/option combination                    |
| 31               | Tailor made combination                      |
| 32               | Tailor made combination crossing             |
| 33               | Late combination trade                       |
| 35               | OTC contingent equity trade                  |
| 4                | Late                                         |
| 40               | Buyback                                      |
| 41               | Booking purposes                             |
| 43               | Directed reporting                           |
| 44               | Option exercise (call)                       |
| 45               | Option exercise (put)                        |
| 46               | ETF special trade                            |
| 47               | Forward delivery                             |
| 5                | Overseas                                     |
| 50               | Loan                                         |
| 51               | Loan return                                  |
| 52               | Non-screen traded government instrument      |
| 53               | Non-screen traded wholesale                  |
| 54               | Foreign to foreign                           |
| 58               | Price stabilisation                          |
| 59               | Price stabilisation late trade               |
| 60               | Portfolio special crossing                   |
| 61               | Price stabilisation late trade reason code a |
| 62               | Price stabilisation late trade reason code b |
| 63               | Price stabilisation late trade reason code c |
| 64               | Price stabilisation late trade reason code d |
| 65               | Price stabilisation late trade reason code e |
| 66               | Put-through special cross ($1M)              |
| 67               | Put-through special cross ($0.5M)            |
| 70               | Quote display board trade report             |
| 8                | Price stabilisation / green shoe order       |
| 9                | Special combo contingent                     |

#### TRADE_TYPE - Enumeration

| Enumeration ID   | Enumeration Description                                                                          |
|------------------|--------------------------------------------------------------------------------------------------|
| 0                | Regular trade                                                                                    |
| 1                | Trade report - Different participants [until 20250630]                                           |
| 10               | Internal trade + buy-write                                                                       |
| 11               | Tailor-Made Derivatives / Cash Combo to Combo accidental crossing [until 20250630]               |
| 12               | Bulletin Board Derivatives / Cash Combo to Combo [until 20250630]                                |
| 14               | Bulletin Board Derivatives / Cash Combo to Combo accidental crossing [until 20250630]            |
| 2                | Internal trade                                                                                   |
| 20               | Volume match book trade, different broker for buy and sell [until 20250630]                      |
| 21               | Volume match book trade, same broker for buy and sell [until 20250630]                           |
| 24               | Centre Point Priority Crossing [until 20250630]                                                  |
| 25               | Centre Point Trade                                                                               |
| 26               | Centre Point Unintentional Crossing                                                              |
| 27               | NBBO Cross                                                                                       |
| 28               | Any Price Block Trade - same participant [until 20250630]                                        |
| 29               | Any Price Block Trade - different participants [until 20250630]                                  |
| 3                | Trade report - Single participant [until 20250630]                                               |
| 30               | Preferenced Any Price Block Crossing - same participant [until 20250630]                         |
| 4                | Bulletin Board trade [until 20250630]                                                            |
| 5                | Centre point preference matched trade [until 20250630]                                           |
| 6                | Bulletin Board Derivatives Only or Cash Only Combo to Combo accidental crossing [until 20250630] |
| 8                | Buy-write                                                                                        |
| 9                | Trade report - Buy-write                                                                         |
| TR               | Trade report                                                                                     |

