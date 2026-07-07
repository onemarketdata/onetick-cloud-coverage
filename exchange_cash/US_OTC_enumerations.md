# US OTC Equities (Trades only) Enumerations

FINRA reported trades for OTC instruments

The following fields have Enumerations:

* LATE_REPORTED - Indicates whether a trade was reported late and/or outside normal trading hours
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
