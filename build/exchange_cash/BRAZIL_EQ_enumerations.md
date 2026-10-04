# B3 (Bovespa) - Equities + Equity Options Enumerations

B3’s Bovespa equities segment is Brazil’s main stock exchange for trading stocks and equity options.

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

|   Enumeration ID | Enumeration Description               |
|------------------|---------------------------------------|
|               02 | Trading halt (Pause)                  |
|               04 | No-Open (Close)                       |
|               17 | Ready to trade (Open)                 |
|               18 | Not available for trading (Pre-close) |
|               21 | Pre-Open                              |
|              101 | Final Closing Call                    |

#### TRADE_PERIOD - Enumeration

| Enumeration ID   | Enumeration Description      |
|------------------|------------------------------|
| -                | Regular trading              |
| C                | Closing auction              |
| L                | Outside hours (Late session) |
| O                | Opening auction              |
| U                | Unscheduled auction          |

#### TRADE_TYPE - Enumeration

| Enumeration ID   | Enumeration Description         |
|------------------|---------------------------------|
| 0                | Regular trade                   |
| 1                | Cross trade                     |
| 24               | After-hours trade               |
| 25               | Retail Liquidity Provider trade |
| 26               | Out of sequence trade           |
| RLP              | Retail Liquidity Provider trade |

