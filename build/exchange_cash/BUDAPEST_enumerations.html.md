# Budapest Stock Exchange Enumerations

The Budapest Stock Exchange (BSE) facilitates trading in shares, bonds, investment funds, derivatives, and other securities issued by Hungarian and foreign companies.

The following fields have Enumerations:

* BOOK_TYPE - Type of order book or trading mechanism through which a trade was executed.
* CALL_PUT_IND - “C” - Call option, “P” - Put option
* MKT_PHASE - Indicates the instrument’s current market phase, as specified by the trading venue
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
* TRADE_PERIOD - Market period during which a trade was executed.
* TRADE_TYPE - Type of trade

#### BOOK_TYPE - Enumeration

| Enumeration ID   | Enumeration Description   |
|------------------|---------------------------|
| ‘””’             | Not applicable            |
| 0                | Lit order book            |
| 1                | Off-book                  |
| 9                | Off-exchange              |
| Q                | Quote-driven trading      |

#### CALL_PUT_IND - Enumeration

| Enumeration ID   | Enumeration Description   |
|------------------|---------------------------|
| C                | Call option               |
| P                | Put option                |

#### MKT_PHASE - Enumeration

|   Enumeration ID | Enumeration Description                  |
|------------------|------------------------------------------|
|                1 | Halted                                   |
|             1001 | Opening auction                          |
|             1002 | Intraday auction                         |
|             1003 | Closing auction                          |
|             1004 | Between auctions                         |
|             1006 | Volatility auction                       |
|             1007 | Extended volatility auction              |
|             1008 | Opening auction call                     |
|             1009 | Opening auction pre-orderbook balancing  |
|             1010 | Opening auction orderbook balancing      |
|             1011 | Intraday auction call                    |
|             1012 | Intraday auction pre-orderbook balancing |
|             1013 | Intraday auction orderbook balancing     |
|             1014 | Closing auction call                     |
|             1015 | Closing auction pre-orderbook balancing  |
|             1016 | Closing auction orderbook balancing      |
|             1017 | Pre-listing                              |
|             1018 | Deleted                                  |
|             1019 | Continuous auction pre-call              |
|             1020 | Continuous auction call                  |
|             1027 | Market halted                            |
|             1028 | Post-trading                             |
|             1029 | Potential volatility interruption        |
|             1030 | Frozen volatility interruption           |
|             1031 | Market order interruption                |
|             1032 | Potential market order interruption      |
|             1033 | Trading at close                         |
|                2 | Suspended                                |
|             2001 | Opening order collection                 |
|             2002 | Opening transaction                      |
|             2003 | Continuous trading                       |
|             2004 | Closing order collection                 |
|             2005 | Closing transaction                      |
|                3 | Volatility auction                       |
|               32 | Start of day                             |
|                4 | Extended volatility auction              |
|                6 | Closed                                   |
|                7 | Pre-trading                              |
|                8 | Continuous trading                       |
|                9 | Not tradable                             |

#### MMT_ALGO_IND - Enumeration

| Enumeration ID   | Enumeration Description   |
|------------------|---------------------------|
| -                | Not an algorithmic trade  |
| H                | Algorithmic trade         |

#### MMT_BENCHMARK_IND - Enumeration

| Enumeration ID   | Enumeration Description                                                            |
|------------------|------------------------------------------------------------------------------------|
| -                | Not applicable                                                                     |
| 1                | Benchmark trade executed at the closing price                                      |
| 2                | Portfolio trade + benchmark trade executed at the closing price                    |
| 3                | Contingent trade + benchmark trade executed at the closing price                   |
| 4                | Contingent trade + portfolio trade + benchmark trade executed at the closing price |
| B                | Benchmark trade                                                                    |
| C                | Contingent trade                                                                   |
| M                | Benchmark trade + contingent trade                                                 |
| N                | Contingent trade + portfolio trade                                                 |
| O                | Benchmark trade + contingent trade + portfolio trade                               |
| P                | Portfolio trade                                                                    |
| S                | Reference price trade                                                              |
| Y                | Benchmark trade + portfolio trade                                                  |

#### MMT_CROSS_IND - Enumeration

| Enumeration ID   | Enumeration Description   |
|------------------|---------------------------|
| -                | Not a cross trade         |
| X                | Agency cross trade        |

#### MMT_DEFERRAL_TYPE - Enumeration

| Enumeration ID   | Enumeration Description   |
|------------------|---------------------------|
| -                | No deferral / unspecified |

#### MMT_DIVIDEND_IND - Enumeration

| Enumeration ID   | Enumeration Description   |
|------------------|---------------------------|
| -                | Not applicable            |

#### MMT_DUP_IND - Enumeration

| Enumeration ID   | Enumeration Description   |
|------------------|---------------------------|
| -                | Unique trade report       |

#### MMT_MKT_MECH - Enumeration

| Enumeration ID   | Enumeration Description   |
|------------------|---------------------------|
| -                | Not applicable            |
| 1                | Central Limit Order Book  |
| 2                | Quote-Driven Market       |
| 4                | Off Book                  |
| 7                | Other / Hybrid            |
| 8                | Hybrid                    |
| 9                | Other                     |

#### MMT_MOD_IND - Enumeration

| Enumeration ID   | Enumeration Description   |
|------------------|---------------------------|
| -                | New trade                 |
| A                | Amended trade             |
| C                | Trade cancellation        |

#### MMT_NEGOTIATED_IND - Enumeration

| Enumeration ID   | Enumeration Description                                                                                                |
|------------------|------------------------------------------------------------------------------------------------------------------------|
| -                | Not applicable                                                                                                         |
| 1                | Negotiated trade in liquid instruments                                                                                 |
| 2                | Negotiated trade in illiquid instruments                                                                               |
| 3                | Negotiated trade subject to conditions other than the current market price                                             |
| 7                | OTC trade larger than LIS brought onto a venue                                                                         |
| 8                | Negotiated trade with pre-trade transparency waiver                                                                    |
| 9                | Large in Scale OTC negotiated trade in liquid instruments brought onto a venue                                         |
| a                | Large in Scale OTC negotiated trade in illiquid instruments brought onto a venue                                       |
| b                | Large in Scale OTC negotiated trade subject to conditions other than the current market price and brought onto a venue |
| c                | Large in Scale OTC negotiated trade with pre-trade transparency waiver brought onto a venue                            |
| N                | Negotiated trade                                                                                                       |

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
| Z                | Price not applicable                                  |

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
| Z                | Package trade             |

#### MMT_TRD_MODE - Enumeration

| Enumeration ID   | Enumeration Description                   |
|------------------|-------------------------------------------|
| -                | Not applicable                            |
| 1                | Auction                                   |
| 2                | Continuous trading                        |
| 3                | Trading at market close                   |
| 5                | Trade reporting (on-exchange)             |
| 6                | Trade reporting (off-exchange)            |
| 7                | Trade reporting (Systematic Internaliser) |
| I                | Intraday auction                          |
| K                | Closing auction                           |
| O                | Opening auction                           |
| U                | Unscheduled auction                       |

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

|   Enumeration ID | Enumeration Description                  |
|------------------|------------------------------------------|
|                1 | Regular trade                            |
|               11 | Price without turnover (Valuation trade) |
|               12 | Continuous auction                       |
|               13 | Reference price                          |
|               14 | Trade at closing price                   |
|                2 | Negotiated trade                         |
|                6 | Opening auction                          |
|                7 | Intraday auction                         |
|                8 | Closing auction                          |
|                9 | Volatility auction                       |

