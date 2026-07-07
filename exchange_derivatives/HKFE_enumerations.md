# Hong Kong Futures Exchange Enumerations

The Hong Kong Futures Exchange (HKFE) offers trading in futures and options on equities, indices, interest rates, and commodities.

The following fields have Enumerations:

* BOOK_TYPE - Type of order book or trading mechanism through which a trade was executed.
* MKT_PHASE - Indicates the instrument’s current market phase, as specified by the trading venue
* TRADE_PERIOD - Market period during which a trade was executed.
* TRADE_TYPE - Type of trade

#### BOOK_TYPE - Enumeration

|   Enumeration ID | Enumeration Description   |
|------------------|---------------------------|
|                0 | Lit order book            |
|                1 | Off-book                  |

#### MKT_PHASE - Enumeration

|   Enumeration ID | Enumeration Description                                                  |
|------------------|--------------------------------------------------------------------------|
|               14 | Start of after hours session, non-T+1 orders removed                     |
|               15 | Market open                                                              |
|               16 | Closed                                                                   |
|               22 | After hours trading - reset price information                            |
|               23 | Continuous trading with dynamic price bands and volatility control       |
|               24 | Continuous trading with volatility control                               |
|               25 | Continuous trading - volatility cool-off period with dynamic price bands |
|               26 | Continuous trading - volatility cool-off period with dynamic price bands |
|               27 | Reset counter for Volatility Control Mechanism trigger time              |
|               28 | Trading halt                                                             |
|               29 | End of day                                                               |
|               30 | Block trades only                                                        |
|               36 | Pre-open                                                                 |
|               37 | Pause                                                                    |
|               44 | After hours trading - market open                                        |
|               45 | After hours trading - closed                                             |
|               46 | Continuous trading with price limits                                     |
|               48 | After hours trading - continuous trading with price limits enabled       |
|               59 | Continuous trading with dynamic price bands and volatility control       |
|               60 | After hours trading - reset price information for next trading day       |
|               62 | Pre-open allocation                                                      |
|               63 | Open allocation                                                          |
|               66 | After hours trading - pre-market                                         |
|               68 | Site failover                                                            |
|               69 | Pre-market                                                               |
|               70 | Start of clearing session                                                |
|               71 | End of clearing session                                                  |
|                9 | End of day                                                               |

#### TRADE_PERIOD - Enumeration

| Enumeration ID   | Enumeration Description   |
|------------------|---------------------------|
| -                | Regular trading           |
| I                | Intraday auction          |
| O                | Opening auction           |

#### TRADE_TYPE - Enumeration

|   Enumeration ID | Enumeration Description                              |
|------------------|------------------------------------------------------|
|                0 | Regular trade (strategy)                             |
|                1 | Regular trade                                        |
|              100 | TMC leg trade [until 20150213]                       |
|                2 | Aggregated auction trade [until 20150213]            |
|               24 | Reported trade (cross)                               |
|                3 | Auction trade                                        |
|               30 | Tailor-Made Combination (TMC) trade [until 20150213] |
|                4 | Reported trade                                       |
|               40 | Combo vs. outright trade [until 20150213]            |
|               90 | Standard combo leg trade [until 20150213]            |

