# Korea Exchange - Derivatives Enumerations

Futures and spreads with Trades, Quotes and bars from the Korea Exchange derivatives market, with KOSPI derivatives from October 2013 and other contracts from April 2017. KOSPI 200 futures are among Asia’s most actively traded index futures, and the market also lists KOSDAQ 150 futures, Korean Treasury bond futures and USD/KRW futures.

The following fields have Enumerations:

* BOOK_TYPE - Type of order book or trading mechanism through which a trade was executed.
* TRADE_PERIOD - Market period during which a trade was executed.
* TRADE_TYPE - Type of trade

#### BOOK_TYPE - Enumeration

|   Enumeration ID | Enumeration Description   |
|------------------|---------------------------|
|                0 | Lit order book            |
|                1 | Off-book                  |

#### TRADE_PERIOD - Enumeration

| Enumeration ID   | Enumeration Description   |
|------------------|---------------------------|
| -                | Regular trading           |
| C                | Closing auction           |
| O                | Opening auction           |
| U                | Unscheduled auction       |

#### TRADE_TYPE - Enumeration

|   Enumeration ID | Enumeration Description   |
|------------------|---------------------------|
|               10 | Opening auction           |
|               11 | Delayed opening           |
|               20 | Auction                   |
|               30 | Closing auction           |
|               40 | Continuous trading        |
|               46 | Negotiated trade          |
|               50 | Volatility auction        |
|               51 | Delayed re-opening        |

