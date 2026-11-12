# JSE Derivatives (SAFEX) Enumerations

Futures and spreads with Trades, Quotes and bars from the JSE’s derivatives markets, with history from March 2016, including SAFEX equity and index derivatives, commodity derivatives such as white and yellow maize and wheat, and currency derivatives such as USD/ZAR futures. Key index futures are on the FTSE/JSE Top 40.

The following fields have Enumerations:

* AGGRESSOR_SIDE - Indicates whether a trade resulted from an incoming buy or sell order.
* BOOK_TYPE - Type of order book or trading mechanism through which a trade was executed.
* OMD_STATUS - Indicates an instrument’s current trading status. Values are normalized across all DBs.
* TRADE_PERIOD - Market period during which a trade was executed.
* TRADE_TYPE - Type of trade

#### AGGRESSOR_SIDE - Enumeration

| Enumeration ID   | Enumeration Description                                          |
|------------------|------------------------------------------------------------------|
| ‘””’             | Undefined (e.g. auction trades, implied trades, off-book trades) |
| B                | Buy                                                              |
| S                | Sell                                                             |

#### BOOK_TYPE - Enumeration

|   Enumeration ID | Enumeration Description   |
|------------------|---------------------------|
|                0 | Lit order book            |
|                1 | Off-book                  |
|                6 | Auction book              |

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
| I                | Intraday auction          |
| O                | Opening auction           |
| U                | Unscheduled auction       |

#### TRADE_TYPE - Enumeration

| Enumeration ID   | Enumeration Description                                                                     |
|------------------|---------------------------------------------------------------------------------------------|
| 0                | Standard trade                                                                              |
| 1                | Auction trade                                                                               |
| 4001             | Negotiated trade                                                                            |
| 4010             | Exchange for Physical                                                                       |
| 4011             | Exchange for Risk                                                                           |
| 4012             | Professional Client                                                                         |
| 4013             | Delta trade                                                                                 |
| 4014             | Late trade                                                                                  |
| 4015             | Roll trade                                                                                  |
| 4016             | Option strategy trade                                                                       |
| 4017             | Net-off                                                                                     |
| 4018             | Non-standard strategy trade                                                                 |
| 4019             | CFD trade report                                                                            |
| 4020             | Strategy trade                                                                              |
| 4022             | Trade Bust                                                                                  |
| 4023             | Price Adjust                                                                                |
| 4024             | Reported trade                                                                              |
| 99               | Auction trade                                                                               |
| FXA              | FX Auction trade                                                                            |
| HO               | Standard trade against hidden order                                                         |
| LEG              | Strategy leg trade [Trade reported on each outright leg when two spread orders are matched] |

