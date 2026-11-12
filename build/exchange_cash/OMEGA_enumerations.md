# Omega ATS Enumerations

Trades, Quotes and Book depth from Omega ATS, a Canadian alternative trading system that trades TSX- and TSX Venture-listed securities, with history from October 2017. Omega ATS is operated by Tradelogiq Markets (formerly Omega Securities), which also runs Lynx ATS, and is known for its inverted taker-maker pricing. Combined with the other Canadian venue databases, or CA_COMP for consolidated data, it shows how liquidity in Canadian stocks such as S&P/TSX 60 constituents is split across marketplaces.   A consolidated tape for all Canadian equity markets is provided in the CA_COMP dataset.

The following fields have Enumerations:

* AGGRESSOR_SIDE - Indicates whether a trade resulted from an incoming buy or sell order.
* BOOK_TYPE - Type of order book or trading mechanism through which a trade was executed.
* BYPASS - Identifies whether the trade resulted from a Bypass order
* MKT_PHASE - Indicates the instrument’s current market phase, as specified by the trading venue
* ODD_LOT - Indicates whether a trade was an odd lot
* OMD_STATUS - Indicates an instrument’s current trading status. Values are normalized across all DBs.
* ORDER_TYPE - Type of order.
* REASON_CODE - Reason for an instrument status update
* SPECIAL_TERMS - Indicates any non-standard settlement / execution terms associated with a trade
* TRADE_PERIOD - Market period during which a trade was executed.
* TRADE_TYPE - Type of trade
* UPDATE_TYPE - Type of update

#### AGGRESSOR_SIDE - Enumeration

| Enumeration ID   | Enumeration Description                          |
|------------------|--------------------------------------------------|
| ‘””’             | Undefined (e.g. off-book trades, auction trades) |
| B                | Buy                                              |
| S                | Sell                                             |

#### BOOK_TYPE - Enumeration

|   Enumeration ID | Enumeration Description   |
|------------------|---------------------------|
|                0 | Lit order book            |
|                1 | Off-book                  |
|                3 | Odd lot book              |
|                4 | Special terms book        |

#### BYPASS - Enumeration

| Enumeration ID   | Enumeration Description   |
|------------------|---------------------------|
| ‘””’             | Not a bypass trade        |
| Y                | Bypass trade              |

#### MKT_PHASE - Enumeration

| Enumeration ID   | Enumeration Description                  |
|------------------|------------------------------------------|
| B                | Market-wide circuit breaker              |
| C                | End of transmission                      |
| E                | End of system hours                      |
| H                | Halted                                   |
| M                | End of market hours                      |
| O                | Start of messages                        |
| Q                | Start of market hours                    |
| R                | Resume after market-wide circuit breaker |
| S                | Start of system hours                    |
| T                | Trading                                  |

#### ODD_LOT - Enumeration

| Enumeration ID   | Enumeration Description   |
|------------------|---------------------------|
| ‘””’             | Board lot                 |
| Y                | Odd lot                   |

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

#### ORDER_TYPE - Enumeration

| Enumeration ID   | Enumeration Description   |
|------------------|---------------------------|
| L                | Limit order               |

#### REASON_CODE - Enumeration

| Enumeration ID   | Enumeration Description   |
|------------------|---------------------------|
| ‘””’             | Unspecified               |
| B                | Business halt             |
| R                | Regulatory halt           |

#### SPECIAL_TERMS - Enumeration

| Enumeration ID   | Enumeration Description                |
|------------------|----------------------------------------|
| ‘””’             | No special terms (standard settlement) |
| C                | Cash                                   |
| DD               | Delayed delivery                       |
| ND               | Next day                               |

#### TRADE_PERIOD - Enumeration

| Enumeration ID   | Enumeration Description   |
|------------------|---------------------------|
| -                | Regular trading           |

#### TRADE_TYPE - Enumeration

| Enumeration ID   | Enumeration Description   |
|------------------|---------------------------|
| ‘””’             | Regular trade             |
| D                | Derivative-related cross  |
| H                | Hidden order execution    |
| I                | Internal cross            |
| M                | Intentional cross         |

#### UPDATE_TYPE - Enumeration

| Enumeration ID   | Enumeration Description   |
|------------------|---------------------------|
| A                | Add                       |
| D                | Delete                    |
| F                | Fill                      |
| M                | Modify                    |
| P                | Partial fill              |

