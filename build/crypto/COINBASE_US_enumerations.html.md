# Coinbase - US Exchange Enumerations

Coinbase is the largest US-based cryptocurrency exchange, founded in 2012 by Brian Armstrong and Fred Ehrsam to facilitate Bitcoin trading. Headquartered in the US, it is a publicly traded company (NASDAQ: COIN) known as a major, regulated spot exchange with over 100 million users. It provides secure custodial services and trading for various digital assets.

The following fields have Enumerations:

* AGGRESSOR_SIDE - Indicates whether a trade resulted from an incoming buy or sell order.
* QUOTE_VENUE - Venue (MIC) from which a quote originates
* TRADE_VENUE - Identifies the venue where a trade was executed.   Typically a MIC, with the special values “XOFF” for off-exchange and “SINT” for Systematic Internaliser trades.
* TRADE_PERIOD - Market period during which a trade was executed.
* BOOK_TYPE - Type of order book or trading mechanism through which a trade was executed.

#### AGGRESSOR_SIDE - Enumeration

| Enumeration ID   | Enumeration Description   |
|------------------|---------------------------|
| B                | Buy                       |
| S                | Sell                      |

#### QUOTE_VENUE - Enumeration

| Enumeration ID   | Enumeration Description   |
|------------------|---------------------------|
| COINBASEUS       | COINBASE US               |

#### TRADE_VENUE - Enumeration

| Enumeration ID   | Enumeration Description   |
|------------------|---------------------------|
| COINBASEUS       | COINBASE US               |

#### TRADE_PERIOD - Enumeration

| Enumeration ID   | Enumeration Description   |
|------------------|---------------------------|
| -                | Regular trading           |

#### BOOK_TYPE - Enumeration

|   Enumeration ID | Enumeration Description   |
|------------------|---------------------------|
|                0 | Lit order book            |

