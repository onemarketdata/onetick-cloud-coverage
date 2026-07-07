# Toronto Stock Exchange Enumerations

The Toronto Stock Exchange is the largest equity market in Canada trading senior equities.

The following fields have Enumerations:

* AGGRESSOR_SIDE - Indicates whether a trade resulted from an incoming buy or sell order.
* BOOK_TYPE - Type of order book or trading mechanism through which a trade was executed.
* BYPASS - Identifies whether the trade resulted from a Bypass order
* MKT_PHASE - Indicates the instrument’s current market phase, as specified by the trading venue
* ODD_LOT - Indicates whether a trade was an odd lot
* ORDER_TYPE - Type of order.
* SPECIAL_TERMS - Indicates any non-standard settlement / execution terms associated with a trade
* TRADE_PERIOD - Market period during which a trade was executed.
* TRADE_TYPE - Type of trade
* UPDATE_TYPE - Type of update

#### AGGRESSOR_SIDE - Enumeration

| Enumeration ID   | Enumeration Description                          |
|------------------|--------------------------------------------------|
| ‘””’             | Undefined (e.g. off-book trades, auction trades) |
| B                | Buy                                              |
| S                | Sell                                             |

#### BOOK_TYPE - Enumeration

|   Enumeration ID | Enumeration Description   |
|------------------|---------------------------|
|                0 | Lit order book            |
|                1 | Off-book                  |
|                2 | Dark book                 |
|                3 | Odd lot book              |
|                4 | Special terms book        |

#### BYPASS - Enumeration

| Enumeration ID   | Enumeration Description   |
|------------------|---------------------------|
| ‘””’             | Not a bypass trade        |
| Y                | Bypass trade              |

#### MKT_PHASE - Enumeration

| Enumeration ID   | Enumeration Description                    |
|------------------|--------------------------------------------|
| A                | CCP determination                          |
| AE               | Price movement delayed                     |
| AR               | Delayed open                               |
| AS               | Halted                                     |
| C                | Closed                                     |
| E                | Price movement extension                   |
| F                | Extended hours close                       |
| G                | NAVex order entry [until 20221230]         |
| H                | End of NAVex order entry [until 20221230]y |
| I                | Inhibited                                  |
| IE               | Inhibited, volatility halt                 |
| IR               | Inhibited, delayed open                    |
| IS               | Inhibited, halted                          |
| J                | NAVex closed [until 20221230]              |
| K                | NAVex AM execution [until 20221230]        |
| L                | Closing                                    |
| M                | MOC imbalance                              |
| N                | Extended hours CXLs                        |
| O                | Opening                                    |
| P                | Pre-open                                   |
| R                | Extended hours open                        |
| S                | Open                                       |
| T                | MOC freeze                                 |
| X                | NAVex PM execution [until 20221230]        |
| Y                | NAVex closed [until 20221230]              |

#### ODD_LOT - Enumeration

| Enumeration ID   | Enumeration Description   |
|------------------|---------------------------|
| ‘””’             | Board lot                 |
| Y                | Odd lot                   |

#### ORDER_TYPE - Enumeration

| Enumeration ID   | Enumeration Description   |
|------------------|---------------------------|
| L                | Limit order               |
| M                | Market order              |

#### SPECIAL_TERMS - Enumeration

| Enumeration ID   | Enumeration Description                |
|------------------|----------------------------------------|
| ‘””’             | No special terms (standard settlement) |
| C                | Cash                                   |
| CT               | Cash today                             |
| DC               | Derivative-related contingent trade    |
| DD               | Delayed delivery                       |
| NN               | Non-net                                |
| NR               | Non-resident                           |

#### TRADE_PERIOD - Enumeration

| Enumeration ID   | Enumeration Description   |
|------------------|---------------------------|
| -                | Regular trading           |
| C                | Closing auction           |
| O                | Opening auction           |
| T                | Trading at closing price  |
| U                | Unscheduled auction       |

#### TRADE_TYPE - Enumeration

| Enumeration ID   | Enumeration Description               |
|------------------|---------------------------------------|
| ‘””’             | Regular trade                         |
