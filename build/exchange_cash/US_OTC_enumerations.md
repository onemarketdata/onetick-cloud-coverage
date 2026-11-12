# US OTC Equities (Trades only) Enumerations

FINRA-reported trades in US OTC equities (non-NMS securities), with history from January 2016, covering OTCQX, OTCQB, Pink and other over-the-counter trades reported to FINRA. It contains trades only: for OTC quotes use OTCM, and for exchange-listed (NMS) securities use US_COMP.

The following fields have Enumerations:

* LATE_REPORTED - Indicates whether a trade was reported late and/or outside normal trading hours
* OMD_STATUS - Indicates an instrument’s current trading status. Values are normalized across all DBs.
* REASON_CODE - Reason for an instrument status update
* SETTLEMENT_TERMS - Settlement terms associated with a trade
* TRADE_TYPE - Type of trade
* TRADING_STATUS - Indicates whether the instrument is subject to a halt or suspension

#### LATE_REPORTED - Enumeration

| Enumeration ID   | Enumeration Description               |
|------------------|---------------------------------------|
| ‘””’             | Reported on time during regular hours |
| T                | Reported on time outside hours        |
| U                | Reported late outside hours           |
| Z                | Reported late during regular hours    |

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

#### REASON_CODE - Enumeration

| Enumeration ID   | Enumeration Description                   |
|------------------|-------------------------------------------|
| ‘””’             | Unspecified                               |
| 1                | Operational halt                          |
| C13              | Quoting resumed after EMC or MWCB         |
| C14              | Trading resumed after EMC or MWCB         |
| D1               | Security deleted from OTC equities        |
| H10              | SEC trading suspension                    |
| H11              | Regulatory concern                        |
| H12              | SEC revocation                            |
| T3               | Trading resumed                           |
| U1               | Foreign market / regulatory halt          |
| U2               | Component / derivative of halted security |
| U3               | Extraordinary events                      |
| U4               | Extraordinary market condition (EMC)      |
| U5               | Market-wide circuit breaker (MWCB)        |

#### SETTLEMENT_TERMS - Enumeration

| Enumeration ID   | Enumeration Description   |
|------------------|---------------------------|
| @                | Standard settlement       |
| C                | Cash                      |
| N                | Next day                  |
| R                | Seller                    |

#### TRADE_TYPE - Enumeration

| Enumeration ID   | Enumeration Description     |
|------------------|-----------------------------|
| ‘””’             | Regular trade               |
| I                | Odd lot trade               |
| P                | Prior reference price trade |
| W                | Average price trade         |

#### TRADING_STATUS - Enumeration

| Enumeration ID   | Enumeration Description   |
|------------------|---------------------------|
| H                | Halted                    |
| Q                | Quoting resumed           |
| T                | Trading resumed           |
| X                | Quoting + trading resumed |

