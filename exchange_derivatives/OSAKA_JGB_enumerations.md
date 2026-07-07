# Osaka Exchange - JGB Futures Enumerations

Osaka Exchange, Inc., renamed from Osaka Securities Exchange Co., Ltd., is the largest derivatives exchange in Japan, in terms of amount of business handled

The following fields have Enumerations:

* BOOK_TYPE - Type of order book or trading mechanism through which a trade was executed.
* CALL_PUT_IND - “C” - Call option, “P” - Put option
* TRADE_PERIOD - Market period during which a trade was executed.
* TRADE_TYPE - Type of trade

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

#### TRADE_PERIOD - Enumeration

| Enumeration ID   | Enumeration Description   |
|------------------|---------------------------|
| -                | Regular trading           |
| A                | Auction                   |
| C                | Closing auction           |
| O                | Opening auction           |
| U                | Unscheduled auction       |

#### TRADE_TYPE - Enumeration

|   Enumeration ID | Enumeration Description           |
|------------------|-----------------------------------|
|                0 | Regular trade                     |
|               20 | Auction trade                     |
|                3 | J-Net trade                       |
|               36 | Tailor-Made Combination leg trade |
|               43 | Trade from implied order          |
|                5 | J-Net cross trade                 |
|                7 | Standard Combination leg trade    |

