# Taiwan Futures Exchange (TAIFEX) Enumerations

The Taiwan Futures Exchange was established in 1998. It offers futures and options on major Taiwan stock indices, government bond futures, equity options and 30-day CP interest rate futures.

The following fields have Enumerations:

* AGGRESSOR_SIDE - Indicates whether a trade resulted from an incoming buy or sell order.
* TRADE_TYPE - Type of trade
* TRADE_PERIOD - Market period during which a trade was executed.
* BOOK_TYPE - Type of order book or trading mechanism through which a trade was executed.
* CALL_PUT_IND - “C” - Call option, “P” - Put option
* TRADE_SESSION - Trading session from which a trade originates, e.g. “Day”, “Night”
* QUOTE_SESSION - Trading session from which the quote originates, e.g. “Day”, “Night”
* SESSION - Trading session to which the update relates, e.g. “Day”, “Night”, “T”, “T+1”
* MKT_PHASE - Indicates the instrument’s current market phase, as specified by the trading venue
* EVENT_CODE - Event that triggered an instrument status update

#### AGGRESSOR_SIDE - Enumeration

| Enumeration ID   | Enumeration Description                                      |
|------------------|--------------------------------------------------------------|
| ‘””’             | Undefined (e.g. auction trades, leg trades, off-book trades) |
| B                | Buy                                                          |
| S                | Sell                                                         |

#### TRADE_TYPE - Enumeration

| Enumeration ID   | Enumeration Description   |
|------------------|---------------------------|
| ‘””’             | Regular trade             |
| LEG              | Strategy leg trade        |

#### TRADE_PERIOD - Enumeration

| Enumeration ID   | Enumeration Description   |
|------------------|---------------------------|
| A                | Auction                   |
| -                | Regular trading           |

#### BOOK_TYPE - Enumeration

| Enumeration ID   | Enumeration Description                                                                  |
|------------------|------------------------------------------------------------------------------------------|
| 0                | Lit order book                                                                           |
| S                | Strategy leg [trade reported in each of outright leg when two spread orders are matched] |

#### CALL_PUT_IND - Enumeration

| Enumeration ID   | Enumeration Description   |
|------------------|---------------------------|
| C                | Call option               |
| P                | Put option                |

#### TRADE_SESSION - Enumeration

| Enumeration ID   | Enumeration Description   |
|------------------|---------------------------|
| Day              | Day session               |
| Night            | Night session             |

#### QUOTE_SESSION - Enumeration

| Enumeration ID   | Enumeration Description   |
|------------------|---------------------------|
| Day              | Day session               |
| Night            | Night session             |

#### SESSION - Enumeration

| Enumeration ID   | Enumeration Description   |
|------------------|---------------------------|
| Day              | Day session               |
| Night            | Night session             |

#### MKT_PHASE - Enumeration

|   Enumeration ID | Enumeration Description   |
|------------------|---------------------------|
|              200 | Suspended                 |
|              302 | Accepting orders          |
|              304 | Open                      |
|              305 | Non-cancel period         |
|              306 | Cloed                     |

#### EVENT_CODE - Enumeration

|   Enumeration ID | Enumeration Description                                   |
|------------------|-----------------------------------------------------------|
|              100 | Circuit breaker cooling-off period                        |
|              101 | Price limits expanded after circuit breaker               |
|              400 | Dynamic price banding suspended                           |
|              401 | Dynamic price banding resumed                             |
|              402 | Dynamic price banding range adjusted                      |
|              403 | Dynamic price banding suspension preliminary notification |
|              404 | Dynamic price banding resumption preliminary notification |
|              405 | Dynamic price banding adjustment preliminary notification |

