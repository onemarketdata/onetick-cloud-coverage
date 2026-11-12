# ICE Abu Dhabi Enumerations

Futures, spreads and indices with Trades, Quotes and bars from ICE Futures Abu Dhabi (IFAD), with history from August 2025. IFAD is home to Murban crude oil futures, the benchmark for Abu Dhabi’s Murban crude, and also lists micro index futures on the MSCI GCC, MSCI Qatar, MSCI UAE and MSCI India indices.

The following fields have Enumerations:

* CALL_PUT_IND - “C” - Call option, “P” - Put option
* OMD_STATUS - Indicates an instrument’s current trading status. Values are normalized across all DBs.

#### CALL_PUT_IND - Enumeration

| Enumeration ID   | Enumeration Description   |
|------------------|---------------------------|
| C                | Call option               |
| P                | Put option                |

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

