# SGX-NZX Dairy Derivatives Enumerations

Futures, options and spreads from the SGX-NZX dairy derivatives market, with history from March 2026. Contracts are cash-settled against Global Dairy Trade (GDT) auction prices for products such as whole milk powder, skim milk powder, butter and anhydrous milk fat, plus NZ milk price futures, and are used to hedge global dairy prices.

The following fields have Enumerations:

* AGGRESSOR_SIDE - Indicates whether a trade resulted from an incoming buy or sell order.
* CALL_PUT_IND - “C” - Call option, “P” - Put option
* TRADE_TYPE - Type of trade
* TRADE_PERIOD - Market period during which a trade was executed.
* BOOK_TYPE - Type of order book or trading mechanism through which a trade was executed.
* TRADE_SESSION - Trading session from which a trade originates, e.g. “Day”, “Night”
* QUOTE_SESSION - Trading session from which the quote originates, e.g. “Day”, “Night”
* MKT_PHASE - Indicates the instrument’s current market phase, as specified by the trading venue
* OMD_STATUS - Indicates an instrument’s current trading status. Values are normalized across all DBs.

#### AGGRESSOR_SIDE - Enumeration

| Enumeration ID   | Enumeration Description                                          |
|------------------|------------------------------------------------------------------|
| ‘””’             | Undefined (e.g. auction trades, implied trades, off-book trades) |
| B                | Buy                                                              |
| S                | Sell                                                             |

#### CALL_PUT_IND - Enumeration

| Enumeration ID   | Enumeration Description   |
|------------------|---------------------------|
| C                | Call option               |
| P                | Put option                |

#### TRADE_TYPE - Enumeration

|   Enumeration ID | Enumeration Description   |
|------------------|---------------------------|
|                0 | Regular trade             |
|                2 | Combo to outright trade   |
|                3 | Combo to combo trade      |

#### TRADE_PERIOD - Enumeration

| Enumeration ID   | Enumeration Description   |
|------------------|---------------------------|
| A                | Auction                   |
| C                | Closing auction           |
| O                | Opening auction           |
| -                | Regular trading           |

#### BOOK_TYPE - Enumeration

| Enumeration ID   | Enumeration Description   |
|------------------|---------------------------|
| 0                | Lit order book            |
| S                | Strategy leg              |

#### TRADE_SESSION - Enumeration

| Enumeration ID   | Enumeration Description          |
|------------------|----------------------------------|
| T                | T session (current business day) |

#### QUOTE_SESSION - Enumeration

| Enumeration ID   | Enumeration Description          |
|------------------|----------------------------------|
| T                | T session (current business day) |

#### MKT_PHASE - Enumeration

|   Enumeration ID | Enumeration Description           |
|------------------|-----------------------------------|
|                0 | Closed                            |
|                1 | Order cancellation                |
|                2 | Halt                              |
|                3 | No cancellation                   |
|                4 | Open                              |
|                5 | Open (Mass Quote enabled)         |
|                6 | Pre-open                          |
|                7 | Break                             |
|                8 | Break                             |
|                9 | Transition (Change clearing date) |
|               12 | Surveillance intervention         |
|               13 | Series generation                 |
|               14 | Day order expiry                  |
|               15 | Close signal                      |
|               78 | Start of day                      |

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

