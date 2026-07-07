# London Metal Exchange Enumerations

The London Metal Exchange (LME) is the world’s largest market for trading base metals futures and options.

The following fields have Enumerations:

* MMT_MKT_MECH - Market mechanism through which a trade was executed.
* MMT_MOD_IND - Identifies trade cancellations, or amendments of a previous trade.
* MMT_PRICE_FORMING_IND - Identifies whether a trade is price-forming, or contributes to the price discovery process.
* MMT_TRD_MODE - Trading period during which an on-book trade was executed, or origin of an off-book trade report (on-exchange / off-exchange / SI).
* TRADE_TYPE - Type of trade

#### MMT_MKT_MECH - Enumeration

|   Enumeration ID | Enumeration Description   |
|------------------|---------------------------|
|                1 | Central Limit Order Book  |
|                4 | Off Book                  |

#### MMT_MOD_IND - Enumeration

| Enumeration ID   | Enumeration Description   |
|------------------|---------------------------|
| -                | New trade                 |
| C                | Trade cancellation        |

#### MMT_PRICE_FORMING_IND - Enumeration

| Enumeration ID   | Enumeration Description             |
|------------------|-------------------------------------|
| P                | Plain vanilla (price-forming) trade |

#### MMT_TRD_MODE - Enumeration

|   Enumeration ID | Enumeration Description       |
|------------------|-------------------------------|
|                2 | Continuous trading            |
|                5 | Trade reporting (on-exchange) |

#### TRADE_TYPE - Enumeration

| Enumeration ID   | Enumeration Description                                              |
|------------------|----------------------------------------------------------------------|
| 11               | Current market price trade (Exchange, non-Select) [until 20250321]   |
| 12               | Current market price trade (Client, non-Select) [until 20250321]     |
| 13               | Average or Amalgamated trade (Exchange, non-Select) [until 20250321] |
| 14               | Average or Amalgamated trade (Client, non-Select) [until 20250321]   |
| 15               | Client cross vs cleared Give-up [until 20250321]                     |
| 16               | Client cross vs late cleared Give-up [until 20250321]                |
