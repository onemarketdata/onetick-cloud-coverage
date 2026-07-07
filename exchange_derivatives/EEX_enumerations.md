# European Energy Exchange (EEX) Enumerations

The European Energy Exchange is a leading energy exchange offering trading in power, natural gas, environmental products and more.

The following fields have Enumerations:

* CALL_PUT_IND - “C” - Call option, “P” - Put option
* MMT_MKT_MECH - Market mechanism through which a trade was executed.
* MMT_MOD_IND - Identifies trade cancellations, or amendments of a previous trade.
* MMT_PRICE_FORMING_IND - Identifies whether a trade is price-forming, or contributes to the price discovery process.
* MMT_TRANS_CAT - Identifies various special categories of trade.
* MMT_TRD_MODE - Trading period during which an on-book trade was executed, or origin of an off-book trade report (on-exchange / off-exchange / SI).
* TRADE_TYPE - Type of trade

#### CALL_PUT_IND - Enumeration

| Enumeration ID   | Enumeration Description   |
|------------------|---------------------------|
| C                | Call option               |
| P                | Put option                |

#### MMT_MKT_MECH - Enumeration

|   Enumeration ID | Enumeration Description   |
|------------------|---------------------------|
|                1 | Central Limit Order Book  |
|                4 | Off Book                  |
|                6 | Request for Quote         |

#### MMT_MOD_IND - Enumeration

| Enumeration ID   | Enumeration Description   |
|------------------|---------------------------|
| -                | New trade                 |

#### MMT_PRICE_FORMING_IND - Enumeration

| Enumeration ID   | Enumeration Description                               |
|------------------|-------------------------------------------------------|
| J                | Trade not contributing to the price discovery process |
| P                | Plain vanilla (price-forming) trade                   |

#### MMT_TRANS_CAT - Enumeration

| Enumeration ID   | Enumeration Description   |
|------------------|---------------------------|
| -                | Not applicable            |
| Y                | Exchange for physical     |
| Z                | Package trade             |

#### MMT_TRD_MODE - Enumeration

| Enumeration ID   | Enumeration Description        |
|------------------|--------------------------------|
| 1                | Auction                        |
| 2                | Continuous trading             |
| 5                | Trade reporting (on-exchange)  |
| 6                | Trade reporting (off-exchange) |
| I                | Intraday auction               |
| K                | Closing auction                |
| O                | Opening auction                |
| U                | Unscheduled auction            |
