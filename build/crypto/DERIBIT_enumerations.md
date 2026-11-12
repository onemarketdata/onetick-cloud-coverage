# Deribit Enumerations

Trades, Quotes and Book depth from Deribit, with history from July 2026, covering futures, perpetuals and options. Founded in 2016, Deribit is the leading crypto options exchange, holding the large majority of bitcoin and ether options open interest, and has been part of Coinbase since Coinbase completed its 2.9 billion USD acquisition in August 2025. It is known for deep options liquidity and its institutional-grade matching engine and risk management.

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
| DERIBIT          | DERIBIT                   |

#### TRADE_VENUE - Enumeration

| Enumeration ID   | Enumeration Description   |
|------------------|---------------------------|
| DERIBIT          | DERIBIT                   |

#### TRADE_PERIOD - Enumeration

| Enumeration ID   | Enumeration Description   |
|------------------|---------------------------|
| -                | Regular trading           |

#### BOOK_TYPE - Enumeration

|   Enumeration ID | Enumeration Description   |
|------------------|---------------------------|
|                0 | Lit order book            |

