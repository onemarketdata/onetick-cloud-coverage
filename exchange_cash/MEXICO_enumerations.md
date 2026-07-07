# Mexico Stock Exchange (BMV) Enumerations

The Mexican Stock Exchange, commonly known as Mexican Bolsa, Mexbol, or BMV, is one of two stock exchanges in Mexico, the other being BIVA - Bolsa Institucional de Valores.

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
|                2 | Dark book                 |
|                6 | Auction book              |

#### MKT_PHASE - Enumeration

|   Enumeration ID | Enumeration Description                                   |
|------------------|-----------------------------------------------------------|
|                0 | Order cancellation                                        |
|                1 | Opening auction                                           |
|               10 | Suspended series                                          |
|               11 | Listing suspended                                         |
|               12 | Unscheduled auction due to breach of listing requirements |
|               13 | Orderbook cleared after continuous auction                |
|               14 | Orderbook cleared after intraday auction                  |
|               15 | News pending                                              |
|               16 | Settlement auction                                        |
|               17 | Extraordinary settlement auction                          |
|               18 | Single daily auction for CKDes                            |
|               19 | Closed                                                    |
|                2 | Pre-market                                                |
|                3 | Auction allocation (uncrossing)                           |
|                4 | Auction allocation completed                              |
|                5 | End of auction                                            |
|                6 | Continuous trading                                        |
|                7 | Volatility auction                                        |
|                8 | Continuous auction due to >20 days of inactivity          |
|                9 | Demerger / spin-off auction                               |

#### TRADE_PERIOD - Enumeration

| Enumeration ID   | Enumeration Description           |
|------------------|-----------------------------------|
| -                | Regular trading                   |
