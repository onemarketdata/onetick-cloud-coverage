# NYSE Auction Imbalance Data Enumerations

Opening and closing auction imbalance data for the New York Stock Exchange, with history from January 2020 and real-time data available. Messages report paired quantity, imbalance quantity and side and indicative match prices ahead of the NYSE opening and closing auctions, which set the official closing prices widely used for index and fund valuations.

The following fields have Enumerations:

* AUCTION_TYPE - Type of auction from which an indicative auction price / auction imbalance originates.
* COND - Condition code

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

#### COND - Enumeration

| Enumeration ID   | Enumeration Description              |
|------------------|--------------------------------------|
| ‘””’             | No condition                         |
| P                | Extreme closing imbalance            |
| R                | Regulatory closing auction imbalance |

