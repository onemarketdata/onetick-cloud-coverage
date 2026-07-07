# Montreal Exchange Enumerations

The Montreal Exchange (MX) offers trading in futures and options on equities, indices, interest rates, and currencies.

The following fields have Enumerations:

* BOOK_TYPE - Type of order book or trading mechanism through which a trade was executed.
* CALL_PUT_IND - “C” - Call option, “P” - Put option
* MKT_PHASE - Indicates the instrument’s current market phase, as specified by the trading venue
* TRADE_PERIOD - Market period during which a trade was executed.
* TRADE_TYPE - Type of trade

#### BOOK_TYPE - Enumeration

|   Enumeration ID | Enumeration Description   |
|------------------|---------------------------|
|                0 | Lit order book            |
|                1 | Off-book                  |

#### CALL_PUT_IND - Enumeration

| Enumeration ID   | Enumeration Description   |
|------------------|---------------------------|
| C                | Call option               |
| P                | Put option                |

#### MKT_PHASE - Enumeration

| Enumeration ID   | Enumeration Description        |
|------------------|--------------------------------|
| B                | Post-trading                   |
| C                | Consultation start             |
| c                | Not trading                    |
| E                | No cancellation                |
| F                | Consultation end               |
| f                | Forbidden                      |
| I                | Prohibited                     |
| M                | Mini-batch                     |
| N                | Market Operations intervention |
| O                | Opening                        |
| P                | Pre-opening                    |
| r                | Pre-opening                    |
| S                | Continuous trading             |
| s                | Suspended                      |
| Z                | Interrupted                    |

#### TRADE_PERIOD - Enumeration

| Enumeration ID   | Enumeration Description   |
|------------------|---------------------------|
| -                | Regular trading           |
| I                | Intraday auction          |
| O                | Opening auction           |
| U                | Unscheduled auction       |

#### TRADE_TYPE - Enumeration
