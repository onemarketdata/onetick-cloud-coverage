# National Stock Exchange of India - Derivatives Enumerations

National Stock Exchange of India Limited (NSE) is one of the leading stock exchanges in India, based in Mumbai. It is the world’s largest derivatives exchange by number of contracts traded

The following fields have Enumerations:

* AGGRESSOR_SIDE - Indicates whether a trade resulted from an incoming buy or sell order.
* TRADE_TYPE - Type of trade
* TRADE_PERIOD - Market period during which a trade was executed.
* BOOK_TYPE - Type of order book or trading mechanism through which a trade was executed.
* CALL_PUT_IND - “C” - Call option, “P” - Put option
* BUY_ALGO_TYPE - Type of algorithm / routing properties associated with the order on the buy side of a trade
* SELL_ALGO_TYPE - Type of algorithm / routing properties associated with the order on the sell side of a trade
* BUY_ORDER_CAPACITY - Indicates whether the buyer was acting in a Principal / Agency / Custodial capacity
* SELL_ORDER_CAPACITY - Indicates whether the seller was acting in a Principal / Agency / Custodial capacity
* UPDATE_TYPE - Type of update
* ORDER_TYPE - Type of order.
* ORDER_CAPACITY - Indicates whether the participant that entered the order was acting in a Principal / Agency / Custodial capacity

#### AGGRESSOR_SIDE - Enumeration

| Enumeration ID   | Enumeration Description                     |
|------------------|---------------------------------------------|
| ‘””’             | Undefined (e.g. auction trades, leg trades) |
| B                | Buy                                         |
| S                | Sell                                        |

#### TRADE_TYPE - Enumeration

| Enumeration ID   | Enumeration Description                                                                                |
|------------------|--------------------------------------------------------------------------------------------------------|
| ‘””’             | Regular trade                                                                                          |
| LEG              | Strategy leg trade  [Synthetic trade reported on each outright leg when two spread orders are matched] |

#### TRADE_PERIOD - Enumeration

| Enumeration ID   | Enumeration Description   |
|------------------|---------------------------|
| C                | Closing auction           |
| O                | Opening auction           |
| T                | Trading at closing price  |
| -                | Regular trading           |

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

#### BUY_ALGO_TYPE - Enumeration

|   Enumeration ID | Enumeration Description                   |
|------------------|-------------------------------------------|
|                0 | Algo order                                |
|                1 | Non-algo order                            |
|                2 | Algo order through Smart Order Router     |
|                3 | Non-algo order through Smart Order Router |

#### SELL_ALGO_TYPE - Enumeration

|   Enumeration ID | Enumeration Description                   |
|------------------|-------------------------------------------|
|                0 | Algo order                                |
|                1 | Non-algo order                            |
|                2 | Algo order through Smart Order Router     |
|                3 | Non-algo order through Smart Order Router |

#### BUY_ORDER_CAPACITY - Enumeration

|   Enumeration ID | Enumeration Description   |
|------------------|---------------------------|
|                1 | Custodial Participant     |
|                2 | Principal                 |
|                3 | Agency                    |

#### SELL_ORDER_CAPACITY - Enumeration

|   Enumeration ID | Enumeration Description   |
|------------------|---------------------------|
|                1 | Custodial Participant     |
|                2 | Principal                 |
|                3 | Agency                    |

#### UPDATE_TYPE - Enumeration

| Enumeration ID   | Enumeration Description   |
|------------------|---------------------------|
