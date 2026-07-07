# National Stock Exchange of India - Equities Enumerations

The NSE is India’s largest stock exchange offering trading in Indian company stocks and equity products.

The following fields have Enumerations:

* AGGRESSOR_SIDE - Indicates whether a trade resulted from an incoming buy or sell order.
* ALGO_TYPE - Type of algorithm / routing properties associated with an order
* BUY_ALGO_TYPE - Type of algorithm / routing properties associated with the order on the buy side of a trade
* BUY_ORDER_CAPACITY - Indicates whether the buyer was acting in a Principal / Agency / Custodial capacity
* ORDER_CAPACITY - Indicates whether the participant that entered the order was acting in a Principal / Agency / Custodial capacity
* SELL_ALGO_TYPE - Type of algorithm / routing properties associated with the order on the sell side of a trade
* SELL_ORDER_CAPACITY - Indicates whether the seller was acting in a Principal / Agency / Custodial capacity
* TRADE_PERIOD - Market period during which a trade was executed.

#### AGGRESSOR_SIDE - Enumeration

| Enumeration ID   | Enumeration Description         |
|------------------|---------------------------------|
| ‘””’             | Undefined (e.g. auction trades) |
| B                | Buy                             |
| S                | Sell                            |

#### ALGO_TYPE - Enumeration

|   Enumeration ID | Enumeration Description                   |
|------------------|-------------------------------------------|
|                0 | Algo order                                |
|                1 | Non-algo order                            |
|                2 | Algo order through Smart Order Router     |
|                3 | Non-algo order through Smart Order Router |

#### BUY_ALGO_TYPE - Enumeration

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

#### ORDER_CAPACITY - Enumeration

|   Enumeration ID | Enumeration Description   |
|------------------|---------------------------|
|                1 | Custodial Participant     |
|                2 | Principal                 |
|                3 | Agency                    |

#### SELL_ALGO_TYPE - Enumeration

|   Enumeration ID | Enumeration Description                   |
|------------------|-------------------------------------------|
