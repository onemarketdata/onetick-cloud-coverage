# Euronext Oslo - Equities Enumerations

The Oslo Stock Exchange (Oslo Bors) is the only regulated market for trading equities, equity certificates and bonds in Norway.

The following fields have Enumerations:

* AGGRESSOR_SIDE - Indicates whether a trade resulted from an incoming buy or sell order.
* BOOK_TYPE - Type of order book or trading mechanism through which a trade was executed.
* MKT_PHASE (before 20201130) -
* MKT_PHASE (from 20201130) - Byte 1 (Orderbook state) -
* MKT_PHASE (from 20201130) - Byte 2 (Market period) -
* MKT_PHASE (from 20201130) - Byte 3 (Phase qualifier) -
* MKT_PHASE (from 20201130) - Byte 1 (Orderbook state) -
* MKT_PHASE (from 20201130) - Byte 3 (Phase qualifier) -
* MKT_PHASE (from 20201130) - Byte 1 (Orderbook state) -
* MKT_PHASE (from 20201130) - Byte 2 (Market period) -
* MKT_PHASE (from 20201130) - Byte 1 (Orderbook state) -
* MKT_PHASE (from 20201130) - Byte 2 (Market period) -
* MKT_PHASE (from 20201130) - Byte 3 (Phase qualifier) -
* MKT_PHASE (from 20201130) - Byte 2 (Market period) -
* MKT_PHASE (from 20201130) - Byte 1 (Orderbook state) -
* MKT_PHASE (from 20201130) - Byte 3 (Phase qualifier) -
* MKT_PHASE (from 20201130) - Byte 1 (Orderbook state) -
* MMT_ALGO_IND - Identifies whether a trade involved an algorithmic order.
* MMT_BENCHMARK_IND - Identifies whether a trade was priced according to a defined benchmark (e.g. VWAP) or reference price (e.g. midpoint of the primary market BBO), or whether it was part of a trade in multiple instruments (contingent trade or portfolio trade).
* MMT_CROSS_IND - Identifies agency cross trades, where a broker crossed two client orders outside the order book.
* MMT_DEFERRAL_TYPE - Type of publication deferral or subsequent enrichment applied to a trade report.
* MMT_DIVIDEND_IND - Identifies whether a trade includes special dividend arrangements, e.g. a trade sold cum-dividend during an ex-dividend period.
* MMT_DUP_IND - Identifies trades reported to more than one Approved Publication Arrangement.
* MMT_MKT_MECH - Market mechanism through which a trade was executed.
* MMT_MOD_IND - Identifies trade cancellations, or amendments of a previous trade.
* MMT_NEGOTIATED_IND - Indicates privately negotiated trades, or Systematic Internaliser trades exempt from pre-trade transparency.
* MMT_OFF_BOOK_AUTO_IND - Identifies whether an off-book trade report was executed via a manual or automated process.
* MMT_PRICE_FORMING_IND - Identifies whether a trade is price-forming, or contributes to the price discovery process.
* MMT_PUB_MODE - Identifies whether a trade was subject to delayed publication, and the reason for the deferral.
* MMT_TRANS_CAT - Identifies various special categories of trade.
* MMT_TRD_MODE - Trading period during which an on-book trade was executed, or origin of an off-book trade report (on-exchange / off-exchange / SI).
* ORDER_ENTRY_STATUS - Indicates the availability of order entry / modification / cancellation
* ORDER_TYPE - Type of order.
* REASON_CODE - Reason for an instrument status update
* TRADE_PERIOD - Market period during which a trade was executed.
* TRADE_TYPE - Type of trade
* UPDATE_TYPE - Type of update

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
| R                | Request for Quote         |
| ‘””’             | Not applicable            |

#### MKT_PHASE (before 20201130) - Enumeration

|   Enumeration ID | Enumeration Description       |
|------------------|-------------------------------|
|              100 | Pre-trading                   |
|              102 | Closing auction call          |
|              103 | End of post-close             |
|              104 | Re-opening auction call       |
|              106 | Pre-open order entry          |
|              107 | Pre-closing order entry       |
|              108 | Issuing/buyback auction call  |
|              109 | Admin                         |
|              110 | Issuing/buyback special entry |
|              111 | Pause                         |
|              113 | Order entry                   |
|              125 | Closing price publication     |
|              126 | Pre-trading                   |
|              127 | Intraday auction call         |
|               17 | Regular trading               |
|               18 | Closed                        |
|                2 | Halted                        |
|               21 | Opening auction call          |
|               26 | Post-close                    |

#### MKT_PHASE (from 20201130) - Byte 1 (Orderbook state) - Enumeration

| Enumeration ID   | Enumeration Description   |
|------------------|---------------------------|
| ‘” “’            | Undefined                 |

#### MKT_PHASE (from 20201130) - Byte 2 (Market period) - Enumeration

| Enumeration ID   | Enumeration Description   |
|------------------|---------------------------|
| ‘” “’            | Undefined                 |

#### MKT_PHASE (from 20201130) - Byte 3 (Phase qualifier) - Enumeration

| Enumeration ID   | Enumeration Description   |
|------------------|---------------------------|
| ‘” “’            | Undefined                 |

#### MKT_PHASE (from 20201130) - Byte 1 (Orderbook state) - Enumeration

| Enumeration ID   | Enumeration Description   |
|------------------|---------------------------|
| A                | Auction call              |

#### MKT_PHASE (from 20201130) - Byte 3 (Phase qualifier) - Enumeration

| Enumeration ID   | Enumeration Description   |
|------------------|---------------------------|
| C                | Call BBO only             |

#### MKT_PHASE (from 20201130) - Byte 1 (Orderbook state) - Enumeration

| Enumeration ID   | Enumeration Description   |
|------------------|---------------------------|
| C                | Closed                    |

#### MKT_PHASE (from 20201130) - Byte 2 (Market period) - Enumeration

| Enumeration ID   | Enumeration Description   |
|------------------|---------------------------|
| C                | Closing                   |

#### MKT_PHASE (from 20201130) - Byte 1 (Orderbook state) - Enumeration

| Enumeration ID   | Enumeration Description   |
|------------------|---------------------------|
| H                | Halted                    |
| I                | Inaccessible              |
| N                | Continuous uncrossing     |
| O                | Continuous trading        |

#### MKT_PHASE (from 20201130) - Byte 2 (Market period) - Enumeration

| Enumeration ID   | Enumeration Description   |
|------------------|---------------------------|
| O                | Opening                   |

#### MKT_PHASE (from 20201130) - Byte 3 (Phase qualifier) - Enumeration

| Enumeration ID   | Enumeration Description   |
|------------------|---------------------------|
| Q                | Quoting period            |
| R                | Random uncrossing         |

#### MKT_PHASE (from 20201130) - Byte 2 (Market period) - Enumeration

| Enumeration ID   | Enumeration Description   |
|------------------|---------------------------|
| S                | Standard                  |

#### MKT_PHASE (from 20201130) - Byte 1 (Orderbook state) - Enumeration

| Enumeration ID   | Enumeration Description   |
|------------------|---------------------------|
| S                | Suspended                 |

#### MKT_PHASE (from 20201130) - Byte 3 (Phase qualifier) - Enumeration

| Enumeration ID   | Enumeration Description   |
|------------------|---------------------------|
| T                | Trading at last           |

#### MKT_PHASE (from 20201130) - Byte 1 (Orderbook state) - Enumeration

| Enumeration ID   | Enumeration Description   |
|------------------|---------------------------|
| U                | Uncrossing                |
| Z                | Reserved                  |

#### MMT_ALGO_IND - Enumeration

| Enumeration ID   | Enumeration Description   |
|------------------|---------------------------|
| -                | Not an algorithmic trade  |
| H                | Algorithmic trade         |

#### MMT_BENCHMARK_IND - Enumeration

| Enumeration ID   | Enumeration Description   |
|------------------|---------------------------|
| -                | Not a benchmark trade     |
| B                | Benchmark trade           |
| S                | Reference price trade     |

#### MMT_CROSS_IND - Enumeration

| Enumeration ID   | Enumeration Description   |
|------------------|---------------------------|
| -                | Not a cross trade         |
| X                | Agency cross trade        |

#### MMT_DEFERRAL_TYPE - Enumeration

| Enumeration ID   | Enumeration Description                                                          |
|------------------|----------------------------------------------------------------------------------|
| -                | No deferral / unspecified                                                        |
| 1                | Limited details                                                                  |
| 2                | Daily aggregated trade                                                           |
| 3                | Volume omission trade                                                            |
| 4                | 4 weeks aggregated trade                                                         |
| 5                | Indefinite aggregated trade                                                      |
| 6                | Volume omission trade eligible for enrichment in aggregated form                 |
| 7                | Full details of earlier Limited Details trade                                    |
| 8                | Full details of earlier Daily Aggregated trade                                   |
| 9                | Full details of earlier Volume Omission trade                                    |
| V                | Full details of 4 Weeks Aggregated trade                                         |
| W                | Full details of Volume Omission trade eligible for enrichment in aggregated form |

#### MMT_DIVIDEND_IND - Enumeration

| Enumeration ID   | Enumeration Description   |
|------------------|---------------------------|
| -                | Not applicable            |
| E                | Ex-/cum-dividend          |

#### MMT_DUP_IND - Enumeration

| Enumeration ID   | Enumeration Description                         |
|------------------|-------------------------------------------------|
| -                | Unique trade report                             |
| 1                | Duplicative trade reported to more than one APA |

#### MMT_MKT_MECH - Enumeration

| Enumeration ID   | Enumeration Description   |
|------------------|---------------------------|
| 1                | Central Limit Order Book  |
| 3                | Dark Book                 |
| 4                | Off Book                  |
| 6                | Request for Quote         |
| -                | Not applicable            |

#### MMT_MOD_IND - Enumeration

| Enumeration ID   | Enumeration Description   |
|------------------|---------------------------|
| -                | New trade                 |
| A                | Amended trade             |
| C                | Trade cancellation        |

#### MMT_NEGOTIATED_IND - Enumeration

| Enumeration ID   | Enumeration Description                                                                                             |
|------------------|---------------------------------------------------------------------------------------------------------------------|
| -                | Not applicable                                                                                                      |
| 1                | Negotiated trade in liquid instruments                                                                              |
| 2                | Negotiated trade in illiquid instruments                                                                            |
| 3                | Negotiated trade subject to conditions other than the market price                                                  |
| 4                | Pre-trade transparency waiver for illiquid instrument on an SI                                                      |
| 5                | Pre-trade transparency waiver for trade larger than Standard Market Size on an SI                                   |
| 6                | Pre-trade transparency waivers for trade larger than Standard Market Size on an SI and illiquid instrument on an SI |
| N                | Negotiated trade                                                                                                    |

#### MMT_OFF_BOOK_AUTO_IND - Enumeration

| Enumeration ID   | Enumeration Description   |
|------------------|---------------------------|
| -                | Not applicable            |
| M                | Off-book manual           |
| Q                | Off-book automated        |

#### MMT_PRICE_FORMING_IND - Enumeration

| Enumeration ID   | Enumeration Description                               |
|------------------|-------------------------------------------------------|
| J                | Trade not contributing to the price discovery process |
| N                | Price not available but pending                       |
| P                | Plain vanilla (price-forming) trade                   |
| T                | Non-price forming (technical) trade                   |

#### MMT_PUB_MODE - Enumeration

| Enumeration ID   | Enumeration Description                                                    |
|------------------|----------------------------------------------------------------------------|
| -                | Immediate publication                                                      |
| 1                | Delayed publication / late reported                                        |
| 2                | Deferred publication (Large in Scale)                                      |
| 3                | Deferred publication (illiquid instrument)                                 |
| 4                | Deferred publication (size specific to instrument)                         |
| 5                | Deferred publication (illiquid instrument and size specific to instrument) |
| 6                | Deferred publication (illiquid instrument and Large in Scale)              |

#### MMT_TRANS_CAT - Enumeration

| Enumeration ID   | Enumeration Description   |
|------------------|---------------------------|
| -                | Not applicable            |
| D                | Dark trade                |
| Y                | Exchange for physical     |
| Z                | Package trade             |

#### MMT_TRD_MODE - Enumeration

| Enumeration ID   | Enumeration Description                   |
|------------------|-------------------------------------------|
| 2                | Continuous trading                        |
| 3                | At Market Close trading                   |
| 5                | Trade reporting (on-exchange)             |
| 6                | Trade reporting (off-exchange)            |
| 7                | Trade reporting (Systematic Internaliser) |
| I                | Intraday auction                          |
| K                | Closing auction                           |
| O                | Opening auction                           |
| U                | Unscheduled auction                       |
| -                | Not applicable                            |

#### ORDER_ENTRY_STATUS - Enumeration

| Enumeration ID   | Enumeration Description           |
|------------------|-----------------------------------|
| ‘””’             | Unspecified                       |
| C                | Cancel only                       |
| D                | No orderbook access               |
| E                | Order entry/cancel/modify enabled |
| M                | Cancel and modify only            |

#### ORDER_TYPE - Enumeration

| Enumeration ID   | Enumeration Description   |
|------------------|---------------------------|
| L                | Limit order               |
| M                | Market order              |

#### REASON_CODE - Enumeration

| Enumeration ID   | Enumeration Description                      |
|------------------|----------------------------------------------|
| ‘””’             | Unspecified                                  |
| A                | Action by Market Operations                  |
| C                | Scheduled transition                         |
| D                | Status change in the underlying security     |
| E                | Knocked out by the exchange                  |
| I                | Knocked in by the issuer                     |
| K                | Knocked out by issuer                        |
| L                | Trade price outside Liquidity Provider quote |
| M                | Status change on the primary market          |
| N                | No liquidity provider quote                  |
| O                | Collars breached                             |
| P                | New listing                                  |
| T                | Automatic reopening                          |

#### TRADE_PERIOD - Enumeration

| Enumeration ID   | Enumeration Description   |
|------------------|---------------------------|
| A                | Auction                   |
| C                | Closing Auction           |
| I                | Intraday Auction          |
| O                | Opening Auction           |
| T                | Trading at last price     |
| U                | Unscheduled Auction       |
| -                | Regular trading           |
| ‘””’             | Not applicable            |

#### TRADE_TYPE - Enumeration

| Enumeration ID   | Enumeration Description                                           |
|------------------|-------------------------------------------------------------------|
| ‘””’             | Regular trade [until 20201127]                                    |
| 0                | Regular trade                                                     |
| 1                | Guaranteed Cross                                                  |
| 10               | Best of Book trade                                                |
| 100              | Regular trade with provisional price                              |
| 101              | Large in Scale (LiS) trade with provisional price                 |
| 102              | Large in Scale (LiS) package trade with provisional price         |
| 103              | Issuing / Tender offer trade                                      |
| 104              | RFQ trade                                                         |
| 105              | Auction Volume Discovery (AVD) trade                              |
| 13               | Guaranteed Cross (Negotiated trade in liquid security)            |
| 14               | Guaranteed Cross (Negotiated trade in illiquid security)          |
| 15               | Non-standard settlement                                           |
| 17               | Odd lot trade                                                     |
| 19               | Repo                                                              |
| 2                | Auction trade                                                     |
| 21               | Exchange Granted trade                                            |
| 23               | Other                                                             |
| 24               | Trade cancellation                                                |
| 28               | Euronext Fund Service trade                                       |
| 3                | Large in Scale trade                                              |
| 33               | Dark trade                                                        |
| 4                | Large in Scale package trade                                      |
| 5                | VWAP trade                                                        |
| 7                | Secondary listing place trade                                     |
| 8                | Off-market trade                                                  |
| 9                | Delta Neutral trade                                               |
| A                | Lit Auction trade [until 20201127]                                |
| AuctTA           | Re-opening auction trade [until 20201127]                         |
| AuctTC           | Closing auction trade [until 20201127]                            |
| AuctTI           | Intraday auction trade [until 20201127]                           |
| AuctTO           | Opening auction trade [until 20201127]                            |
| DE               | Exchange granted trade with delayed publication [until 20201127]  |
| DH               | Other with delayed publication [until 20201127]                   |
| DL               | Odd lot with delayed publication [until 20201127]                 |
| DN               | Non-standard settlement with delayed publication [until 20201127] |
| DR               | Repo with delayed publication [until 20201127]                    |
| DT               | Derivative related trade [until 20201127]                         |
| DU               | Outside hours with delayed publication [until 20201127]           |
| M                | Dark midpoint trade [until 20201127]                              |
| NK               | Negotiated trade with delayed publication [until 20201127]        |
| NT               | Negotiated trade [until 20201127]                                 |
| O                | Ordinary trade [until 20201127]                                   |
| OE               | Exchange granted trade [until 20201127]                           |
| OH               | Other [until 20201127]                                            |
| OK               | Ordinary trade with delayed publication [until 20201127]          |
| OL               | Odd lot [until 20201127]                                          |
| ON               | Non-standard settlement [until 20201127]                          |
| OT               | OTC trade [until 20201127]                                        |
| OU               | Outside hours [until 20201127]                                    |
| RE               | Repo [until 20201127]                                             |
| SI               | Systematic Internaliser trade [until 20201127]                    |
| SK               | SI with delayed publication [until 20201127]                      |
| TK               | OTC trade with delayed publication [until 20201127]               |
| UT               | Uncrossing trade [until 20121109]                                 |
| VW               | VWAP trade [until 20201127]                                       |

#### UPDATE_TYPE - Enumeration

| Enumeration ID   | Enumeration Description   |
|------------------|---------------------------|
| A                | Add                       |
| D                | Delete                    |
| M                | Modify                    |

