# OKX (formerly OKEx) Enumerations

Trades, Quotes and Book depth from OKX, with spot and futures history from August 2024 and options from September 2026. OKX is a major global cryptocurrency exchange owned by OK Group, whose roots go back to Okcoin, founded by Star Xu in 2013; the exchange, formerly OKEx, rebranded as OKX in January 2022. It offers spot, derivatives and Web3 wallet services and relaunched in the US in 2025.

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
| OKX              | OKX                       |

#### TRADE_VENUE - Enumeration

| Enumeration ID   | Enumeration Description   |
|------------------|---------------------------|
| OKX              | OKX                       |

#### TRADE_PERIOD - Enumeration

| Enumeration ID   | Enumeration Description   |
|------------------|---------------------------|
| -                | Regular trading           |

#### BOOK_TYPE - Enumeration

|   Enumeration ID | Enumeration Description   |
|------------------|---------------------------|
|                0 | Lit order book            |

