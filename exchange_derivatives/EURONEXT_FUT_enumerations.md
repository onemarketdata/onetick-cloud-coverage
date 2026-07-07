# Euronext Equity + Index Derivatives Enumerations

Euronext Equity + Index Derivatives offers trading in futures and options on European equities and indices.

The following fields have Enumerations:

* MMT_CROSS_IND - Identifies agency cross trades, where a broker crossed two client orders outside the order book.
* MMT_MKT_MECH - Market mechanism through which a trade was executed.
* MMT_MOD_IND - Identifies trade cancellations, or amendments of a previous trade.
* MMT_TRANS_CAT - Identifies various special categories of trade.
* MMT_TRD_MODE - Trading period during which an on-book trade was executed, or origin of an off-book trade report (on-exchange / off-exchange / SI).
* TRADE_TYPE - Type of trade

#### MMT_CROSS_IND - Enumeration

| Enumeration ID   | Enumeration Description   |
|------------------|---------------------------|
| -                | Not a cross trade         |
| X                | Agency cross trade        |

#### MMT_MKT_MECH - Enumeration

|   Enumeration ID | Enumeration Description   |
|------------------|---------------------------|
|                1 | Central Limit Order Book  |
|                4 | Off Book                  |

#### MMT_MOD_IND - Enumeration

| Enumeration ID   | Enumeration Description   |
|------------------|---------------------------|
| -                | New trade                 |
| A                | Amended trade             |
| C                | Trade cancellation        |

#### MMT_TRANS_CAT - Enumeration

| Enumeration ID   | Enumeration Description   |
|------------------|---------------------------|
| -                | Not applicable            |
| Y                | Exchange for Physical     |
| Z                | Package trade             |

#### MMT_TRD_MODE - Enumeration

| Enumeration ID   | Enumeration Description       |
|------------------|-------------------------------|
| 2                | Continuous trading            |
| 5                | Trade reporting (on-exchange) |
| O                | Opening auction               |
| U                | Unscheduled auction           |

#### TRADE_TYPE - Enumeration

|   Enumeration ID | Enumeration Description                      |
|------------------|----------------------------------------------|
|               10 | Guaranteed Cross                             |
|               11 | Against Actual                               |
|               12 | Asset Allocation                             |
|               14 | Exchange for Swap                            |
|               29 | Strategy leg trade                           |
|               30 | LIS leg trade                                |
|               31 | Basis leg trade                              |
|               33 | Guaranteed Cross leg trade                   |
|               34 | Against Actual leg trade                     |
|               35 | Asset Allocation leg trade                   |
|               37 | EFS leg trade                                |
|               38 | EFP leg trade                                |
|               39 | AtomX trade                                  |
|               43 | Request for Cross (RFC) trade                |
|               44 | RFC leg trade                                |
|               49 | Delta Neutral trade - underlying futures leg |
|                6 | Standard trade                               |
|                7 | Large in Scale (LIS) trade                   |
|                8 | Basis trade                                  |
|                9 | Large in Scale Package Trade                 |

