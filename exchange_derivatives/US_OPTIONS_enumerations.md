# US Consolidated Options (OPRA) Enumerations

This refers to consolidated data from all US options exchanges disseminated through the Options Price Reporting Authority (OPRA).

The following fields have Enumerations:

* CALL_PUT_IND - “C” - Call option, “P” - Put option
* EXCHANGE - Exchange from which the update originates
* QUOTE_COND - Indicates any special conditions applicable to a quote
* TRADE_TYPE - Type of trade
* TRADE_TYPE_EXT - Extended trade type code

#### CALL_PUT_IND - Enumeration

| Enumeration ID   | Enumeration Description   |
|------------------|---------------------------|
| C                | Call option               |
| P                | Put option                |

#### EXCHANGE - Enumeration

| Enumeration ID   | Enumeration Description       |
|------------------|-------------------------------|
| A                | NYSE American                 |
| B                | Boston Options Exchange (BOX) |
| C                | Cboe C1                       |
| D                | MIAX Emerald                  |
| E                | Cboe EDGX                     |
| G                | MX2                           |
| H                | Nasdaq GEMX                   |
| I                | Nasdaq ISE                    |
| J                | Nasdaq MRX                    |
| M                | MIAX                          |
| N                | NYSE Arca                     |
| P                | MIAX Pearl                    |
| Q                | Nasdaq                        |
| S                | MIAX Sapphire                 |
| T                | Nasdaq BX                     |
| U                | Members Exchange (MEMX)       |
| V                | IEX                           |
| W                | Cboe C2                       |
| X                | Nasdaq PHLX                   |
| Z                | Cboe BZX                      |

#### QUOTE_COND - Enumeration

| Enumeration ID   | Enumeration Description                         |
|------------------|-------------------------------------------------|
| ‘””’             | Regular quote                                   |
| A                | Eligible for automatic execution                |
| B                | Bid contains customer trading interest          |
| C                | Bid and offer contain customer trading interest |
| F                | Non-firm quote                                  |
| I                | Indicative                                      |
| O                | Offer contains customer trading interest        |
| R                | Opening rotation                                |
| T                | Trading halted                                  |
| X                | Offer side not firm                             |
| Y                | Bid side not firm                               |

#### TRADE_TYPE - Enumeration

| Enumeration ID   | Enumeration Description                                                                  |
|------------------|------------------------------------------------------------------------------------------|
| ‘””’             | Regular trade                                                                            |
| A                | Cancel trade other than last or opening                                                  |
| a                | Single leg auction non-ISO                                                               |
| B                | Out of sequence                                                                          |
| b                | Single leg auction ISO                                                                   |
| C                | Cancel last trade                                                                        |
| c                | Single leg cross non-ISO                                                                 |
| D                | Reported late but in sequence                                                            |
| d                | Single leg cross ISO                                                                     |
| E                | Cancel opening trade                                                                     |
| e                | Single leg floor trade                                                                   |
| f                | Multi-leg electronic trade                                                               |
| F                | Opening trade reported out of sequence                                                   |
| G                | Cancellation of only trade reported today                                                |
| g                | Multi-leg auction trade                                                                  |
| h                | Multi-leg cross                                                                          |
| H                | Opening trade reported late but in sequence                                              |
| I                | Electronic trade                                                                         |
| i                | Multi-leg floor trade                                                                    |
| j                | Multi-leg against single leg                                                             |
| J                | Re-opening trade                                                                         |
| K                | Adjusted contract                                                                        |
| k                | Auction trade - multi-leg with underlying stock                                          |
| l                | Auction trade - multi-leg against single leg                                             |
| L                | Spread trade                                                                             |
| m                | Multi-leg floor trade against single leg                                                 |
| M                | Straddle                                                                                 |
| n                | Multi-leg with underlying stock                                                          |
| N                | Stopped trade reported following a non-stopped trade at the same price                   |
| O                | Cancel stopped trade                                                                     |
| o                | Cross trade - multi-leg with underlying stock                                            |
| P                | Buy-write                                                                                |
| p                | Floor trade - multi-leg with underlying stock                                            |
| Q                | Combo                                                                                    |
| q                | Multi-leg with underlying stock against single leg                                       |
| r                | Auction trade - multi-leg with underlying stock against single leg                       |
| R                | Stopped trade that did not trade through another eligible market at the time of the stop |
| s                | Floor trade - multi-leg with underlying stock against single leg                         |
| S                | Intermarket sweep                                                                        |
| T                | Benchmark trade                                                                          |
| t                | Multi-leg floor trade of prioprietary products                                           |
| u                | Multilateral compression trade of proprietary products                                   |
| v                | Extended hours trade                                                                     |
| X                | Trade-through exempt                                                                     |

#### TRADE_TYPE_EXT - Enumeration

| Enumeration ID   | Enumeration Description                                                                  |
|------------------|------------------------------------------------------------------------------------------|
| ‘””’             | Regular trade                                                                            |
| AJST             | Adjusted contract                                                                        |
| AUTO             | Electronic trade                                                                         |
| BNMT             | Benchmark trade                                                                          |
| BWRT             | Buy-write                                                                                |
| CANC             | Cancel trade other than last or opening                                                  |
| CBMO             | Multi-leg floor trade of prioprietary products                                           |
| CMBO             | Combo                                                                                    |
| CNCL             | Cancel last trade                                                                        |
| CNCO             | Cancel opening trade                                                                     |
| CNOL             | Cancellation of only trade reported today                                                |
| CSTP             | Cancel stopped trade                                                                     |
| EXHT             | Extended hours trade                                                                     |
| ISOI             | Intermarket sweep                                                                        |
| LATE             | Reported late but in sequence                                                            |
| MASL             | Auction trade - multi-leg against single leg                                             |
| MCTP             | Multilateral compression trade of proprietary products                                   |
| MESL             | Multi-leg against single leg                                                             |
| MFSL             | Multi-leg floor trade against single leg                                                 |
| MLAT             | Multi-leg auction trade                                                                  |
| MLCT             | Multi-leg cross                                                                          |
| MLET             | Multi-leg electronic trade                                                               |
| MLFT             | Multi-leg floor trade                                                                    |
| OPEN             | Opening trade reported out of sequence                                                   |
| OPNL             | Opening trade reported late but in sequence                                              |
| OSEQ             | Out of sequence                                                                          |
| REOP             | Re-opening trade                                                                         |
| SLAI             | Single leg auction ISO                                                                   |
| SLAN             | Single leg auction non-ISO                                                               |
| SLCI             | Single leg cross ISO                                                                     |
| SLCN             | Single leg cross non-ISO                                                                 |
| SLFT             | Single leg floor trade                                                                   |
| SPIM             | Stopped trade that did not trade through another eligible market at the time of the stop |
| SPRD             | Spread trade                                                                             |
| STDL             | Straddle                                                                                 |
| STPD             | Stopped trade reported following a non-stopped trade at the same price                   |
| TASL             | Auction trade - multi-leg with underlying stock against single leg                       |
| TESL             | Multi-leg with underlying stock against single leg                                       |
| TFSL             | Floor trade - multi-leg with underlying stock against single leg                         |
| TLAT             | Auction trade - multi-leg with underlying stock                                          |
| TLCT             | Cross trade - multi-leg with underlying stock                                            |
| TLET             | Multi-leg with underlying stock                                                          |
| TLFT             | Floor trade - multi-leg with underlying stock                                            |
| XMPT             | Trade-through exempt                                                                     |

