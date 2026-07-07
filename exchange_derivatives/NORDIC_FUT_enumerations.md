# Nasdaq Nordic - Derivatives Enumerations

In addition to equities, Nasdaq Nordic also offers trading in Nordic derivatives like stock options and futures.

The following fields have Enumerations:

* CALL_PUT_IND - “C” - Call option, “P” - Put option
* MKT_PHASE (before 20220912) -
* MKT_PHASE (from 20220912) -
* MMT_MKT_MECH - Market mechanism through which a trade was executed.
* MMT_MOD_IND - Identifies trade cancellations, or amendments of a previous trade.
* MMT_NEGOTIATED_IND - Indicates privately negotiated trades, or Systematic Internaliser trades exempt from pre-trade transparency.
* MMT_PRICE_FORMING_IND - Identifies whether a trade is price-forming, or contributes to the price discovery process.
* MMT_TRD_MODE - Trading period during which an on-book trade was executed, or origin of an off-book trade report (on-exchange / off-exchange / SI).
* ORDER_TYPE - Type of order.
* TRADE_TYPE - Type of trade
* UPDATE_TYPE - Type of update

#### CALL_PUT_IND - Enumeration

| Enumeration ID   | Enumeration Description   |
|------------------|---------------------------|
| C                | Call option               |
| P                | Put option                |

#### MKT_PHASE (before 20220912) - Enumeration

| Enumeration ID   | Enumeration Description   |
|------------------|---------------------------|
| 13               | Turnover                  |
| 14               | End of trading            |
| 15               | Statistics                |
| 16               | Order expiry              |
| 24               | Post-close                |
| 4                | Terminating               |
| C                | Closed                    |
| H                | Halted                    |
| L                | Closing auction           |
| O                | Opening auction           |
| P                | Pre-trading               |
| Q                | Auction                   |
| S                | Post-trading              |
| T                | Continuous trading        |

#### MKT_PHASE (from 20220912) - Enumeration

| Enumeration ID   | Enumeration Description              |
|------------------|--------------------------------------|
| 13               | Turnover                             |
| 24               | Post-close                           |
| C                | Closing auction                      |
| E                | Continuous trading (evening session) |
| G                | Regulatory suspension                |
| H                | Technical halt                       |
| L                | Post-close                           |
| M                | Continuous trading (morning session) |
| O                | Opening auction                      |
| P                | Pre-trading                          |
| R                | Re-opening auction                   |
| S                | Continuous trading (evening session) |
| T                | Continuous trading                   |
| V                | Volatility auction                   |
| X                | Closed                               |

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

#### MMT_NEGOTIATED_IND - Enumeration

| Enumeration ID   | Enumeration Description   |
|------------------|---------------------------|
| -                | Not applicable            |
| N                | Negotiated trade          |

#### MMT_PRICE_FORMING_IND - Enumeration

| Enumeration ID   | Enumeration Description                               |
|------------------|-------------------------------------------------------|
| J                | Trade not contributing to the price discovery process |
| N                | Price not available but pending                       |
| P                | Plain vanilla (price-forming) trade                   |
| T                | Non-price forming (technical) trade                   |

#### MMT_TRD_MODE - Enumeration

| Enumeration ID   | Enumeration Description                   |
|------------------|-------------------------------------------|
| 1                | Auction                                   |
| 2                | Continuous trading                        |
| 4                | Out of Main Session trading               |
| 5                | Trade reporting (on-exchange)             |
| 6                | Trade reporting (off-exchange)            |
| 7                | Trade reporting (Systematic Internaliser) |
| K                | Closing auction                           |
| O                | Opening auction                           |
| U                | Unscheduled auction                       |

#### ORDER_TYPE - Enumeration

| Enumeration ID   | Enumeration Description   |
|------------------|---------------------------|
| L                | Limit order               |
| M                | Market order              |

#### TRADE_TYPE - Enumeration

| Enumeration ID   | Enumeration Description                          |
|------------------|--------------------------------------------------|
| ‘””’             | Regular trade                                    |
| 1                | Off-book trade - Standard                        |
| 10               | Off-book trade - Off-hours [until 20250926]      |
| 101              | Off-book trade - Outside spread [until 20250926] |
| 1341             | Block trade                                      |
| 1342             | Block trade - Cash related                       |
| 1343             | Block trade - Exchange Granted                   |
| 1344             | Block trade - Off-hours                          |
| 154              | OTC trade                                        |
