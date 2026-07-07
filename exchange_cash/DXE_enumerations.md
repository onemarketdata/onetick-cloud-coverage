# Cboe DXE Enumerations

Cboe DXE is Cboe’s institutional equities trading book, providing trading across 23 European markets.

The following fields have Enumerations:

* BOOK_TYPE - Type of order book or trading mechanism through which a trade was executed.
* LATE_REPORTED - Indicates whether a trade was reported late and/or outside normal trading hours
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

|   Enumeration ID | Enumeration Description   |
|------------------|---------------------------|
|                0 | Lit order book            |
|                1 | Off-book                  |
|                2 | Dark book                 |
|                6 | Auction book              |

#### LATE_REPORTED - Enumeration

| Enumeration ID   | Enumeration Description                            |
|------------------|----------------------------------------------------|
| -                | Not reported late or outside hours                 |
| 1                | Reported late                                      |
| 2                | Reported outside the main trading session          |
| 3                | Reported late and outside the main trading session |

#### MKT_PHASE - Enumeration

|   Enumeration ID | Enumeration Description   |
|------------------|---------------------------|
|                1 | Closed                    |
|                2 | No reference price        |
|                3 | Suspended                 |
|                4 | Trading                   |
|                5 | Volatility interruption   |
|                7 | Off-book trade reporting  |
|                8 | Opening auction           |
|                9 | Closing auction           |
|               10 | Regulatory halt           |
|               11 | Market order imbalance    |
|               12 | Cboe Closing Cross        |
|               13 | Volatility auction        |

#### MMT_ALGO_IND - Enumeration

| Enumeration ID   | Enumeration Description   |
|------------------|---------------------------|
| -                | Not an algorithmic trade  |
| H                | Algorithmic trade         |

#### MMT_BENCHMARK_IND - Enumeration

| Enumeration ID   | Enumeration Description                                                            |
|------------------|------------------------------------------------------------------------------------|
| -                | Not a benchmark trade                                                              |
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
| E                | Ex-/cum-dividend          |

#### MMT_DUP_IND - Enumeration

| Enumeration ID   | Enumeration Description                         |
|------------------|-------------------------------------------------|
| -                | Unique trade report                             |
| 1                | Duplicative trade reported to more than one APA |

#### MMT_MKT_MECH - Enumeration

|   Enumeration ID | Enumeration Description   |
|------------------|---------------------------|
|                1 | Central Limit Order Book  |
|                3 | Dark Book                 |
|                4 | Off Book                  |
|                5 | Periodic Auction          |
|                7 | Hybrid / Other            |
|                8 | Hybrid                    |
|                9 | Other                     |

#### MMT_MOD_IND - Enumeration

| Enumeration ID   | Enumeration Description   |
|------------------|---------------------------|
| -                | New trade                 |
| A                | Amended trade             |
| C                | Trade cancellation        |

#### MMT_NEGOTIATED_IND - Enumeration

| Enumeration ID   | Enumeration Description                                                                                                |
|------------------|------------------------------------------------------------------------------------------------------------------------|
| -                | Not a negotiated trade                                                                                                 |
| 1                | Negotiated trade in liquid instruments                                                                                 |
| 2                | Negotiated trade in illiquid instruments                                                                               |
| 3                | Negotiated trade subject to conditions other than the current market price                                             |
| 4                | Pre-trade transparency waiver for illiquid instrument on an SI                                                         |
| 5                | Pre-trade transparency waiver for trade larger than Standard Market Size on an SI                                      |
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
| 1                | Delayed publication (including late reported)                              |
| 2                | Deferred publication (Large in Scale)                                      |
| 3                | Deferred publication (illiquid instrument)                                 |
| 4                | Deferred publication (size specific to instrument)                         |
| 5                | Deferred publication (illiquid instrument and size specific to instrument) |
| 6                | Deferred publication (illiquid instrument and Large in Scale)              |
| G                | Deferral for ETCs / ETNs / SFPs / emission allowances                      |

#### MMT_TRANS_CAT - Enumeration

| Enumeration ID   | Enumeration Description           |
|------------------|-----------------------------------|
| -                | No condition                      |
| D                | Dark trade                        |
| R                | Trade receiving price improvement |
| Z                | Package trade                     |

#### MMT_TRD_MODE - Enumeration

| Enumeration ID   | Enumeration Description       |
|------------------|-------------------------------|
| 2                | Continuous trading            |
| 3                | Trading at market close       |
| 4                | Outside Hours trading         |
| 5                | Trade reporting (On-exchange) |
| I                | Intraday auction              |
| K                | Closing auction               |
| O                | Opening auction               |
| P                | On Demand auction             |
| U                | Unscheduled auction           |

#### TRADE_PERIOD - Enumeration

