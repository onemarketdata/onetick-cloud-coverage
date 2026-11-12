# Hong Kong Stock Exchange Enumerations

Trades, quotes and bars from the Hong Kong Stock Exchange (HKEX), with history from May 2008, covering the Main Board and GEM as well as trading in mainland China A-shares through Shanghai and Shenzhen Stock Connect. Covered stocks include constituents of the Hang Seng Index, Hang Seng China Enterprises Index and Hang Seng TECH Index.

The following fields have Enumerations:

* AUCTION_TYPE - Type of auction from which an indicative auction price / auction imbalance originates.
* BOOK_TYPE - Type of order book or trading mechanism through which a trade was executed.
* CALL_PUT_IND - “C” - Call option, “P” - Put option
* MKT_PHASE - Indicates the instrument’s current market phase, as specified by the trading venue
* OMD_STATUS - Indicates an instrument’s current trading status. Values are normalized across all DBs.
* TRADE_PERIOD - Market period during which a trade was executed.
* TRADE_TYPE - Type of trade

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
|                3 | Odd lot book              |

#### CALL_PUT_IND - Enumeration

| Enumeration ID   | Enumeration Description   |
|------------------|---------------------------|
| C                | Call option               |
| P                | Put option                |

#### MKT_PHASE - Enumeration

|   Enumeration ID | Enumeration Description             |
|------------------|-------------------------------------|
|               10 | End of day                          |
|              105 | Reference price fixing              |
|              106 | No cancellation                     |
|              107 | Randomized closing auction matching |
|              108 | Randomized matching                 |
|               15 | Continuous trading                  |
|               16 | Closed                              |
|               17 | Exchange intervention               |
|                3 | Pre-trading                         |
|               36 | Opening auction matching            |
|                4 | Closing auction matching            |
|               44 | No cancel / modification            |
|                5 | Closing auction call                |
|               58 | Pause                               |
|               67 | Order cancellation                  |
|               69 | Opening auction call                |

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

| Enumeration ID   | Enumeration Description   |
|------------------|---------------------------|
| -                | Regular trading           |
| A                | Auction                   |
| C                | Closing auction           |
| O                | Opening auction           |
| U                | Unscheduled auction       |

#### TRADE_TYPE - Enumeration

|   Enumeration ID | Enumeration Description                |
|------------------|----------------------------------------|
|                0 | Automatch                              |
|              104 | Overseas trade                         |
|               15 | Non-direct off-exchange trade          |
|               20 | Late trade (previous day off-exchange) |
|               25 | Auction trade                          |
|               30 | Direct off-exchange trade              |
|               31 | Automatch internalised trade           |
|                4 | Odd lot                                |

