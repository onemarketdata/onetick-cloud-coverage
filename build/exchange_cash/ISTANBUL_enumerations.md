# Borsa Istanbul - Equities Enumerations

Trades, quotes and bars from Borsa Istanbul’s equity market, with history from November 2009. Borsa Istanbul is Turkey’s sole exchange, and its equity market covers Turkish stocks, ETFs and warrants. Covered stocks include constituents of the BIST 100 and BIST 30; index values are in ISTANBUL_IDX.

The following fields have Enumerations:

* AGGRESSOR_SIDE - Indicates whether a trade resulted from an incoming buy or sell order.
* AUCTION_TYPE - Type of auction from which an indicative auction price / auction imbalance originates.
* BOOK_TYPE - Type of order book or trading mechanism through which a trade was executed.
* CALL_PUT_IND - “C” - Call option, “P” - Put option
* MKT_PHASE - Indicates the instrument’s current market phase, as specified by the trading venue
* OMD_STATUS - Indicates an instrument’s current trading status. Values are normalized across all DBs.
* TRADE_PERIOD - Market period during which a trade was executed.
* TRADE_TYPE - Type of trade

#### AGGRESSOR_SIDE - Enumeration

| Enumeration ID   | Enumeration Description                          |
|------------------|--------------------------------------------------|
| ‘””’             | Undefined (e.g. auction trades, off-book trades) |
| B                | Buy                                              |
| S                | Sell                                             |

#### AUCTION_TYPE - Enumeration

| Enumeration ID   | Enumeration Description                 |
|------------------|-----------------------------------------|
| A                | Unspecified auction                     |
| C                | Closing auction                         |
| I                | Intraday auction                        |
| O                | Opening auction                         |
| P                | IPO / Public offering auction           |
| S                | Settlement (EDSP) auction               |
| U                | Unscheduled auction                     |
| c                | Post-close auction                      |
| o                | Opening auction (extended hours)        |
| p                | Auction initiated by market participant |
| u                | Unscheduled auction (extended hours)    |

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

#### MKT_PHASE - Enumeration

|   Enumeration ID | Enumeration Description                        |
|------------------|------------------------------------------------|
|                1 | Closed                                         |
|               10 | Suspended                                      |
|               11 | Trading at last price (Odd lot market)         |
|               12 | Continuous trading (Odd lot market)            |
|               13 | Volatility auction                             |
|               14 | One-sided buyback auction (hidden) uncrossing  |
|               15 | One-sided buyback auction (open) uncrossing    |
|               16 | One-sided issuing auction (hidden) uncrossing  |
|               17 | One-sided issuing auction (open) uncrossing    |
|               18 | After one-sided auction                        |
|                2 | Continuous trading                             |
|               20 | Single price auction uncrossing                |
|               21 | One-sided auction                              |
|               22 | Issuing auction (open) uncrossing              |
|               23 | Issuing auction (hidden) uncrossing            |
|               24 | Buyback auction (open) uncrossing              |
|               25 | Buyback auction (hidden) uncrossing            |
|               26 | Non-tradable                                   |
|               27 | Dissemination of price limits                  |
|                3 | Uncrossing                                     |
|                4 | Opening auction                                |
|                5 | Closing auction                                |
|               51 | Opening auction                                |
|               52 | One-sided auction                              |
|               53 | Volatility auction                             |
|               54 | Closing auction                                |
|               55 | Single price auction                           |
|               56 | Break after hours                              |
|               57 | Suspended after hours                          |
|               58 | Order cancellation                             |
|               59 | Circuit breaker auction                        |
|                6 | Break                                          |
|               60 | Circuit breaker auction                        |
|               61 | Market-wide circuit breaker auction uncrossing |
|               62 | Market-wide circuit breaker halt               |
|               63 | Market maker quoting period                    |
|                7 | Trading at last price                          |
|                8 | Intraday auction                               |
|                9 | Continuous trading (Primary market)            |
|               99 | Reset                                          |

#### OMD_STATUS - Enumeration

| Enumeration ID   | Enumeration Description       |
|------------------|-------------------------------|
| A                | Auction                       |
| B                | Break / Pause                 |
| C                | Closing auction               |
| D                | Delisted / Pending deletion   |
| H                | Halted                        |
| I                | Scheduled intraday auction    |
| M                | Mandatory quoting period      |
| N                | New instrument / Pre-listing  |
| O                | Opening auction               |
| P                | Pre-market                    |
| Q                | Indicative quoting period     |
| R                | Off-book trade reporting      |
| S                | Suspended                     |
| T                | Continuous trading            |
| U                | Unscheduled auction           |
| c                | Closed                        |
| i                | IPO / Public offering auction |
| n                | No market phase / Unspecified |
| o                | Order management              |
| p                | Post-market                   |
| t                | Trading at last price         |

#### TRADE_PERIOD - Enumeration

| Enumeration ID   | Enumeration Description           |
|------------------|-----------------------------------|
| -                | Regular trading                   |
| A                | Auction                           |
| C                | Closing auction                   |
| I                | Intraday auction                  |
| O                | Opening auction                   |
| P                | Public offering / buyback auction |
| T                | Trading at closing price          |
| U                | Unscheduled auction               |

#### TRADE_TYPE - Enumeration

| Enumeration ID   | Enumeration Description                    |
|------------------|--------------------------------------------|
| ‘””’             | Regular trade                              |
| BBO10            | Trade report at best bid/offer +/-10 ticks |
| LTP              | Trade report at last trade price           |
| LTP10            | Trade report at last trade price +/-10%    |
| LTP3             | Trade report at last trade price +/-3%     |
| LTP6             | Trade report at last trade price +/-6%     |
| WT               | Wholesale trade report                     |
| WTN              | Wholesale trade not settled by Takasbank   |

