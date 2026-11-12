# Coinbase - International Exchange Enumerations

Trades, Quotes and Book depth from Coinbase International Exchange, with history from September 2024. Launched by Coinbase in May 2023 and licensed by the Bermuda Monetary Authority, it offers USDC-settled perpetual futures, starting with bitcoin and ether, to non-US institutional clients and, since late 2023, eligible non-US retail users. Since October 2026 liquidity has been moved for COINBASE_US for spot, and DERIBIT for Derivatives.

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
| COINBASEINTL     | COINBASE International    |

#### TRADE_VENUE - Enumeration

| Enumeration ID   | Enumeration Description   |
|------------------|---------------------------|
| COINBASEINTL     | COINBASE International    |

#### TRADE_PERIOD - Enumeration

| Enumeration ID   | Enumeration Description   |
|------------------|---------------------------|
| -                | Regular trading           |

#### BOOK_TYPE - Enumeration

|   Enumeration ID | Enumeration Description   |
|------------------|---------------------------|
|                0 | Lit order book            |

