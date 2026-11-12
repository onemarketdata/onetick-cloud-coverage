# Coinbase - US Exchange Enumerations

Trades, Quotes and Book depth from Coinbase’s US exchange, with spot history from September 2024 and futures from August 2026. Coinbase is the largest US-based cryptocurrency exchange, founded in 2012 by Brian Armstrong and Fred Ehrsam and publicly traded on Nasdaq (COIN), and is known as a major regulated spot venue offering trading and custody for a wide range of digital assets.

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

