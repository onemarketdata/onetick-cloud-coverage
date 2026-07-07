# Canadian Consolidated Equities (all Trades, Quotes, NBBO) Enumerations

Consolidated data from all Canadian equities exchanges, covering Trades, Quotes and NBBO.

The following fields have Enumerations:

* AGGRESSOR_SIDE - Indicates whether a trade resulted from an incoming buy or sell order.
* BOOK_TYPE - Type of order book or trading mechanism through which a trade was executed.
* BUYER - ID of the market participant on the buy side of a trade
* BYPASS - Identifies whether the trade resulted from a Bypass order
* ODD_LOT - Indicates whether a trade was an odd lot
* OMD_STATUS - Indicates an instrument’s current trading status. Values are normalized across all DBs.
* QUOTE_VENUE - Venue (MIC) from which a quote originates
* SELLER - ID of the market participant on the sell side of a trade
* SPECIAL_TERMS - Indicates any non-standard settlement / execution terms associated with a trade
* TRADE_PERIOD - Market period during which a trade was executed.
* TRADE_TYPE - Type of trade
* TRADE_VENUE - Identifies the venue where a trade was executed.   Typically a MIC, with the special values “XOFF” for off-exchange and “SINT” for Systematic Internaliser trades.

#### AGGRESSOR_SIDE - Enumeration

| Enumeration ID   | Enumeration Description                          |
|------------------|--------------------------------------------------|
| ‘””’             | Undefined (e.g. auction trades, off-book trades) |
| B                | Buy                                              |
| S                | Sell                                             |

#### BOOK_TYPE - Enumeration

| Enumeration ID   | Enumeration Description   |
|------------------|---------------------------|
| 0                | Lit order book            |
| 1                | Off-book                  |
| 2                | Dark book                 |
| 3                | Odd lot book              |
| 4                | Special terms book        |
| 6                | Auction book              |
| ‘””’             | Not applicable            |

#### BUYER - Enumeration

|   Enumeration ID | Enumeration Description                                       |
|------------------|---------------------------------------------------------------|
|               10 | StephenAvenue Securities Inc.                                 |
|              100 | TSX Buy-ins                                                   |
|              101 | Societe Generale Capital Canada Inc.                          |
|               11 | Jefferies Securities Inc.                                     |
|              123 | Citigroup Global Markets Canada                               |
|              124 | Questrade Inc.                                                |
|               13 | Instinet Canada Ltd.                                          |
|               14 | Virtu Canada Corp.                                            |
|               15 | UBS Securities Canada Inc./UBS Valeurs Mobilieres Canada Inc. |
|              150 | Generation IACP Inc.                                          |
|               16 | Paradigm Capital Inc.                                         |
|               17 | Integral Wealth Securities Limited                            |
|               19 | Desjardins Securities Inc.                                    |
|                2 | RBC Capital Markets                                           |
|              200 | Acumen Capital Finance Partners Ltd.                          |
|              203 | Assante Capital Management Ltd.                               |
|              205 | Lightyear Capital Inc.                                        |
|              206 | Moomoo Financial Canada Inc                                   |
|              208 | Kingwest and Company                                          |
|               21 | PGM Global Inc.                                               |
|               22 | Fidelity Clearing Canada ULC                                  |
|              222 | JP Morgan Securities Canada Inc.                              |
|               23 | State Street Global Markets Canada Inc.                       |
|               24 | Clarus Securities Inc                                         |
|               25 | Odlum Brown Ltd.                                              |
|               26 | Wells Fargo Securities Canada Ltd.                            |
|               28 | CI Investment Services Inc.                                   |
|                3 | ATB Securities Inc.                                           |
|              300 | CSE Buy-ins                                                   |
|              301 | NEO Buy-ins                                                   |
|               33 | Canaccord Genuity Corp.                                       |
|               34 | Maison Placements Canada Inc.                                 |
|               35 | Friedberg Mercantile Group                                    |
|               36 | W.D. Latimer Co. Ltd.                                         |
|               38 | Liquidnet Canada Inc                                          |
|               39 | Merrill Lynch Canada Inc.                                     |
|                4 | Cantor Fitzgerald Canada Corporation                          |
|               43 | Caldwell Securities Ltd.                                      |
|               48 | Laurentian Bank Securities Inc.                               |
|                5 | Citadel Securities Canada ULC                                 |
|               53 | Morgan Stanley Canada Ltd.                                    |
|               55 | Velocity Trade Capital Ltd.                                   |
|               56 | Edward Jones                                                  |
|               57 | Interactive Brokers Canada Inc                                |
|               59 | Ventum Financial Corp.                                        |
|                6 | INFOR Financial Inc.                                          |
|               62 | Haywood Securities Inc.                                       |
|               65 | Goldman Sachs Canada Inc.                                     |
|               68 | Leede Financial Inc.                                          |
|                7 | TD Securities Inc.                                            |
|               73 | Cormark Securities Inc./Valeurs Mobilieres Cormark Inc.       |
|               76 | iA Private Wealth Inc.                                        |
|               77 | Peters & Co. Ltd.                                             |
|               79 | CIBC World Markets  Inc.                                      |
|               80 | National Bank Financial Inc.                                  |
|               82 | Stifel Nicolaus Canada Inc.                                   |
|               83 | Research Capital Corporation                                  |
|               84 | Independent Trading Group                                     |
|               85 | Scotia Capital Inc.                                           |
|               86 | Pictet Canada L.P.                                            |
|               87 | Beacon Securities Ltd.                                        |
|               88 | Aviso?Financial Inc.                                          |
|               89 | Raymond James Ltd.                                            |
|                9 | BMO Nesbitt Burns Inc.                                        |
|               90 | Barclays Capital Canada Inc.                                  |
|               91 | JonesTrading Canada Inc.                                      |
|               92 | Pollitt & Co. Inc.                                            |
|               94 | Hampton Securities Ltd.                                       |
|               98 | Red Cloud Securites Inc.                                      |

#### BYPASS - Enumeration

| Enumeration ID   | Enumeration Description   |
|------------------|---------------------------|
| ‘””’             | Not a bypass trade        |
| Y                | Bypass trade              |

#### ODD_LOT - Enumeration

| Enumeration ID   | Enumeration Description   |
|------------------|---------------------------|
| ‘””’             | Board lot                 |
| Y                | Odd lot                   |

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

| Enumeration ID   | Enumeration Description             |
|------------------|-------------------------------------|
| CHIC             | Chi-X Canada                        |
| CSE2             | Canadian Securities Exchange        |
| LICA             | Liquidnet Canada                    |
| LYNX             | Lynx                                |
| MATN             | CBOE Canada - MatchNow              |
| NEOD             | CBOE Canada - Neo Dark              |
| NEOE             | CBOE Canada - Neo  L                |
| NEON             | CBOE Canada - Neo  LN               |
| OMGA             | Omega                               |
| PURE             | Canadian Securities Exchange - Pure |
| XATS             | Alpha Exchange                      |
| XATX             | Alpha-X                             |
| XCX2             | CX2                                 |
| XCXD             | Nasdaq CXD                          |
| XICX             | Instinet Canada Cross               |
| XTSE             | Toronto Stock Exchange              |

#### SELLER - Enumeration

|   Enumeration ID | Enumeration Description                                       |
|------------------|---------------------------------------------------------------|
|               10 | StephenAvenue Securities Inc.                                 |
|              100 | TSX Buy-ins                                                   |
|              101 | Societe Generale Capital Canada Inc.                          |
|               11 | Jefferies Securities Inc.                                     |
|              123 | Citigroup Global Markets Canada                               |
|              124 | Questrade Inc.                                                |
|               13 | Instinet Canada Ltd.                                          |
|               14 | Virtu Canada Corp.                                            |
|               15 | UBS Securities Canada Inc./UBS Valeurs Mobilieres Canada Inc. |
|              150 | Generation IACP Inc.                                          |
|               16 | Paradigm Capital Inc.                                         |
|               17 | Integral Wealth Securities Limited                            |
|               19 | Desjardins Securities Inc.                                    |
|                2 | RBC Capital Markets                                           |
|              200 | Acumen Capital Finance Partners Ltd.                          |
|              203 | Assante Capital Management Ltd.                               |
|              205 | Lightyear Capital Inc.                                        |
|              206 | Moomoo Financial Canada Inc                                   |
|              208 | Kingwest and Company                                          |
|               21 | PGM Global Inc.                                               |
|               22 | Fidelity Clearing Canada ULC                                  |
|              222 | JP Morgan Securities Canada Inc.                              |
|               23 | State Street Global Markets Canada Inc.                       |
|               24 | Clarus Securities Inc                                         |
|               25 | Odlum Brown Ltd.                                              |
|               26 | Wells Fargo Securities Canada Ltd.                            |
|               28 | CI Investment Services Inc.                                   |
|                3 | ATB Securities Inc.                                           |
|              300 | CSE Buy-ins                                                   |
|              301 | NEO Buy-ins                                                   |
|               33 | Canaccord Genuity Corp.                                       |
|               34 | Maison Placements Canada Inc.                                 |
|               35 | Friedberg Mercantile Group                                    |
|               36 | W.D. Latimer Co. Ltd.                                         |
|               38 | Liquidnet Canada Inc                                          |
|               39 | Merrill Lynch Canada Inc.                                     |
|                4 | Cantor Fitzgerald Canada Corporation                          |
|               43 | Caldwell Securities Ltd.                                      |
|               48 | Laurentian Bank Securities Inc.                               |
|                5 | Citadel Securities Canada ULC                                 |
|               53 | Morgan Stanley Canada Ltd.                                    |
|               55 | Velocity Trade Capital Ltd.                                   |
|               56 | Edward Jones                                                  |
|               57 | Interactive Brokers Canada Inc                                |
|               59 | Ventum Financial Corp.                                        |
|                6 | INFOR Financial Inc.                                          |
|               62 | Haywood Securities Inc.                                       |
|               65 | Goldman Sachs Canada Inc.                                     |
|               68 | Leede Financial Inc.                                          |
|                7 | TD Securities Inc.                                            |
|               73 | Cormark Securities Inc./Valeurs Mobilieres Cormark Inc.       |
|               76 | iA Private Wealth Inc.                                        |
|               77 | Peters & Co. Ltd.                                             |
|               79 | CIBC World Markets  Inc.                                      |
|               80 | National Bank Financial Inc.                                  |
|               82 | Stifel Nicolaus Canada Inc.                                   |
|               83 | Research Capital Corporation                                  |
|               84 | Independent Trading Group                                     |
|               85 | Scotia Capital Inc.                                           |
|               86 | Pictet Canada L.P.                                            |
|               87 | Beacon Securities Ltd.                                        |
|               88 | Aviso?Financial Inc.                                          |
|               89 | Raymond James Ltd.                                            |
|                9 | BMO Nesbitt Burns Inc.                                        |
|               90 | Barclays Capital Canada Inc.                                  |
|               91 | JonesTrading Canada Inc.                                      |
|               92 | Pollitt & Co. Inc.                                            |
|               94 | Hampton Securities Ltd.                                       |
|               98 | Red Cloud Securites Inc.                                      |

#### SPECIAL_TERMS - Enumeration

| Enumeration ID   | Enumeration Description                |
|------------------|----------------------------------------|
| ‘””’             | No special terms (standard settlement) |
| C                | Cash                                   |
| CT               | Cash today                             |
| DC               | Derivative-related contingent trade    |
| DD               | Delayed delivery                       |
| ND               | Next day                               |
| NN               | Non-net                                |
| NR               | Non-resident                           |
| Y                | Special settlement terms               |

#### TRADE_PERIOD - Enumeration

| Enumeration ID   | Enumeration Description                 |
|------------------|-----------------------------------------|
| -                | Regular trading                         |
| A                | Auction                                 |
| C                | Closing auction                         |
| E                | Extended hours (early session)          |
| I                | Intraday auction                        |
| L                | Extended hours (late session)           |
| O                | Opening auction                         |
| P                | Public offering / buyback auction       |
| T                | Trading at closing price                |
| U                | Unscheduled auction                     |
| c                | Post-close auction                      |
| e                | Extended hours                          |
| o                | Opening auction (extended hours)        |
| p                | Auction initiated by market participant |
| u                | Unscheduled auction (extended hours)    |
| ‘””’             | Not applicable                          |

#### TRADE_TYPE - Enumeration

| Enumeration ID   | Enumeration Description                                                    |                                         |
|------------------|----------------------------------------------------------------------------|-----------------------------------------|
|                  | ‘Values are exchange-specific - e.g. if the CLOUD_DB field is set to “TSX” | refer to the TRADE_TYPE values for TSX’ |

