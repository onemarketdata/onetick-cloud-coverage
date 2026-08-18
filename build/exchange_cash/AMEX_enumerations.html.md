# NYSE American Equities Enumerations

The AMEX (American Stock Exchange) is a prominent US stock and options exchange based in New York City, which is now officially known as the NYSE American. Acquired by the NYSE’s parent company, it functions as an electronic exchange primarily focused on listing and trading small-cap stocks and ETFs (Exchange Traded Funds)

The following fields have Enumerations:

* AGGRESSOR_SIDE - Indicates whether a trade resulted from an incoming buy or sell order.
* TRADE_TYPE - Type of trade
* TRADE_TYPE_EXT - Extended trade type code
* ODD_LOT - Indicates whether a trade was an odd lot
* TRADE_PERIOD - Market period during which a trade was executed.
* BOOK_TYPE - Type of order book or trading mechanism through which a trade was executed.
* RPI - Indicates the presence of Retail Price Improvement interest on bid and/or ask side
* COND - Condition code
* COND2 - Second condition code
* COND3 - Third condition code
* MKT_PHASE - Indicates the instrument’s current market phase, as specified by the trading venue
* REASON_CODE - Reason for an instrument status update
* SHORT_SALE_RESTRICTION - Indicates whether short selling is permitted
* SESSION - Trading session to which the update relates, e.g. “Day”, “Night”, “T”, “T+1”
* UPDATE_TYPE - Type of update
* ORDER_TYPE - Type of order.

#### AGGRESSOR_SIDE - Enumeration

| Enumeration ID   | Enumeration Description                                          |
|------------------|------------------------------------------------------------------|
| ‘””’             | Undefined (e.g. auction trades, trades against hidden liquidity) |
| B                | Buy                                                              |
| S                | Sell                                                             |

#### TRADE_TYPE - Enumeration

| Enumeration ID   | Enumeration Description                |
|------------------|----------------------------------------|
| ‘””’             | Regular trade                          |
| A                | Auction trade                          |
| H                | Regular trade against hidden liquidity |

#### TRADE_TYPE_EXT - Enumeration

| Enumeration ID   | Enumeration Description          |
|------------------|----------------------------------|
| @                | Standard settlement              |
| ‘” “’            | No trade-through exemption       |
| F                | Intremarket sweep                |
| O                | Market center opening trade      |
| 5                | Re-opening trade                 |
| 6                | Market center closing trade      |
| T                | Extended hours                   |
| U                | Extended hours + out of sequence |
| Z                | Out of sequence                  |
| I                | Odd lot trade                    |

#### ODD_LOT - Enumeration

| Enumeration ID   | Enumeration Description   |
|------------------|---------------------------|
| Y                | Odd lot                   |
| ‘””’             | Not an odd lot            |

#### TRADE_PERIOD - Enumeration

| Enumeration ID   | Enumeration Description              |
|------------------|--------------------------------------|
| -                | Regular trading                      |
| C                | Closing auction                      |
| E                | Extended hours (Early session)       |
| L                | Extended hours (Late session)        |
| O                | Opening auction                      |
| U                | Unscheduled auction                  |
| o                | Opening auction (extended hours)     |
| u                | Unscheduled auction (extended hours) |

#### BOOK_TYPE - Enumeration

|   Enumeration ID | Enumeration Description   |
|------------------|---------------------------|
|                0 | Lit order book            |

#### RPI - Enumeration

| Enumeration ID   | Enumeration Description   |
|------------------|---------------------------|
| ‘””’             | No retail interest        |

#### COND - Enumeration

| Enumeration ID   | Enumeration Description                                   |
|------------------|-----------------------------------------------------------|
| ‘””’             | No condition                                              |
| P                | Closing auction extended due to extreme closing imbalance |

#### COND2 - Enumeration

|   Enumeration ID | Enumeration Description                                                            |
|------------------|------------------------------------------------------------------------------------|
|                0 | Auction will run                                                                   |
|                1 | Auction will run + interest exists within the auction collars or imbalance is zero |
|                2 | Auction will not run because of an imbalance outside the auction collars           |
|                3 | Auction will not run and will transition to the closing auction instead            |

#### COND3 - Enumeration

|   Enumeration ID | Enumeration Description                                                    |
|------------------|----------------------------------------------------------------------------|
|                0 | No imbalance freeze                                                        |
|                1 | Imbalance freeze - MOO/LOO orders cannot be entered / modified / cancelled |

#### MKT_PHASE - Enumeration

| Enumeration ID   | Enumeration Description   |
|------------------|---------------------------|
| ‘””’             | Unspecified               |
| 4                | Halted                    |
| 6                | Suspended                 |
| B                | Begin accepting orders    |
| E                | Early session             |
| L                | Late session              |
| O                | Core session              |
| P                | Pre-open                  |
| X                | Closed                    |

#### REASON_CODE - Enumeration

| Enumeration ID   | Enumeration Description                         |
|------------------|-------------------------------------------------|
| ‘””’             | Unspecified                                     |
| 1                | Market-wide circuit breaker (MWCB) halt level 1 |
| 2                | Market-wide circuit breaker (MWCB) halt level 2 |
| 3                | Market-wide circuit breaker (MWCB) halt level 3 |
| 6                | Suspended                                       |
| A                | Additional information requested                |
| C                | Regulatory concern                              |
| D                | News disseminated                               |
| E                | Merger effective                                |
| F                | ETF component prices not available              |
| I                | Order imbalance                                 |
| M                | LULD pause                                      |
| N                | Corporate action                                |
| O                | New security offering                           |
| P                | News pending                                    |
| V                | Intraday indicative value not available         |
| X                | Equipment changeover                            |

#### SHORT_SALE_RESTRICTION - Enumeration

| Enumeration ID   | Enumeration Description             |
|------------------|-------------------------------------|
| ‘””’             | Unspecified                         |
| 0                | No short selling restriction        |
| 1                | Short selling restriction in effect |

#### SESSION - Enumeration

| Enumeration ID   | Enumeration Description              |
|------------------|--------------------------------------|
| Main             | Main trading session                 |
| Pre-Market       | Extended hours - pre-market session  |
| Post-Market      | Extended hours - post-market session |

#### UPDATE_TYPE - Enumeration

| Enumeration ID   | Enumeration Description                                                                                         |
|------------------|-----------------------------------------------------------------------------------------------------------------|
| A                | Add                                                                                                             |
| D                | Delete                                                                                                          |
| F                | Fill                                                                                                            |
| M                | Modify                                                                                                          |
| N                | Fill (non-printable - does not appear in trade tickers as the execution is part of an aggregated auction print) |
| O                | Partial fill (non-printable)                                                                                    |
| P                | Partial fill                                                                                                    |
| R                | Refresh                                                                                                         |

#### ORDER_TYPE - Enumeration

| Enumeration ID   | Enumeration Description   |
|------------------|---------------------------|
| L                | Limit order               |

