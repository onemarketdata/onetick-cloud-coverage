# Euronext Dublin (Irish Stock Exchange) Enumerations

Euronext Dublin, formerly the Irish Stock Exchange, is part of the Euronext group, offering trading in equities, bonds, funds, and derivatives of Irish and international companies.

The following fields have Enumerations:

* AGGRESSOR_SIDE - Indicates whether a trade resulted from an incoming buy or sell order.
* BOOK_TYPE - Type of order book or trading mechanism through which a trade was executed.
* MKT_PHASE (before 20190204) -
* MKT_PHASE (from 20190204) - Byte 1 (Orderbook state) -
* MKT_PHASE (from 20190204) - Byte 2 (Market period) -
* MKT_PHASE (from 20190204) - Byte 3 (Phase qualifier) -
* MKT_PHASE (from 20190204) - Byte 1 (Orderbook state) -
* MKT_PHASE (from 20190204) - Byte 3 (Phase qualifier) -
* MKT_PHASE (from 20190204) - Byte 1 (Orderbook state) -
* MKT_PHASE (from 20190204) - Byte 2 (Market period) -
* MKT_PHASE (from 20190204) - Byte 1 (Orderbook state) -
* MKT_PHASE (from 20190204) - Byte 2 (Market period) -
* MKT_PHASE (from 20190204) - Byte 3 (Phase qualifier) -
* MKT_PHASE (from 20190204) - Byte 2 (Market period) -
* MKT_PHASE (from 20190204) - Byte 1 (Orderbook state) -
* MKT_PHASE (from 20190204) - Byte 3 (Phase qualifier) -
* MKT_PHASE (from 20190204) - Byte 1 (Orderbook state) -
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
| ‘””’             | Not applicable            |

#### MKT_PHASE (before 20190204) - Enumeration

| Enumeration ID   | Enumeration Description                        |
|------------------|------------------------------------------------|
| 201              | Restricted                                     |
| 202              | Book                                           |
| 211              | Closing auction freeze                         |
| ADD              | New instrument before its first day of trading |
| CCAL             | Closing auction call                           |
| COBB             | Closing auction orderbook balancing            |
| CPOB             | Closing auction pre-orderbook balancing        |
| ENDT             | End of trading                                 |
| HALT             | Halted                                         |
| HOL              | Holiday                                        |
| IAIP             | Intraday auction freeze                        |
| ICAL             | Intraday auction call                          |
| IOBB             | Intraday auction orderbook balancing           |
| IPOB             | Intraday auction pre-orderbook balancing       |
| OAIP             | Opening IPO auction                            |
| OCAL             | Opening auction call                           |
| OOBB             | Opening auction orderbook balancing            |
| OPOB             | Opening auction pre-orderbook balancing        |
| POST             | Post-trading                                   |
| PRET             | Pre-trading                                    |
| STAR             | Start of trading                               |
| SUSP             | Suspended                                      |
| TRAD             | Continuous trading                             |
| UNDE             | Undefined                                      |
| VOLA             | Volatility auction                             |

#### MKT_PHASE (from 20190204) - Byte 1 (Orderbook state) - Enumeration

| Enumeration ID   | Enumeration Description   |
|------------------|---------------------------|
| ‘” “’            | Undefined                 |

#### MKT_PHASE (from 20190204) - Byte 2 (Market period) - Enumeration

| Enumeration ID   | Enumeration Description   |
|------------------|---------------------------|
| ‘” “’            | Undefined                 |

#### MKT_PHASE (from 20190204) - Byte 3 (Phase qualifier) - Enumeration

| Enumeration ID   | Enumeration Description   |
|------------------|---------------------------|
| ‘” “’            | Undefined                 |

#### MKT_PHASE (from 20190204) - Byte 1 (Orderbook state) - Enumeration

| Enumeration ID   | Enumeration Description   |
|------------------|---------------------------|
| A                | Auction call              |

#### MKT_PHASE (from 20190204) - Byte 3 (Phase qualifier) - Enumeration

| Enumeration ID   | Enumeration Description   |
|------------------|---------------------------|
| C                | Call BBO only             |

#### MKT_PHASE (from 20190204) - Byte 1 (Orderbook state) - Enumeration

| Enumeration ID   | Enumeration Description   |
|------------------|---------------------------|
| C                | Closed                    |

#### MKT_PHASE (from 20190204) - Byte 2 (Market period) - Enumeration

| Enumeration ID   | Enumeration Description   |
|------------------|---------------------------|
| C                | Closing                   |

#### MKT_PHASE (from 20190204) - Byte 1 (Orderbook state) - Enumeration

| Enumeration ID   | Enumeration Description   |
|------------------|---------------------------|
| H                | Halted                    |
| I                | Inaccessible              |
| N                | Continuous uncrossing     |
| O                | Continuous trading        |

#### MKT_PHASE (from 20190204) - Byte 2 (Market period) - Enumeration

| Enumeration ID   | Enumeration Description   |
|------------------|---------------------------|
| O                | Opening                   |

#### MKT_PHASE (from 20190204) - Byte 3 (Phase qualifier) - Enumeration

| Enumeration ID   | Enumeration Description   |
|------------------|---------------------------|
| Q                | Quoting period            |
| R                | Random uncrossing         |

#### MKT_PHASE (from 20190204) - Byte 2 (Market period) - Enumeration

| Enumeration ID   | Enumeration Description   |
|------------------|---------------------------|
| S                | Standard                  |

#### MKT_PHASE (from 20190204) - Byte 1 (Orderbook state) - Enumeration

| Enumeration ID   | Enumeration Description   |
|------------------|---------------------------|
| S                | Suspended                 |

#### MKT_PHASE (from 20190204) - Byte 3 (Phase qualifier) - Enumeration

| Enumeration ID   | Enumeration Description   |
|------------------|---------------------------|
| T                | Trading at last           |

#### MKT_PHASE (from 20190204) - Byte 1 (Orderbook state) - Enumeration

| Enumeration ID   | Enumeration Description   |
|------------------|---------------------------|
| U                | Uncrossing                |
| Z                | > Reserved                |

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
| -                | Not applicable            |
| 1                | Central Limit Order Book  |
| 3                | Dark Book                 |
| 4                | Off Book                  |

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
| -                | Not applicable                            |
| 2                | Continuous trading                        |
| 3                | At Market Close trading                   |
| 5                | Trade reporting (on-exchange)             |
| 6                | Trade reporting (off-exchange)            |
| 7                | Trade reporting (Systematic Internaliser) |
| I                | Intraday auction                          |
| K                | Closing auction                           |
| O                | Opening auction                           |
| U                | Unscheduled auction                       |

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
| ‘””’             | Not applicable            |
| A                | Auction                   |
| C                | Closing Auction           |
| I                | Intraday Auction          |
| O                | Opening Auction           |
| T                | Trading at last price     |
| U                | Unscheduled Auction       |
| -                | Regular trading           |

#### TRADE_TYPE - Enumeration

| Enumeration ID   | Enumeration Description                                   |
|------------------|-----------------------------------------------------------|
| ‘””’             | Unspecified                                               |
| 1                | Regular trade                                             |
| 10               | Exchange for Physical - cash leg                          |
| 100              | Regular trade with provisional price                      |
| 101              | Large in Scale (LiS) trade with provisional price         |
| 102              | Large in Scale (LiS) package trade with provisional price |
| 20               | Best of Book trade                                        |
| 24               | Trade cancellation                                        |
| 25               | Off-market trade                                          |
| 26               | Delta Neutral trade                                       |
