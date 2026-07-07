# SIX Swiss Exchange Enumerations

The SIX Swiss Exchange is Switzerland’s principal stock exchange located in Zurich.

The following fields have Enumerations:

* AGGRESSOR_SIDE - Indicates whether a trade resulted from an incoming buy or sell order.
* BOOK_TYPE - Type of order book or trading mechanism through which a trade was executed.
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
* ORDER_TYPE - Type of order.
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
| 9                | Off-exchange              |
| Q                | Quote-driven trading      |
| R                | Request for Quote         |

#### MKT_PHASE - Enumeration

| Enumeration ID   | Enumeration Description                                                   |
|------------------|---------------------------------------------------------------------------|
| 1                | Accepting orders                                                          |
| 10               | Holiday                                                                   |
| 11               | Intraday auction                                                          |
| 14               | Closing auction                                                           |
| 15               | Pre-open                                                                  |
| 2                | Break                                                                     |
| 24               | Continuous trading                                                        |
| 25               | Trading at last                                                           |
| 3                | Closed                                                                    |
| 5                | Post-close                                                                |
| 6                | End break [until 20180622]                                                |
| 8                | Auction [until 20180622]                                                  |
| A                | Break                                                                     |
| B                | Resume                                                                    |
| C                | End of day                                                                |
| E                | Closed                                                                    |
| HALT             | Halted                                                                    |
| I                | Accepting orders                                                          |
| L                | Post-close (end of Trading at Last)                                       |
| M                | Post-close                                                                |
| O                | Start of day                                                              |
| Q                | Continuous trading                                                        |
| S                | Pre-open                                                                  |
| SUSP             | Suspended                                                                 |
| T                | Trading at last                                                           |
| U                | End of closing auction                                                    |
| UND              | Underlying condition (halted due to the underlying security being halted) |
| V                | Closing auction                                                           |

#### MMT_ALGO_IND - Enumeration

| Enumeration ID   | Enumeration Description   |
|------------------|---------------------------|
| -                | Not an algorithmic trade  |
| H                | Algorithmic trade         |

#### MMT_BENCHMARK_IND - Enumeration

| Enumeration ID   | Enumeration Description   |
|------------------|---------------------------|
| -                | Not applicable            |
| B                | Benchmark trade           |
| S                | Reference price trade     |

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

| Enumeration ID   | Enumeration Description                         |
|------------------|-------------------------------------------------|
| -                | Unique trade report                             |
| 1                | Duplicative trade reported to more than one APA |

#### MMT_MKT_MECH - Enumeration

|   Enumeration ID | Enumeration Description   |
|------------------|---------------------------|
|                1 | Central Limit Order Book  |
|                2 | Quote-Driven Market       |
|                3 | Dark Book                 |
|                4 | Off Book                  |
|                5 | Periodic Auction          |
|                6 | Request for Quote         |
|                7 | Hybrid / Other            |
|                8 | Hybrid                    |

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
| D                | Dark trade                |
| Y                | Exchange for physical     |
| Z                | Package trade             |

#### MMT_TRD_MODE - Enumeration

| Enumeration ID   | Enumeration Description                   |
|------------------|-------------------------------------------|
| 2                | Continuous trading                        |
| 3                | Trading at market close                   |
| 5                | Trade reporting (on-exchange)             |
| 6                | Trade reporting (off-exchange)            |
| 7                | Trade reporting (Systematic Internaliser) |
| I                | Intraday auction                          |
| K                | Closing auction                           |
| O                | Opening auction                           |
| U                | Unscheduled auction                       |

#### ORDER_TYPE - Enumeration

| Enumeration ID   | Enumeration Description   |
|------------------|---------------------------|
| L                | Limit order               |
| M                | Market order              |

#### TRADE_PERIOD - Enumeration

| Enumeration ID   | Enumeration Description   |
|------------------|---------------------------|
| A                | Auction                   |
| C                | Closing auction           |
| I                | Intraday auction          |
| O                | Opening auction           |
| T                | Trading at last price     |
| U                | Unscheduled auction       |
| -                | Regular trading           |

#### TRADE_TYPE - Enumeration

| Enumeration ID   | Enumeration Description   |
|------------------|---------------------------|
| ‘””’             | Standard trade            |
| NC               | Nostro cross              |

#### UPDATE_TYPE - Enumeration

| Enumeration ID   | Enumeration Description   |
|------------------|---------------------------|
| A                | Add                       |
| D                | Delete                    |
| F                | Fill                      |
| M                | Modify                    |
| P                | Partial fill              |

